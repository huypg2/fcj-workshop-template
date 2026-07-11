---
title: "Worklog Tuần 2"
date: 2026-05-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 2:

* **Chủ đề:** Lưu trữ, cơ sở dữ liệu và mở rộng quy mô.
* Tuần này tập trung vào các dịch vụ lưu trữ tĩnh, cơ sở dữ liệu, bộ nhớ đệm và cách tự động mở rộng hệ thống.
* Làm quen với Amazon S3, RDS, DynamoDB và ElastiCache.
* Hiểu cách triển khai ứng dụng đơn giản bằng Lightsail và container.
* Nắm cơ chế mở rộng tự động, giám sát hệ thống và quản lý DNS.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 24/04/2026 | - Tìm hiểu Amazon S3 và hosting website tĩnh. <br> - Kết quả: Biết cách tạo bucket, lưu nội dung tĩnh và cấu hình website static phục vụ truy cập cơ bản. | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 25/04/2026 | - Tìm hiểu Amazon RDS cho cơ sở dữ liệu quan hệ. <br> - Kết quả: Nắm được cách chọn database engine, tạo DB instance, cấu hình backup và kết nối ứng dụng. | 25/04/2026 | 25/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 26/04/2026 | - Tìm hiểu Amazon DynamoDB cho dữ liệu NoSQL. <br> - Kết quả: Hiểu mô hình key-value/document, cách dùng partition key và cách DynamoDB hỗ trợ mở rộng. | 26/04/2026 | 26/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 27/04/2026 | - Tìm hiểu Amazon ElastiCache. <br> - Kết quả: Biết vai trò của cache trong việc giảm tải database và tăng tốc độ phản hồi ứng dụng. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 28/04/2026 | - Tìm hiểu Amazon Lightsail và Lightsail Containers. <br> - Kết quả: Nắm được cách triển khai ứng dụng nhỏ hoặc container đơn giản với chi phí dễ dự đoán. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 29/04/2026 | - Tìm hiểu EC2 Auto Scaling và CloudWatch. <br> - Kết quả: Hiểu cách tự động tăng giảm tài nguyên theo tải và cách theo dõi metric, log, alarm. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 30/04/2026 | - Tìm hiểu Amazon Route 53. <br> - Kết quả: Biết cách DNS record và routing policy hỗ trợ định tuyến người dùng đến tài nguyên AWS. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Nắm được vai trò của Amazon S3 trong việc lưu trữ dữ liệu tĩnh, hosting website tĩnh và quản lý dữ liệu đối tượng với độ bền cao.
* Hiểu cách cấu hình bucket, quyền truy cập và các thiết lập cần thiết khi triển khai website tĩnh trên S3, đồng thời nhận biết rủi ro khi cấu hình public access không đúng cách.
* Nắm được cách Amazon RDS hỗ trợ triển khai cơ sở dữ liệu quan hệ được quản lý, bao gồm lựa chọn engine, cấu hình instance, backup, bảo mật và kết nối ứng dụng.
* Hiểu được sự khác nhau giữa cơ sở dữ liệu quan hệ và NoSQL thông qua DynamoDB, đặc biệt là cách thiết kế khóa chính, lưu trữ dữ liệu dạng key-value và mở rộng theo nhu cầu truy cập.
* Biết được vai trò của ElastiCache trong việc tăng hiệu năng ứng dụng, giảm truy vấn lặp lại vào database và cải thiện tốc độ phản hồi của hệ thống.
* Làm quen với Lightsail và Lightsail Containers như một phương án triển khai ứng dụng đơn giản, phù hợp cho website nhỏ, môi trường thử nghiệm hoặc dự án cần quản lý chi phí rõ ràng.
* Nắm được nguyên lý EC2 Auto Scaling, biết cách hệ thống tự động tăng hoặc giảm số lượng máy chủ dựa trên tải để cân bằng giữa hiệu năng và chi phí.
* Hiểu cách CloudWatch hỗ trợ theo dõi metric, log và alarm, từ đó có khả năng phát hiện sớm tình trạng bất thường trong quá trình vận hành.
* Nắm được vai trò của Route 53 trong quản lý DNS, domain và định tuyến truy cập, tạo nền tảng để triển khai ứng dụng có địa chỉ truy cập rõ ràng hơn.


