---
title: "Blog 1"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

<div class="workshop-big-title">
AUTOMATING CONTAINER APPLICATION DEPLOYMENT TO AMAZON ECS EXPRESS MODE WITH GITHUB ACTIONS
</div>

In the DevOps era, optimizing CI/CD pipelines to shorten product delivery time is a top priority. When applications are containerized, manual packaging and deployment processes are often time-consuming and prone to errors.

Automation using GitHub Actions combined with Amazon ECS Express Mode simplifies the entire infrastructure, from networking and load balancing to resource provisioning, without requiring manual configuration. This article summarizes the architecture, operational workflow, and practical experience of building a secure and fully automated CI/CD pipeline from source code to a live environment.

## 1. Core advantages of the solution

The system is designed to optimize deployment speed and eliminate potential security risks through modern mechanisms:

- **Secure authentication through OIDC:** Instead of storing static credentials such as long-term AWS Access Keys in GitHub Secrets, the system establishes a trust mechanism through OpenID Connect. Each time the workflow runs, GitHub Actions automatically assumes a short-term IAM role to interact with AWS.
- **Infrastructure automation with ECS Express Mode:** Express Mode can automatically configure and manage complex components, including Application Load Balancers, Target Groups, Security Groups, CPU-based Auto Scaling, and a ready-to-use access URL with an AWS-provided certificate.
- **Accurate version management:** After the Docker image is built, it is automatically tagged using the first seven characters of the Commit SHA. This allows the development team to easily trace the source code, manage versions, and quickly roll back when an issue occurs.

## 2. System operational workflow

The automated workflow is triggered as soon as a developer interacts with the source code repository:

- **CI stage:** When code is pushed to the main branch, GitHub Actions triggers the workflow. The system uses OIDC to securely connect to AWS, builds a Docker image from the source code, tags it based on the Commit SHA, and pushes the image to Amazon ECR.
- **CD stage:** After the image is successfully pushed, the `amazon-ecs-deploy-express-service` Action calls the AWS API to update the service. ECS Express Mode automatically creates or updates the cluster, orchestrates Tasks running on AWS Fargate, and routes traffic from the Load Balancer to the new container.

<div class="image-holder large">
CI/CD Architecture Diagram
</div>

## 3. Technology selection and system roles

<table class="work-table">
  <thead>
    <tr>
      <th>System component</th>
      <th>Technology used</th>
      <th>Role in the architecture</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>CI/CD Pipeline</td>
      <td>GitHub Actions</td>
      <td>Automates the entire process of building, tagging, pushing, and triggering application deployment.</td>
    </tr>
    <tr>
      <td>Container Storage</td>
      <td>Amazon ECR</td>
      <td>Centrally stores and securely manages Docker image versions.</td>
    </tr>
    <tr>
      <td>Container Orchestration</td>
      <td>Amazon ECS Express Mode</td>
      <td>Automatically manages services, networking configurations, and load balancing for containers.</td>
    </tr>
    <tr>
      <td>Serverless Compute</td>
      <td>AWS Fargate</td>
      <td>Provides compute resources for running containers without managing EC2 instances.</td>
    </tr>
    <tr>
      <td>Identity & Access</td>
      <td>IAM & OIDC Provider</td>
      <td>Provides passwordless authentication and short-term permissions based on the Least Privilege principle.</td>
    </tr>
  </tbody>
</table>

## 4. Technical considerations for practical deployment

During the process of configuring and optimizing the pipeline, several key points should be considered to ensure stable system operation.

### Applying least-privilege permissions to IAM Policies

To ensure information security, the IAM Policies attached to `github-actions-ecs-role` should be strictly limited. Instead of using the wildcard character `*` for all resources, the policies should specify the exact ARNs of the Amazon ECR Repository and Amazon ECS Cluster. This prevents a compromised repository from interfering with other AWS resources.

<div class="image-holder medium">
IAM OIDC Role
</div>

### Monitoring the automation process on GitHub Actions

When code is pushed to the main branch, the entire packaging process, from building the Dockerfile and logging in to Amazon ECR to calling the deployment command for ECS Express Mode, should be closely monitored through real-time logs. This helps detect dependency conflicts or permission errors at an early stage.

<div class="image-holder medium">
GitHub Actions Workflow
</div>

### Checking the service status on Amazon ECS Express Mode

After the workflow completes successfully, Express Mode automatically creates the routing and load-balancing configurations. The application container running on AWS Fargate can then be accessed directly through the default endpoint provided by AWS.

<div class="image-holder medium">
Amazon ECS Express Service
</div>

## 5. Conclusion

The combination of GitHub Actions and Amazon ECS Express Mode provides a streamlined, powerful, and highly secure CI/CD solution for containerized applications. By removing the burden of managing network infrastructure and servers, the development team can focus entirely on optimizing source code, improving product quality, and accelerating application releases.

**Original article:** https://aws.amazon.com/blogs/containers/automated-deployments-with-github-actions-for-amazon-ecs-express-mode/
