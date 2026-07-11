---
title: "Worklog Tuần 1"
date: 2026-04-24
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 1:

* **Chủ đề:** Khởi động Đám mây và nền tảng mạng, máy chủ.
* Tuần này tập trung vào các khái niệm cốt lõi, cách quản lý tài khoản và thiết lập hạ tầng mạng, máy chủ cơ bản.
* Làm quen với điện toán đám mây, hệ sinh thái AWS và các nhóm dịch vụ nền tảng.
* Thiết lập môi trường thực hành ban đầu, bao gồm tài khoản AWS, Console, Budgets và AWS CLI.
* Nắm các kiến thức cơ bản về IAM, VPC, EC2, IAM Role, Cloud9 và thao tác dòng lệnh.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 17/04/2026 | - Khám phá tổng quan dịch vụ AWS, phân loại các nhóm dịch vụ chính như Compute, Storage, Networking, Database, Security và Monitoring. <br> - Kết quả: Hình thành được cái nhìn tổng thể về vai trò của AWS trong việc cung cấp tài nguyên Cloud cho hệ thống ứng dụng. | 17/04/2026 | 17/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 18/04/2026 | - Tạo mới tài khoản AWS, kiểm tra thông tin đăng nhập và làm quen với AWS Management Console. <br> - Kết quả: Chuẩn bị được môi trường thực hành ban đầu và biết cách tìm kiếm, truy cập các dịch vụ AWS trên giao diện web. | 18/04/2026 | 18/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 19/04/2026 | - Tìm hiểu AWS Budgets và cách thiết lập cảnh báo chi phí. <br> - Kết quả: Nắm được cách tạo ngân sách, đặt ngưỡng cảnh báo và theo dõi chi phí để hạn chế phát sinh ngoài dự kiến. | 19/04/2026 | 19/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 20/04/2026 | - Tìm hiểu AWS Support, các hình thức hỗ trợ kỹ thuật và cách tra cứu tài liệu khi gặp sự cố. <br> - Kết quả: Biết cách phân biệt nhu cầu hỗ trợ cơ bản, tra cứu tài liệu và xác định tình huống cần tạo support case. | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 21/04/2026 | - Tìm hiểu IAM với User, Group, Policy và Role. <br> - Kết quả: Hiểu được nguyên tắc phân quyền tối thiểu và cách IAM kiểm soát quyền truy cập đến tài nguyên AWS. | 21/04/2026 | 21/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 22/04/2026 | - Tìm hiểu Amazon VPC và Amazon EC2, bao gồm subnet, route table, internet gateway, security group, AMI, instance type, key pair và EBS. <br> - Kết quả: Nắm được cách thiết lập mạng cơ bản và cách tạo máy chủ ảo phục vụ triển khai ứng dụng. | 22/04/2026 | 22/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 23/04/2026 | - Tìm hiểu IAM Roles for EC2, AWS Cloud9 và AWS CLI. <br> - Kết quả: Biết cách cấp quyền an toàn cho EC2, sử dụng môi trường phát triển trên Cloud và thao tác AWS bằng dòng lệnh. | 23/04/2026 | 23/04/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 1:

* Hình thành được bức tranh tổng quan về AWS, bao gồm vai trò của Cloud trong việc cung cấp tài nguyên điện toán, lưu trữ, mạng, cơ sở dữ liệu, bảo mật và giám sát cho hệ thống ứng dụng.
* Hoàn tất bước chuẩn bị môi trường thực hành ban đầu: tài khoản AWS được tạo, AWS Management Console được làm quen và AWS Budgets được cấu hình để theo dõi chi phí sử dụng tài nguyên.
* Nắm được cách quản lý ngân sách trên AWS, hiểu được ý nghĩa của ngưỡng cảnh báo, chi phí dự kiến và tầm quan trọng của việc kiểm soát tài chính khi thực hành trên môi trường Cloud.
* Hiểu nền tảng phân quyền truy cập bằng IAM, bao gồm vai trò của user, group, policy và role trong việc kiểm soát quyền sử dụng tài nguyên AWS theo nguyên tắc tối thiểu quyền.
* Hiểu được cấu trúc mạng cơ bản trên AWS thông qua VPC, subnet, route table, internet gateway và security group, từ đó hình dung được cách một hệ thống được cô lập và kiểm soát lưu lượng mạng.
* Nắm được cách EC2 hoạt động, bao gồm lựa chọn AMI, instance type, key pair, EBS volume và cấu hình bảo mật khi tạo máy chủ ảo phục vụ triển khai ứng dụng.
* Biết cách cấp quyền an toàn cho EC2 bằng IAM Role, tránh lưu Access Key và Secret Key trực tiếp trong máy chủ hoặc mã nguồn, góp phần tăng tính bảo mật cho hệ thống.
* Sử dụng được AWS CLI cho một số thao tác cơ bản như kiểm tra cấu hình, xem thông tin tài khoản, liệt kê region, truy vấn thông tin EC2 và hỗ trợ quản lý tài nguyên song song với giao diện Console.
* Có nền tảng ban đầu để tiếp tục học các dịch vụ nâng cao hơn trong những tuần sau, đặc biệt là networking, storage, security, automation và triển khai ứng dụng trên AWS.


