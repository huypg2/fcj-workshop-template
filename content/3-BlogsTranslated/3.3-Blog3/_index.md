---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# BREAKING THE 90-DAY LIMIT OF EC2 CAPACITY MANAGER WITH AMAZON ATHENA

In large-scale AWS infrastructure management, controlling and forecasting server costs is always a difficult challenge for businesses. To help engineers monitor resources, Amazon EC2 Capacity Manager provides a centralized view of capacity usage, including On-Demand, Spot, and ODCR, across accounts and Regions throughout the entire organization.

However, a major bottleneck in real-world operations is that the system stores a maximum of only 90 days of historical data on the AWS Management Console. This causes many difficulties when FinOps teams need to analyze long-term yearly trends, plan budgets, or evaluate the effectiveness of previously purchased On-Demand Capacity Reservations (ODCR). This article summarizes the architecture, automated partitioning process, and practical SQL scenarios in detail to help manage long-term infrastructure data.

---

## 1. Core advantages of the solution

The deployment architecture focuses on optimizing the system based on two important aspects: long-term storage capability and intelligent data querying at scale.

- **Overcoming the data retention limit:** The solution allows all infrastructure data, including On-Demand, Spot, and ODCR, to be automatically packaged hourly into optimized compressed Parquet files using Snappy. This helps businesses store data permanently on Amazon S3 for yearly trend analysis.
- **Automation with Partition Projection:** This eliminates the need to manually operate data scanning tools such as AWS Glue Crawler every day to update metadata. By configuring `TBLPROPERTIES` in Athena, the system automatically calculates and identifies new date/hour folder partitions directly at query time.
- **Resource separation security through Bucket Policy:** Strict `Condition` statements such as `aws:SourceAccount` and `ArnLike` are applied to the specific export path, ensuring that write permissions are granted only to the EC2 Capacity Manager service according to the Least Privilege principle.

---

## 2. System workflow

The data processing flow of the solution is clearly divided into two independent phases through AWS service configuration:

- **When exporting data (Data Export):** EC2 Capacity Manager receives the configuration, periodically scans every hour, aggregates resource usage metrics from all accounts and Regions, then compresses and pushes the data directly to the S3 Bucket following the date/hour folder partition structure (`y=YYYY/m=MM/d=DD/h=HH`).
- **When querying:** FinOps engineers execute SQL statements on Amazon Athena. At this point, Athena does not scan the entire bucket. Instead, it relies on the Partition Projection configuration parameters to calculate the exact folder path that needs to be read, helping return analysis results within a few seconds with minimal scanned data.

---

![EC2 Capacity Manager](/images/105.png)

## 3. Technology selection and storage scope

| System component | Technology used | Role in the architecture |
| :--- | :--- | :--- |
| **Data Collection** | EC2 Capacity Manager | Collects centralized infrastructure usage data, including On-Demand, Spot, and ODCR |
| **Data Storage** | Amazon S3 | Stores long-term historical data in compressed Parquet format using Snappy |
| **Metadata Store** | AWS Glue Data Catalog | Stores table structure definitions (Schema) for Amazon Athena to reference |
| **Data Analytics** | Amazon Athena | Executes advanced SQL statements to filter and extract FinOps reports |

---

## 4. Cost optimization scenarios (FinOps) in practical deployment

The solution enables advanced infrastructure cost optimization through 3 practical SQL query scenarios applied directly to the system:

### Searching for wasted ODCR packages

The system uses advanced mathematical functions such as `CAST` and `ROUND` to filter and accurately identify the `reservationid` of underutilized capacity reservations with usage efficiency below 50% that are still being charged. It calculates the hourly wasted cost (`wasted_cost_usd`) so businesses can promptly cancel or reallocate resources.

### Identifying peak usage patterns

The dataset in the `Instance Usage` group is used to calculate the average number of actually running servers by each hour of the day, from 00:00 to 23:00. This analysis process helps accurately identify when the system reaches peak usage, providing a basis for making appropriate resource purchasing strategies.

### Intelligent internal resource sharing

The query goes deeper into data at the physical infrastructure Availability Zone level (`az-id`) to identify which zones have excess capacity. This data helps businesses proactively coordinate and share unused capacity with other teams, while also cleaning up all testing resources after completion.

---

![Athena SQL Query Results](/images/103.png)

## 5. Conclusion

The combination of EC2 Capacity Manager, S3, and Athena provides a comprehensive infrastructure management and cost optimization solution that goes beyond the normal storage limit. This approach helps businesses shift from passively handling unexpected costs to proactively controlling data, optimizing infrastructure, and improving financial efficiency on the AWS cloud.

Original article: https://aws.amazon.com/vi/blogs/compute/maximize-amazon-ec2-capacity-reservations-with-capacity-manager-data-exports/