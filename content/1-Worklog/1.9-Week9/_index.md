---
title: "Week 9 Worklog"
date: 2026-06-19
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 9: Deployment Environment Preparation, AWS CLI, and Amazon ECR

### Week 9 Objectives:

* Prepare the deployment environment following the opening workshop tasks.
* Configure AWS CLI to operate AWS resources from the command line.
* Build Docker images and push them to Amazon ECR for ECS Fargate deployment.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | - Review deployment architecture and execution order<br>&emsp; + Identify AWS components required for deployment<br>&emsp; + Prepare the execution order from environment, image, network, database, to compute<br>&emsp; + Record required values such as Region, repository name, and resource names | 06/15/2026 | 06/15/2026 | https://cloudjourney.awsstudygroup.com/ |
| Tuesday | - Prepare prerequisites before creating resources<br>&emsp; + Check AWS account and deployment Region<br>&emsp; + Review IAM permissions required for deployment<br>&emsp; + Verify Docker and local tools before building images | 06/16/2026 | 06/16/2026 | https://000002.awsstudygroup.com/ |
| Wednesday | - Configure AWS CLI on the practice machine<br>&emsp; + Set up AWS CLI access information<br>&emsp; + Verify configuration using account authentication commands<br>&emsp; + Ensure CLI can be used for later ECR and ECS steps | 06/17/2026 | 06/17/2026 | https://000011.awsstudygroup.com/ |
| Thursday | - Build and standardize Docker images for ECR<br>&emsp; + Build image from the project source<br>&emsp; + Tag the image using the ECR repository format<br>&emsp; + Log Docker in to Amazon ECR using AWS CLI | 06/18/2026 | 06/18/2026 | https://000015.awsstudygroup.com/ |
| 06/19/2026 | - Push image to Amazon ECR and verify it<br>&emsp; + Push the tagged image to the ECR repository<br>&emsp; + Check image tag, digest, and update time<br>&emsp; + Save the image URI for ECS Task Definition | 06/19/2026 | 06/19/2026 | https://000067.awsstudygroup.com/ |

### Week 9 Results:

* Defined the infrastructure and application deployment order according to the workshop direction.
* Prepared Region, resource names, and required components before working on AWS.
* Checked AWS account and IAM permissions to reduce permission errors during resource creation.
* Prepared the local environment with Docker and AWS CLI.
* Configured AWS CLI and confirmed account access from the command line.
* Understood how AWS CLI supports ECR login, image push, and later deployment operations.
* Built Docker images from the project source.
* Tagged images using the correct Amazon ECR repository format.
* Logged Docker in to Amazon ECR using AWS CLI.
* Pushed images to ECR and verified them after upload.
* Recorded image URIs for ECS Task Definition.
* Completed the preparation, AWS CLI, and ECR task group using Cloud Journey/AWS Study Group references.