---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice warning %}}
⚠️ **Note:** All content below is provided for guidance and reference purposes only. Please rewrite it in your own words and do not copy any passage verbatim, including this notice, into your official report.
{{% /notice %}}

<div class="workshop-big-title">
BREAKING THE 90-DAY LIMIT OF EC2 CAPACITY MANAGER WITH AMAZON ATHENA
</div>

In large-scale AWS infrastructure management, controlling and forecasting server costs is always a challenging task for enterprises. To help engineers monitor resources, Amazon EC2 Capacity Manager provides a centralized view of On-Demand, Spot, and ODCR capacity usage across accounts and Regions throughout an organization.

However, a major limitation in real-world operations is that the system retains only up to 90 days of historical data in the AWS Management Console. This creates difficulties for FinOps teams that need to analyze long-term annual trends, plan budgets, or evaluate the effectiveness of previously purchased capacity reservations. This article provides a detailed overview of the architecture, automated partitioning workflow, and practical SQL scenarios for managing long-term infrastructure data.

## 1. Core advantages of the solution

The deployment architecture focuses on optimizing the system in two important areas: long-term data storage and intelligent large-scale data querying capabilities.

- **Overcoming the data retention limit:** The solution automatically packages hourly On-Demand, Spot, and ODCR infrastructure data into optimized compressed Parquet files, allowing enterprises to store the data permanently in Amazon S3 for annual trend analysis.
- **Automation with Partition Projection:** This eliminates the need to manually operate data-scanning tools such as AWS Glue Crawlers every day to update metadata. By configuring `TBLPROPERTIES` in Athena, the system automatically calculates and identifies new date- and hour-based folder partitions at query time.
- **Resource isolation through Bucket Policies:** Conditional statements such as `aws:SourceAccount` and `ArnLike` are applied to specific export paths, ensuring that write access is granted only to the EC2 Capacity Manager service according to the principle of least privilege.

## 2. System operational workflow

The solution's data-processing workflow is clearly divided into two independent stages through AWS service configurations:

- **During data export:** EC2 Capacity Manager receives the configuration and performs hourly scans to aggregate resource usage data across all accounts and Regions. The data is then compressed and uploaded directly to an S3 Bucket using a date- and hour-based partitioned folder structure.
- **During querying:** FinOps engineers execute SQL statements on Amazon Athena. Instead of scanning the entire bucket, Athena uses the configured Partition Projection parameters to calculate the exact folder paths that need to be read, enabling faster analysis with a minimal amount of scanned data.

<div class="image-holder large">
EC2 Capacity Manager
</div>

## 3. Technology selection and storage scope

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
      <td>Data Collection</td>
      <td>EC2 Capacity Manager</td>
      <td>Centrally collects On-Demand, Spot, and ODCR infrastructure usage data.</td>
    </tr>
    <tr>
      <td>Data Storage</td>
      <td>Amazon S3</td>
      <td>Provides long-term historical data storage using the compressed Parquet format.</td>
    </tr>
    <tr>
      <td>Metadata Store</td>
      <td>AWS Glue Data Catalog</td>
      <td>Stores table schema definitions for Amazon Athena to reference.</td>
    </tr>
    <tr>
      <td>Data Analytics</td>
      <td>Amazon Athena</td>
      <td>Executes advanced SQL statements to filter data and generate FinOps reports.</td>
    </tr>
  </tbody>
</table>

## 4. Cost optimization scenarios in practical deployment

The solution enables advanced infrastructure cost optimization through three practical SQL query scenarios applied directly to the system.

### Identifying underutilized ODCRs

The system uses mathematical functions such as `CAST` and `ROUND` to filter and accurately identify the `reservationid` of inefficient capacity reservations, such as those with utilization below 50% that are still generating charges. This allows enterprises to calculate hourly financial losses and take timely action by canceling or reallocating resources.

### Identifying peak load patterns

Instance Usage datasets are analyzed to calculate the average number of running servers during each hour of the day. This analysis helps determine exactly when the system reaches peak demand, providing a foundation for developing an appropriate resource-purchasing strategy.

### Intelligent internal resource sharing

Queries analyze data at the physical Availability Zone level to identify areas with excess capacity. This information allows enterprises to proactively allocate and share unused capacity with other teams and remove temporary testing resources after they are no longer required.

<div class="image-holder medium">
Athena SQL Query Results
</div>

## 5. Conclusion

The combination of EC2 Capacity Manager, Amazon S3, and Amazon Athena provides a comprehensive infrastructure management and cost optimization solution that overcomes standard data retention limits. This approach enables enterprises to move from reactively handling unexpected expenses to proactively managing data, optimizing infrastructure, and improving financial efficiency on the AWS Cloud.

**Original article:** https://aws.amazon.com/vi/blogs/compute/maximize-amazon-ec2-capacity-reservations-with-capacity-manager-data-exports/
