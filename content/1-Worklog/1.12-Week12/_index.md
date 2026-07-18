---
title: "Week 12 Worklog"
date: 2026-07-10
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 12: CloudWatch Alarm, Load Testing, S3 Backup, Verification, and Cleanup

### Week 12 Objectives:

* Create SNS Topic, CloudWatch Alarm, and run Load Testing according to the monitoring task group.
* Configure S3 Backup, KMS, IAM Policy/Role, and Export Snapshot.
* Perform Verification and Cleanup to complete the deployment.

### Tasks to be carried out this week:
| Date | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 07/06/2026 | - Create SNS Topic for alerting<br>&emsp; + Create a notification channel for monitoring alerts<br>&emsp; + Configure notification receiver information<br>&emsp; + Prepare SNS Topic for CloudWatch Alarm integration | 07/06/2026 | 07/06/2026 | https://000077.awsstudygroup.com/ |
| 07/07/2026 | - Create CloudWatch Alarm and run Load Testing<br>&emsp; + Select the metric to monitor<br>&emsp; + Attach alarm to the created SNS Topic<br>&emsp; + Run load testing to observe metric and alarm status | 07/07/2026 | 07/07/2026 | https://000008.awsstudygroup.com/ |
| 07/08/2026 | - Configure S3 Bucket and KMS for backup<br>&emsp; + Create bucket for backup/export data<br>&emsp; + Configure KMS encryption<br>&emsp; + Verify storage and encryption configuration after setup | 07/08/2026 | 07/08/2026 | https://000057.awsstudygroup.com/<br>https://000033.awsstudygroup.com/ |
| 07/09/2026 | - Create IAM Policy/Role and export snapshot<br>&emsp; + Create permissions required for backup/export tasks<br>&emsp; + Configure access to S3, KMS, and RDS<br>&emsp; + Export snapshot and verify data in S3 | 07/09/2026 | 07/09/2026 | https://000005.awsstudygroup.com/<br>https://000013.awsstudygroup.com/ |
| 07/10/2026 | - Verify deployment and clean up resources<br>&emsp; + Recheck deployed components<br>&emsp; + Confirm main steps are working correctly<br>&emsp; + Delete or stop unused AWS resources | 07/10/2026 | 07/10/2026 | https://000007.awsstudygroup.com/<br>https://cloudjourney.awsstudygroup.com/3-optimize/ |

### Week 12 Results:

* Created SNS Topic for alert notifications.
* Configured notification receiver information from SNS.
* Created CloudWatch Alarm based on the metric to monitor.
* Attached Alarm to SNS Topic for alert delivery.
* Ran Load Testing to observe metric changes and alarm status.
* Created S3 Bucket for backup or export data.
* Configured KMS encryption for data stored in S3.
* Created IAM Policy/Role for backup/export tasks.
* Configured required access to S3, KMS, and RDS.
* Exported snapshot and checked exported data in S3.
* Performed Verification to review deployed components.
* Cleaned up unused resources to reduce unnecessary charges.
* Completed the CloudWatch Alarm, Load Testing, S3 Backup, Verification, and Cleanup task groups using Cloud Journey/AWS Study Group references.