---
title: "Week 11 Worklog"
date: 2026-07-03
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---


### Week 11: AWS Infrastructure Deployment, ECS Fargate, Monitoring, and Data Backup

### Week 11 Objectives:

* Package the Backend and Frontend applications with Docker for AWS deployment.
* Set up VPC networking, Security Groups, RDS PostgreSQL, and Bastion Host.
* Configure Load Balancer and deploy the application using Amazon ECS Fargate.
* Set up CloudWatch Alarm, SNS, and data backup with S3 Backup and KMS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | - Package the application and manage ECR Repository<br>&emsp; + Package Backend and Frontend source code with Docker<br>&emsp; + Create Amazon ECR Repositories for backend and frontend<br>&emsp; + Build and push Docker images from the development environment to Amazon ECR | 29/06/2026  | 29/06/2026  |  |
| Tuesday | - Set up VPC networking and Security Groups<br>&emsp; + Create a 3-tier VPC across 2 Availability Zones with Public/Private Subnets<br>&emsp; + Configure Internet Gateway and NAT Gateway for outbound connectivity<br>&emsp; + Set up isolated Security Groups for ALB, ECS Fargate, RDS, and Bastion Host | 30/06/2026 | 30/06/2026 |  |
| Wednesday | - Create RDS PostgreSQL database and Bastion Host<br>&emsp; + Create DB Subnet Group and launch Amazon RDS PostgreSQL in Private Subnet<br>&emsp; + Launch EC2 Bastion Host in Public Subnet<br>&emsp; + Connect securely through Bastion Host to import SQL Schema into RDS | 01/07/2026 | 0/07/2026 |  |
| Thursday | - Configure Load Balancer and deploy ECS Fargate<br>&emsp; + Create Target Groups and a public Application Load Balancer<br>&emsp; + Create ECS Cluster and define Task Definitions for backend with Redis sidecar<br>&emsp; + Deploy ECS Services on Fargate and configure ECS Service Auto Scaling | 02/07/2026 | 02/07/2026 |  |
| Friday | - Configure CloudWatch Alarm and S3 Backup with KMS<br>&emsp; + Configure Amazon SNS Topic to send email alerts when infrastructure is overloaded<br>&emsp; + Set up CloudWatch Alarms to monitor CPU utilization threshold<br>&emsp; + Create S3 Bucket, KMS Key, and export RDS Snapshot to Amazon S3 | 03/07/2026 | 03/07/2026 |  |

### Week 11 Results:

* Packaged Backend and Frontend source code with Docker.
* Created Amazon ECR Repositories to store Docker images for backend and frontend.
* Built and pushed Docker images from the development environment to Amazon ECR.
* Set up a 3-tier VPC across 2 Availability Zones with Public and Private Subnets.
* Configured Internet Gateway and NAT Gateway to support the required network connectivity.
* Created separate Security Groups for ALB, ECS Fargate, RDS, and Bastion Host.
* Created DB Subnet Group for deploying Amazon RDS inside the VPC.
* Launched Amazon RDS PostgreSQL in Private Subnet.
* Launched EC2 Bastion Host in Public Subnet for secure administrative access.
* Connected to RDS through Bastion Host and imported the initial SQL Schema.
* Created Target Groups for the application.
* Created a public Application Load Balancer to receive requests.
* Created ECS Cluster for container deployment.
* Defined Task Definitions for backend with Redis sidecar integration.
* Deployed ECS Services on AWS Fargate.
* Configured ECS Service Auto Scaling to support application scaling.
* Configured Amazon SNS Topic for email alert notifications.
* Set up CloudWatch Alarm to monitor CPU utilization.
* Created S3 Bucket and KMS Key for data backup.
* Exported RDS Snapshot to Amazon S3.
* Completed the infrastructure deployment, application deployment, monitoring, and backup tasks according to the workshop content.