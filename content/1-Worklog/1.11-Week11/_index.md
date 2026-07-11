---
title: "Week 11 Worklog"
date: 2026-07-03
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 11 Objectives:

* Review and connect the payment system microservices in the local environment before cloud deployment.
* Prepare the AWS architecture for the topic **Deploying a High-Performance Payment System on AWS ECS Fargate with Private Subnets, RDS PostgreSQL, and S3 Backup**.
* Package services as Docker images, push them to Amazon ECR, and prepare ECS Fargate runtime configuration.
* Set up foundational components such as VPC, private subnets, Internal ALB, RDS PostgreSQL, ElastiCache Redis, IAM Roles, Security Groups, and CloudWatch.

### Tasks to be carried out this week:
| Date | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 06/26/2026 | - Review source code and local runtime configuration<br>&emsp; + Run API Gateway, Payment Service, Account Service, Transaction Service, PostgreSQL, and Redis together<br>&emsp; + Check health endpoints and the Payment Service to Account Service flow<br>&emsp; + Adjust environment variables, ports, connection strings, and schema issues | 06/26/2026 | 06/26/2026 | Project source code, Docker Compose |
| 06/27/2026 | - Standardize configuration before AWS deployment<br>&emsp; + Separate configuration for each service<br>&emsp; + Identify variables required in Task Definitions such as database URL, Redis endpoint, service port, and profile settings<br>&emsp; + Review Dockerfiles to ensure images can be built consistently | 06/27/2026 | 06/27/2026 | Dockerfile, application configuration |
| 06/28/2026 | - Finalize the AWS architecture design<br>&emsp; + Define the request flow from API Gateway to VPC Link, Internal ALB, and ECS Fargate<br>&emsp; + Place services in private subnets to reduce direct Internet exposure<br>&emsp; + Identify the roles of RDS PostgreSQL, ElastiCache Redis, and S3 Backup in the architecture | 06/28/2026 | 06/28/2026 | AWS architecture documents |
| 06/29/2026 | - Create and configure basic networking components<br>&emsp; + Prepare VPC, subnets, route tables, and security groups for each layer<br>&emsp; + Design rules so API Gateway enters the system only through VPC Link and Internal ALB<br>&emsp; + Restrict access to RDS and Redis to required ECS Services only | 06/29/2026 | 06/29/2026 | Amazon VPC, Security Group |
| 06/30/2026 | - Package applications and store images<br>&emsp; + Create Amazon ECR repositories for each service<br>&emsp; + Build Docker images for Account, Payment, and Transaction Service<br>&emsp; + Push images to ECR for use in ECS Task Definitions | 06/30/2026 | 06/30/2026 | Amazon ECR, Docker |
| 07/01/2026 | - Create ECS Cluster, Task Definitions, and ECS Services<br>&emsp; + Define image, port, CPU, memory, and environment variables for each task<br>&emsp; + Attach suitable IAM Roles so tasks can read secrets and write logs<br>&emsp; + Create Fargate ECS Services and check task status after startup | 07/01/2026 | 07/01/2026 | Amazon ECS Fargate |
| 07/02/2026 | - Connect access, data, and monitoring layers<br>&emsp; + Create Internal ALB, target groups, and listener rules for services<br>&emsp; + Prepare RDS PostgreSQL, ElastiCache Redis, Secrets Manager, and CloudWatch Logs<br>&emsp; + Check startup logs, health checks, and service connectivity to database/cache | 07/02/2026 | 07/02/2026 | ALB, RDS, ElastiCache, CloudWatch |

### Week 11 Achievements:

* Completed local verification and standardization of the microservice system. API Gateway, Payment Service, Account Service, and Transaction Service can run together with PostgreSQL and Redis and communicate through the expected flow.

* Reviewed common configuration issues before AWS deployment, including environment variables, service ports, connection strings, database schema, and API paths between services. This reduces errors when moving from local to cloud.

* Built an AWS architecture direction suitable for a high-performance payment system. The request flow is designed as API Gateway entering the VPC through VPC Link, then Internal ALB distributing traffic to ECS Services running on Fargate.

* Designed a model where backend services run inside private subnets. This keeps services from being reached directly from the Internet while still allowing controlled access through the entry layer.

* Identified the responsibility of each architecture component: ECS Fargate runs containerized applications, RDS PostgreSQL stores business data, ElastiCache Redis supports cache/lock/rate limiting, S3 stores backup or exported data, and CloudWatch collects logs and metrics.

* Packaged services as Docker images and pushed them to Amazon ECR. Centralized image storage makes ECS deployment clearer, version management easier, and service updates more convenient.

* Created ECS Cluster, Task Definitions, and ECS Services for the main services. Task Definitions describe the image, port, CPU, memory, environment variables, and permissions needed for services to run on Fargate.

* Set up basic security components such as IAM Roles and Security Groups. Permissions are separated by responsibility, and network access between ALB, ECS, RDS, and Redis is restricted based on actual needs.

* Prepared the data layer with RDS PostgreSQL and ElastiCache Redis. Services can use the database for account, payment, and transaction data, while Redis supports high-speed operations.

* Enabled CloudWatch Logs to observe ECS task startup and runtime behavior. Centralized logs make it easier to inspect service errors, database/cache connection status, and issues before load testing.

* By the end of the week, the AWS deployment foundation was ready for end-to-end verification, idempotency and rate-limit checks, and load testing in the following week.