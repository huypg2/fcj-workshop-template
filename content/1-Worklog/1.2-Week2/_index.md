---
title: "Week 2 Worklog"
date: 2026-05-03
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Week 2: Storage, Databases, Cache, DNS, Monitoring, and System Scaling

### Week 2 Objectives:

* Study common AWS storage and database services.
* Understand the role of cache, DNS, monitoring, and auto scaling in cloud systems.
* Get familiar with services that support small application deployment and scalable systems.
* Connect knowledge between storage, database, cache, monitoring, and resource scaling.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Studied Amazon S3, buckets, objects, storage classes, access control, and static data storage on AWS. | 27/04/2026 | 27/04/2026 | https://000057.awsstudygroup.com/ |
| Tuesday | Practiced static website hosting with Amazon S3, checked bucket policy, static website endpoint, and browser access. | 28/04/2026 | 28/04/2026 | https://000057.awsstudygroup.com/ |
| Wednesday | Studied Amazon RDS, DB instances, engines, backup, Multi-AZ, connection endpoints, and managed relational databases. | 29/04/2026 | 29/04/2026 | https://000005.awsstudygroup.com/ |
| Thursday | Studied Amazon DynamoDB, partition keys, sort keys, NoSQL tables, and the basic comparison between relational and NoSQL databases. | 30/04/2026 | 30/04/2026 | https://000060.awsstudygroup.com/ |
| Friday | Studied Amazon ElastiCache, Redis, Memcached, and the role of cache in reducing database query load and improving response time. | 01/05/2026 | 01/05/2026 | https://000061.awsstudygroup.com/ |
| Saturday | Studied Amazon Route 53, DNS records, hosted zones, and Amazon CloudWatch for metrics, logs, and alarms. | 02/05/2026 | 02/05/2026 | https://000010.awsstudygroup.com/<br>https://000008.awsstudygroup.com/ |
| Sunday | Studied EC2 Auto Scaling, Lightsail, and Lightsail Containers to understand small application deployment and scaling based on workload. | 03/05/2026 | 03/05/2026 | https://000006.awsstudygroup.com/<br>https://000045.awsstudygroup.com/<br>https://000046.awsstudygroup.com/ |

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