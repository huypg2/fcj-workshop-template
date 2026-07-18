---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Automating the Deployment Process of Container Applications to Amazon ECS Express Mode with GitHub Actions

In the DevOps era, optimizing CI/CD pipelines to shorten the time required to bring products to market is a top priority. When applications are containerized, the manual packaging and deployment process is often prone to errors and time-consuming.

The automation solution using **GitHub Actions** combined with **Amazon ECS Express Mode** helps simplify the entire infrastructure, from networking and load balancing to resource provisioning, without requiring manual configuration. This article summarizes the architecture, operating process, and practical experience when building a secure and fully automated CI/CD pipeline from source code to the live runtime environment.

---

## 1. Core advantages of the solution

The system is designed to optimize deployment speed and eliminate potential security risks through modern mechanisms:

- **Secure authentication through OIDC:** Instead of storing static credentials such as long-term AWS Access Keys in GitHub Secrets, which may cause data leakage risks, the system establishes a trust mechanism through OpenID Connect (OIDC). Each time the workflow runs, GitHub Actions automatically assumes a short-term IAM role to interact with AWS.
- **Infrastructure automation with ECS Express Mode:** The key advantage of Express Mode is its ability to automatically set up and manage complex components, including Application Load Balancer (ALB), Target Groups, Security Groups, CPU-based Auto Scaling, and a ready-to-use access URL with an AWS-provided identity certificate.
- **Accurate version management (Traceability):** After the Docker image is built, it is automatically tagged based on the first 7 characters of the Commit SHA. This helps the development team easily trace source code, control versions, and perform rollback quickly when incidents occur.

---

## 2. System workflow

The automated workflow is triggered as soon as a developer interacts with the source code repository:

- **CI phase (Continuous Integration):** When code is pushed to the `main` branch, GitHub Actions triggers the workflow. The system uses OIDC to securely connect to AWS, builds a Docker image from the source code, tags it according to the Commit SHA, and pushes the image to the private Amazon ECR repository.
- **CD phase (Continuous Deployment):** After the image is successfully pushed, the `amazon-ecs-deploy-express-service` action calls the AWS API to update the service. ECS Express Mode automatically creates or updates the cluster, orchestrates tasks running on the serverless AWS Fargate platform, and routes traffic from the Load Balancer to the new container smoothly.

---

![CI/CD Architecture Diagram](/images/106.png)

## 3. Technology selection and system roles

| System component | Technology used | Role in the architecture |
| :--- | :--- | :--- |
| **CI/CD Pipeline** | GitHub Actions | Automates the entire process of building, tagging, pushing, and triggering application deployment |
| **Container Storage** | Amazon ECR | Centrally stores and securely manages Docker Image versions |
| **Container Orchestration** | Amazon ECS Express Mode | Automatically manages services, network configuration, and load balancing for containers |
| **Serverless Compute** | AWS Fargate | Provides compute resources to run containers without managing EC2 instances |
| **Identity & Access** | IAM & OIDC Provider | Provides passwordless authentication and short-term permissions based on the Least Privilege principle |

---

## 4. Technical notes for practical deployment

Through the process of configuring and optimizing the pipeline, several key points should be noted to ensure stable system operation:

### Grant minimum permissions for IAM Policy

To ensure information security, IAM Policies attached to the `github-actions-ecs-role` should be restricted carefully. Instead of using the wildcard character `*` for all resources, the exact ARN of the Amazon ECR Repository and the specific Amazon ECS Cluster should be limited to prevent a compromised repository from affecting other resources.

![IAM OIDC Role](/images/78.png)

### Monitor the automation process on GitHub Actions

When code is pushed to the main branch, the entire packaging process, from building the Dockerfile and logging in to ECR to calling the deployment command to ECS Express Mode, should be closely monitored through real-time logs to detect dependency conflicts or permission errors early.

![GitHub Actions Workflow](/images/77.png)

### Check the service status on Amazon ECS Express Mode

After the workflow reports success, Express Mode automatically creates routing and load balancing configurations. The containerized application running on AWS Fargate can then be accessed directly through the default endpoint provided by AWS.

![Amazon ECS Express Service](/images/79.png)

---

## 5. Conclusion

The combination of GitHub Actions and Amazon ECS Express Mode provides a streamlined, powerful, and highly secure CI/CD solution for containerized applications. By removing the burden of managing network infrastructure and servers, the development team can focus entirely on optimizing source code, improving product quality, and accelerating application release speed.

Original article: https://aws.amazon.com/blogs/containers/automated-deployments-with-github-actions-for-amazon-ecs-express-mode/