---
title: "Week 10 Worklog"
date: 2026-06-26
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Week 10: VPC, Subnets, Security Groups, and Amazon RDS PostgreSQL

### Week 10 Objectives:

* Set up VPC, subnets, route tables, and NAT in deployment order.
* Configure Security Groups to control communication between components.
* Create DB Subnet Group, RDS Instance, and initialize the database.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | - Create a VPC as the private network for the system<br>&emsp; + Select a suitable CIDR range<br>&emsp; + Create a new VPC for the deployment environment<br>&emsp; + Verify VPC ID, status, and required DNS settings | 06/22/2026 | 06/22/2026 | https://000003.awsstudygroup.com/ |
| Tuesday | - Create subnets, route tables, and NAT based on the network structure<br>&emsp; + Create subnets across Availability Zones<br>&emsp; + Associate subnets with proper route tables<br>&emsp; + Configure NAT to support the required traffic flow | 06/23/2026 | 06/23/2026 | https://000092.awsstudygroup.com/ |
| Wednesday | - Create and configure Security Groups<br>&emsp; + Create security groups for required resource layers<br>&emsp; + Configure inbound and outbound rules according to the traffic flow<br>&emsp; + Review rules before creating database and compute resources | 06/24/2026 | 06/24/2026 | https://000003.awsstudygroup.com/ |
| Thursday | - Create DB Subnet Group for RDS<br>&emsp; + Select subnets for the database layer<br>&emsp; + Create DB Subnet Group so RDS can run inside the VPC<br>&emsp; + Verify subnet group before creating the RDS instance | 06/25/2026 | 06/25/2026 | https://000005.awsstudygroup.com/ |
| Friday | - Create RDS PostgreSQL and initialize the database<br>&emsp; + Create the RDS instance using prepared settings<br>&emsp; + Check endpoint, port, and database status<br>&emsp; + Initialize the database/schema for application use | 06/26/2026 | 06/26/2026 | https://000005.awsstudygroup.com/ |

### Week 10 Results:

* Created a dedicated VPC for deployment resources.
* Understood the role of CIDR block planning for VPC IP addressing.
* Created subnets across Availability Zones.
* Configured route tables and subnet associations based on the network flow.
* Configured NAT according to the workshop network task group.
* Created the required Security Groups.
* Configured inbound and outbound rules for each resource layer.
* Prepared DB Subnet Group for Amazon RDS deployment inside the VPC.
* Created RDS PostgreSQL after completing network and security setup.
* Checked endpoint, port, and RDS running status.
* Initialized the database/schema for ECS application deployment.
* Completed the VPC Networking, Security Groups, and RDS Database task groups using Cloud Journey/AWS Study Group references.