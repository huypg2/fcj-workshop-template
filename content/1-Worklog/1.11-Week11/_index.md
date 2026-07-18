---
title: "Week 11 Worklog"
date: 2026-07-03
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 11: Load Balancer Configuration and ECS Fargate Deployment

### Week 11 Objectives:

* Create Target Group, Application Load Balancer, and Listener Rules.
* Prepare CloudWatch Log Group and IAM Role for ECS.
* Register ECS Task Definition and launch ECS Service with Fargate.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | - Create Target Group for the application<br>&emsp; + Select target type suitable for ECS Fargate<br>&emsp; + Configure request receiving port<br>&emsp; + Configure health check for task status verification | 06/29/2026 | 06/29/2026 | https://000016.awsstudygroup.com/ |
| Tuesday | - Create Application Load Balancer<br>&emsp; + Select the prepared VPC and subnets<br>&emsp; + Attach Security Group to ALB<br>&emsp; + Verify Load Balancer status after creation | 06/30/2026 | 06/30/2026 | https://000067.awsstudygroup.com/ |
| Wednesday | - Configure Listener Rules for ALB<br>&emsp; + Create listener to receive requests<br>&emsp; + Configure rule to forward requests to Target Group<br>&emsp; + Verify the relationship between listener, rule, and target group | 07/01/2026 | 07/01/2026 | https://000067.awsstudygroup.com/ |
| Thursday | - Prepare Log Group and IAM Role for ECS Fargate<br>&emsp; + Create CloudWatch Log Group for container logs<br>&emsp; + Prepare ECS Task Execution Role<br>&emsp; + Verify permissions to pull images from ECR and write logs to CloudWatch | 07/02/2026 | 07/02/2026 | https://000008.awsstudygroup.com/ |
| Friday | - Register Task Definition and launch ECS Service<br>&emsp; + Declare image URI from Amazon ECR<br>&emsp; + Configure CPU, memory, port mapping, and environment variables<br>&emsp; + Launch service on ECS Fargate and check task status | 07/03/2026 | 07/03/2026 | https://000067.awsstudygroup.com/ |

### Week 11 Results:

* Created Target Group for the application running on ECS Fargate.
* Configured port and health check so Load Balancer can check task health.
* Created Application Load Balancer in the prepared VPC and subnets.
* Attached the proper Security Group to the Load Balancer.
* Configured listener to receive requests.
* Created Listener Rule to forward requests to Target Group.
* Created CloudWatch Log Group for container logs.
* Prepared ECS Task Execution Role so tasks can pull images from ECR and write logs to CloudWatch.
* Registered ECS Task Definition using the image URI from Amazon ECR.
* Configured CPU, memory, port mapping, and environment variables for the container.
* Launched ECS Service using Fargate.
* Checked task and service status after launch.
* Completed the Load Balancer and ECS Fargate task groups using Cloud Journey/AWS Study Group references.