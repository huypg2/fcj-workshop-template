---
title: "Worklog Tuần 11"
date: 2026-07-03
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---


### Tuần 11: Cấu hình Load Balancer và triển khai ứng dụng bằng ECS Fargate

### Mục tiêu tuần 11:

* Tạo Target Group, Application Load Balancer và Listener Rules.
* Chuẩn bị CloudWatch Log Group và IAM Role cho ECS.
* Đăng ký ECS Task Definition và khởi chạy ECS Service bằng Fargate.

### Tuần 11: Triển khai hạ tầng AWS, ECS Fargate, giám sát và sao lưu dữ liệu

### Mục tiêu tuần 11:

* Đóng gói ứng dụng Backend và Frontend bằng Docker để chuẩn bị triển khai lên AWS.
* Thiết lập hạ tầng mạng VPC, Security Groups, RDS PostgreSQL và Bastion Host.
* Cấu hình Load Balancer và triển khai ứng dụng bằng Amazon ECS Fargate.
* Thiết lập CloudWatch Alarm, SNS và cơ chế sao lưu dữ liệu với S3 Backup, KMS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | - Đóng gói ứng dụng và quản lý ECR Repository<br>&emsp; + Đóng gói mã nguồn Backend và Frontend bằng Docker<br>&emsp; + Khởi tạo Amazon ECR Repository cho backend và frontend<br>&emsp; + Build và push Docker image từ môi trường phát triển lên Amazon ECR | 29/06/2026 | 29/06/2026 |  |
| Thứ 3 | - Thiết lập hạ tầng mạng VPC và Security Groups<br>&emsp; + Khởi tạo VPC 3-tier trên 2 Availability Zones với Public/Private Subnets<br>&emsp; + Cấu hình Internet Gateway và NAT Gateway cho kết nối đi ra ngoài<br>&emsp; + Thiết lập các Security Groups cách ly cho ALB, ECS Fargate, RDS và Bastion Host | 30/06/2026 | 30/06/2026 |  |
| Thứ 4 | - Khởi tạo cơ sở dữ liệu RDS PostgreSQL và Bastion Host<br>&emsp; + Tạo DB Subnet Group và khởi tạo Amazon RDS PostgreSQL trong Private Subnet<br>&emsp; + Khởi tạo máy chủ EC2 Bastion Host tại Public Subnet<br>&emsp; + Kết nối an toàn qua Bastion Host để nạp SQL Schema cho RDS | 01/07/2026 | 01/07/2026 |  |
| Thứ 5 | - Cấu hình Load Balancer và triển khai ECS Fargate<br>&emsp; + Khởi tạo Target Groups và Application Load Balancer công khai<br>&emsp; + Tạo ECS Cluster, định nghĩa Task Definitions cho backend tích hợp Redis sidecar<br>&emsp; + Triển khai ECS Services trên Fargate và cấu hình ECS Service Auto Scaling | 02/07/2026 | 02/07/2026 |  |
| Thứ 6 | - Giám sát CloudWatch Alarm và cơ chế S3 Backup KMS<br>&emsp; + Cấu hình Amazon SNS Topic gửi cảnh báo email khi hạ tầng quá tải<br>&emsp; + Thiết lập CloudWatch Alarms theo dõi ngưỡng CPU utilization<br>&emsp; + Khởi tạo S3 Bucket, KMS Key và thực hiện Export RDS Snapshot sang Amazon S3 | 03/07/2026 | 03/07/2026 |  |

### Kết quả đạt được tuần 11:

* Đóng gói được mã nguồn Backend và Frontend bằng Docker.
* Tạo được Amazon ECR Repository để lưu trữ Docker image của backend và frontend.
* Build và push được Docker image từ môi trường phát triển lên Amazon ECR.
* Thiết lập được mô hình VPC 3-tier trên 2 Availability Zones với Public Subnet và Private Subnet.
* Cấu hình được Internet Gateway và NAT Gateway để hỗ trợ kết nối mạng theo yêu cầu triển khai.
* Tạo được các Security Groups riêng cho ALB, ECS Fargate, RDS và Bastion Host.
* Tạo được DB Subnet Group để triển khai Amazon RDS trong VPC.
* Khởi tạo được Amazon RDS PostgreSQL trong Private Subnet.
* Khởi tạo được EC2 Bastion Host trong Public Subnet để hỗ trợ kết nối quản trị an toàn.
* Kết nối được đến RDS thông qua Bastion Host và nạp SQL Schema ban đầu.
* Tạo được Target Groups cho ứng dụng.
* Tạo được Application Load Balancer công khai để tiếp nhận request.
* Tạo được ECS Cluster phục vụ triển khai container.
* Định nghĩa được Task Definitions cho backend có tích hợp Redis sidecar.
* Triển khai được ECS Services trên AWS Fargate.
* Cấu hình được ECS Service Auto Scaling để hỗ trợ mở rộng ứng dụng.
* Cấu hình được Amazon SNS Topic để gửi cảnh báo qua email.
* Thiết lập được CloudWatch Alarm theo dõi CPU utilization.
* Tạo được S3 Bucket và KMS Key phục vụ sao lưu dữ liệu.
* Thực hiện được Export RDS Snapshot sang Amazon S3.
* Hoàn thành nhóm công việc triển khai hạ tầng, ứng dụng, giám sát và sao lưu theo nội dung workshop.