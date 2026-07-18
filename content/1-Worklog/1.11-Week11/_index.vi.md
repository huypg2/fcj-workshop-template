---
title: "Worklog Tuần 11"
date: 2026-07-03
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Tuần 11: Cấu hình Load Balancer và triển khai ứng dụng bằng ECS Fargate

### Mục tiêu tuần 11:

* Tạo Target Group, Application Load Balancer và Listener Rules.
* Chuẩn bị CloudWatch Log Group và IAM Role cho ECS.
* Đăng ký ECS Task Definition và khởi chạy ECS Service bằng Fargate.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 29/06/2026 | - Tạo Target Group cho ứng dụng<br>&emsp; + Chọn loại target phù hợp với ECS Fargate<br>&emsp; + Cấu hình port nhận request<br>&emsp; + Thiết lập health check để kiểm tra trạng thái task | 29/06/2026 | 29/06/2026 | https://000016.awsstudygroup.com/ |
| 30/06/2026 | - Tạo Application Load Balancer<br>&emsp; + Chọn VPC và subnet đã chuẩn bị<br>&emsp; + Gắn Security Group cho ALB<br>&emsp; + Kiểm tra trạng thái Load Balancer sau khi tạo | 30/06/2026 | 30/06/2026 | https://000067.awsstudygroup.com/ |
| 01/07/2026 | - Cấu hình Listener Rules cho ALB<br>&emsp; + Tạo listener để nhận request<br>&emsp; + Thiết lập rule điều hướng request về Target Group<br>&emsp; + Kiểm tra liên kết giữa listener, rule và target group | 01/07/2026 | 01/07/2026 | https://000067.awsstudygroup.com/ |
| 02/07/2026 | - Chuẩn bị Log Group và IAM Role cho ECS Fargate<br>&emsp; + Tạo CloudWatch Log Group để lưu log container<br>&emsp; + Chuẩn bị ECS Task Execution Role<br>&emsp; + Kiểm tra quyền pull image từ ECR và ghi log lên CloudWatch | 02/07/2026 | 02/07/2026 | https://000008.awsstudygroup.com/ |
| 03/07/2026 | - Đăng ký Task Definition và khởi chạy ECS Service<br>&emsp; + Khai báo image URI lấy từ Amazon ECR<br>&emsp; + Cấu hình CPU, memory, port mapping và biến môi trường<br>&emsp; + Launch service trên ECS Fargate và kiểm tra trạng thái task | 03/07/2026 | 03/07/2026 | https://000067.awsstudygroup.com/ |

### Kết quả đạt được tuần 11:

* Tạo được Target Group cho ứng dụng chạy trên ECS Fargate.
* Cấu hình được port và health check để Load Balancer kiểm tra trạng thái task.
* Tạo được Application Load Balancer trong VPC và subnet đã chuẩn bị.
* Gắn được Security Group phù hợp cho Load Balancer.
* Cấu hình được listener để tiếp nhận request.
* Tạo được Listener Rule để điều hướng request về Target Group.
* Tạo được CloudWatch Log Group phục vụ lưu log container.
* Chuẩn bị được ECS Task Execution Role để task có thể pull image từ ECR và ghi log lên CloudWatch.
* Đăng ký được ECS Task Definition dựa trên image URI đã lưu từ Amazon ECR.
* Cấu hình được CPU, memory, port mapping và biến môi trường cho container.
* Khởi chạy được ECS Service bằng Fargate.
* Kiểm tra được trạng thái task và service sau khi launch.
* Hoàn thành đúng nhóm công việc Load Balancer và ECS Fargate; nguồn tham khảo dùng tài liệu trong Cloud Journey/AWS Study Group.