---
title: "Week 2 Worklog"
date: 2026-05-03
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 2: Storage, Databases, Cache, DNS, Monitoring, and System Scaling

### Week 2 Objectives:

* Study common AWS storage and database services.
* Understand the role of cache, DNS, monitoring, and auto scaling in cloud systems.
* Get familiar with services that support small application deployment and scalable systems.
* Connect knowledge between storage, database, cache, monitoring, and resource scaling.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Studied Amazon S3, buckets, objects, storage classes, access control, and static data storage on AWS. | 04/27/2026 | 04/27/2026 | https://docs.aws.amazon.com/s3/ |
| Tuesday | Practiced static website hosting with Amazon S3, checked bucket policy, static website endpoint, and browser access. | 04/28/2026 | 04/28/2026 | https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html |
| Wednesday | Studied Amazon RDS, DB instances, engines, backup, Multi-AZ, connection endpoints, and managed relational databases. | 04/29/2026 | 04/29/2026 | https://docs.aws.amazon.com/rds/ |
| Thursday | Studied Amazon DynamoDB, partition keys, sort keys, NoSQL tables, and the basic comparison between relational and NoSQL databases. | 04/30/2026 | 04/30/2026 | https://docs.aws.amazon.com/dynamodb/ |
| Friday | Studied Amazon ElastiCache, Redis, Memcached, and the role of cache in reducing database query load and improving response time. | 05/01/2026 | 05/01/2026 | https://docs.aws.amazon.com/elasticache/ |
| Saturday | Studied Amazon Route 53, DNS records, hosted zones, and Amazon CloudWatch for metrics, logs, and alarms. | 05/02/2026 | 05/02/2026 | https://docs.aws.amazon.com/route53/ |
| Sunday | Studied EC2 Auto Scaling, Lightsail, and Lightsail Containers to understand small application deployment and scaling based on workload. | 05/03/2026 | 05/03/2026 | https://docs.aws.amazon.com/autoscaling/ |

### Week 2 Results:

* Understood Amazon S3 as a highly scalable object storage service suitable for static data, backup, logs, and website assets.
* Practiced static website hosting with S3 and understood how bucket policy and website endpoints affect access.
* Understood the role of Amazon RDS in operating relational databases without managing all database infrastructure manually.
* Understood important RDS concepts such as DB instance, endpoint, backup, and Multi-AZ, which are useful for later RDS PostgreSQL usage.
* Distinguished between data suitable for relational databases and data suitable for NoSQL databases such as DynamoDB.
* Understood DynamoDB's role in systems requiring fast scaling, low latency, and reduced database server management.
* Understood how ElastiCache/Redis reduces database load, accelerates queries, and supports cache, distributed lock, or rate limiting.
* Understood how Route 53 supports DNS routing so users can access systems through domain names.
* Understood CloudWatch's role in system monitoring through logs, metrics, and alarms.
* Understood Auto Scaling and how systems can automatically increase or reduce resources based on load.
* Learned about Lightsail and Lightsail Containers as simpler options for small applications or testing environments.
* Connected S3, RDS, DynamoDB, Redis, Route 53, CloudWatch, and Auto Scaling into a scalable application architecture.