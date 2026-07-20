---
title: "Worklog Tuần 2"
date: 2026-05-03
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Tuần 2: Lưu trữ, cơ sở dữ liệu, cache, DNS, giám sát và mở rộng hệ thống

### Mục tiêu tuần 2:

* Tìm hiểu các dịch vụ lưu trữ và cơ sở dữ liệu phổ biến trên AWS.
* Nắm được vai trò của cache, DNS, monitoring và auto scaling trong hệ thống Cloud.
* Làm quen với các dịch vụ hỗ trợ triển khai ứng dụng nhỏ và hệ thống có khả năng mở rộng.
* Kết nối kiến thức giữa lưu trữ, database, cache, giám sát và mở rộng tài nguyên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu Amazon S3, bucket, object, storage class, phân quyền truy cập và cách lưu trữ dữ liệu tĩnh trên AWS. | 27/04/2026 | 27/04/2026 | https://000057.awsstudygroup.com/vi/ |
| Thứ 3 | Thực hành hosting website tĩnh bằng Amazon S3, kiểm tra cấu hình bucket policy, static website endpoint và truy cập nội dung qua trình duyệt. | 28/04/2026 | 28/04/2026 | https://000057.awsstudygroup.com/vi/ |
| Thứ 4 | Tìm hiểu Amazon RDS, DB instance, engine, backup, Multi-AZ, connection endpoint và vai trò của cơ sở dữ liệu quan hệ được quản lý. | 29/04/2026 | 29/04/2026 | https://000005.awsstudygroup.com/vi/ |
| Thứ 5 | Tìm hiểu Amazon DynamoDB, partition key, sort key, bảng NoSQL và so sánh cơ bản giữa database quan hệ với NoSQL. | 30/04/2026 | 30/04/2026 | https://000060.awsstudygroup.com/vi/ |
| Thứ 6 | Tìm hiểu Amazon ElastiCache, Redis, Memcached và vai trò của cache trong giảm tải truy vấn database, tăng tốc độ phản hồi hệ thống. | 01/05/2026 | 01/05/2026 | https://000061.awsstudygroup.com/vi/ |
| Thứ 7 | Tìm hiểu Amazon Route 53, DNS record, hosted zone, đồng thời tìm hiểu Amazon CloudWatch để theo dõi metric, log và alarm. | 02/05/2026 | 02/05/2026 | https://000010.awsstudygroup.com/vi/<br>https://000008.awsstudygroup.com/vi/ |
| Chủ nhật | Tìm hiểu EC2 Auto Scaling, Lightsail và Lightsail Containers để nắm được cách triển khai ứng dụng nhỏ và tự mở rộng tài nguyên khi tải thay đổi. | 03/05/2026 | 03/05/2026 | https://000006.awsstudygroup.com/vi/<br>https://000045.awsstudygroup.com/vi/<br>https://000046.awsstudygroup.com/vi/ |

### Kết quả đạt được tuần 2:

* Hiểu được Amazon S3 là dịch vụ lưu trữ object có khả năng mở rộng cao và phù hợp cho dữ liệu tĩnh, backup, log hoặc tài nguyên website.
* Thực hành được cách hosting website tĩnh bằng S3, từ đó hiểu rõ hơn cách bucket policy và static website endpoint ảnh hưởng đến khả năng truy cập nội dung.
* Nắm được vai trò của Amazon RDS trong việc vận hành cơ sở dữ liệu quan hệ mà không cần tự quản lý toàn bộ hạ tầng database.
* Hiểu được các khái niệm quan trọng trong RDS như DB instance, endpoint, backup và Multi-AZ, làm cơ sở cho việc sử dụng RDS PostgreSQL trong đề tài sau này.
* Phân biệt được dữ liệu phù hợp với database quan hệ và dữ liệu phù hợp với NoSQL như DynamoDB.
* Nắm được vai trò của DynamoDB trong các hệ thống cần mở rộng nhanh, độ trễ thấp và không muốn quản lý máy chủ database.
* Hiểu được ElastiCache/Redis giúp giảm tải database, tăng tốc truy vấn và có thể dùng cho các chức năng như cache, distributed lock hoặc rate limiting.
* Nắm được Route 53 hỗ trợ định tuyến DNS và giúp người dùng truy cập hệ thống thông qua tên miền thay vì địa chỉ kỹ thuật phức tạp.
* Hiểu được CloudWatch đóng vai trò quan trọng trong giám sát hệ thống thông qua log, metric và alarm.
* Nắm được ý nghĩa của Auto Scaling trong việc tự động tăng hoặc giảm tài nguyên theo tải, giúp hệ thống linh hoạt và tối ưu chi phí hơn.
* Biết thêm Lightsail và Lightsail Containers như lựa chọn đơn giản hơn cho ứng dụng nhỏ hoặc môi trường thử nghiệm.
* Liên kết được các thành phần S3, RDS, DynamoDB, Redis, Route 53, CloudWatch và Auto Scaling trong một kiến trúc ứng dụng có khả năng mở rộng.


