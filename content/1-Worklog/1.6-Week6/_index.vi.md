---
title: "Worklog Tuần 6"
date: 2026-05-29
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 6:

* **Chủ đề:** Độ tin cậy, hiệu suất và tối ưu chi phí.
* Tuần này tập trung vào sao lưu, phục hồi, kết nối mạng, xử lý bất đồng bộ và tối ưu chi phí vận hành.
* Tìm hiểu các giải pháp sao lưu, snapshot và chuẩn hóa image máy chủ.
* Nắm các mô hình kết nối mạng giữa nhiều VPC và hệ thống nhắn tin.
* Hiểu cách tối ưu tài nguyên, hạn ngạch và chi phí AWS.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 22/05/2026 | - Tìm hiểu AWS Backup, EBS Data Lifecycle Manager và phát hiện bất thường cho EBS Backups. <br> - Kết quả: Biết cách lập kế hoạch sao lưu, tự động hóa snapshot và theo dõi rủi ro backup. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 23/05/2026 | - Tìm hiểu EC2 Image Builder. <br> - Kết quả: Hiểu cách tạo image máy chủ chuẩn, tích hợp bản vá và giảm lỗi cấu hình khi triển khai. | 23/05/2026 | 23/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 24/05/2026 | - Tìm hiểu VPC Peering và AWS Transit Gateway. <br> - Kết quả: Nắm được cách kết nối nhiều VPC và quản lý mạng tập trung. | 24/05/2026 | 24/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 25/05/2026 | - Tìm hiểu Amazon SQS và SNS. <br> - Kết quả: Biết cách tách rời các thành phần hệ thống và xử lý thông điệp bất đồng bộ. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 26/05/2026 | - Tìm hiểu Amazon EBS Multi-Attach và mô hình HA cho cơ sở dữ liệu. <br> - Kết quả: Hiểu thêm các yêu cầu lưu trữ trong hệ thống cần tính sẵn sàng cao. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 27/05/2026 | - Tìm hiểu EC2 Resource Optimization và Service Quotas. <br> - Kết quả: Biết cách đánh giá kích thước instance và theo dõi hạn mức tài nguyên. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 28/05/2026 | - Tìm hiểu Savings Plans, Reserved Instances, AWS Glue, Athena và phân quyền Billing Console. <br> - Kết quả: Nắm được các hướng tiết kiệm, phân tích chi phí và quản lý quyền truy cập billing. | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 6:

* Nắm được vai trò của AWS Backup trong việc sao lưu dữ liệu tập trung cho nhiều tài nguyên, hỗ trợ phục hồi hệ thống khi có sự cố hoặc mất dữ liệu.
* Hiểu cách EBS Data Lifecycle Manager giúp tự động hóa snapshot, giảm thao tác thủ công và đảm bảo dữ liệu được sao lưu theo lịch định kỳ.
* Biết vai trò của EC2 Image Builder trong việc tạo image máy chủ chuẩn, hỗ trợ cập nhật bản vá, cài đặt cấu hình cần thiết và triển khai môi trường nhất quán.
* Nắm được cách VPC Peering kết nối hai VPC và cách Transit Gateway giúp đơn giản hóa kiến trúc mạng khi cần kết nối nhiều VPC hoặc hệ thống on-premises.
* Hiểu cách SQS và SNS hỗ trợ xử lý bất đồng bộ, giảm phụ thuộc trực tiếp giữa các service và giúp hệ thống ổn định hơn khi lưu lượng tăng.
* Biết thêm về EBS Multi-Attach và các tình huống yêu cầu chia sẻ lưu trữ cho nhiều EC2 instance trong kiến trúc cần tính sẵn sàng cao.
* Nắm được cách EC2 Resource Optimization hỗ trợ đánh giá tài nguyên sử dụng thực tế, từ đó điều chỉnh kích thước instance phù hợp để tránh lãng phí.
* Hiểu vai trò của Service Quotas trong việc kiểm tra hạn mức tài nguyên và chủ động yêu cầu tăng hạn mức trước khi triển khai hệ thống lớn.
* Nắm được các hướng tối ưu chi phí như Savings Plans, Reserved Instances, phân tích chi phí bằng Glue/Athena và kiểm soát quyền truy cập Billing Console.


