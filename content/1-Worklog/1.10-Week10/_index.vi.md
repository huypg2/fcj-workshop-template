---
title: "Worklog Tuần 10"
date: 2026-06-26
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Tuần 10: Thiết lập VPC, Subnet, Security Groups và Amazon RDS PostgreSQL

### Mục tiêu tuần 10:

* Thiết lập lớp mạng VPC, subnet, route table và NAT theo thứ tự triển khai.
* Cấu hình Security Groups để kiểm soát kết nối giữa các thành phần.
* Tạo DB Subnet Group, RDS Instance và khởi tạo database ban đầu.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | - Tạo VPC làm mạng riêng cho hệ thống<br>&emsp; + Chọn dải CIDR phù hợp<br>&emsp; + Tạo VPC mới cho môi trường triển khai<br>&emsp; + Kiểm tra VPC ID, trạng thái và thiết lập DNS cần thiết | 22/06/2026 | 22/06/2026 | https://000003.awsstudygroup.com/ |
| Thứ 3 | - Tạo subnet, route table và NAT theo cấu trúc mạng<br>&emsp; + Tạo các subnet theo Availability Zone<br>&emsp; + Liên kết subnet với route table phù hợp<br>&emsp; + Cấu hình NAT để hỗ trợ luồng truy cập theo yêu cầu triển khai | 23/06/2026 | 23/06/2026 | https://000092.awsstudygroup.com/ |
| Thứ 4 | - Tạo và cấu hình Security Groups<br>&emsp; + Tạo security group cho các lớp tài nguyên cần thiết<br>&emsp; + Cấu hình inbound rule và outbound rule theo đúng luồng truy cập<br>&emsp; + Kiểm tra lại rule trước khi tạo database và compute | 24/06/2026 | 24/06/2026 | https://000003.awsstudygroup.com/ |
| Thứ 5 | - Tạo DB Subnet Group cho RDS<br>&emsp; + Chọn các subnet dùng cho tầng database<br>&emsp; + Tạo DB Subnet Group để RDS có thể triển khai trong VPC<br>&emsp; + Kiểm tra subnet group trước khi tạo RDS instance | 25/06/2026 | 25/06/2026 | https://000005.awsstudygroup.com/ |
| Thứ 6 | - Tạo RDS PostgreSQL và khởi tạo database<br>&emsp; + Tạo RDS instance theo cấu hình đã chuẩn bị<br>&emsp; + Kiểm tra endpoint, port và trạng thái database<br>&emsp; + Khởi tạo database/schema ban đầu phục vụ ứng dụng | 26/06/2026 | 26/06/2026 | https://000005.awsstudygroup.com/ |

### Kết quả đạt được tuần 10:

* Tạo được VPC riêng để đặt các tài nguyên triển khai trong một môi trường mạng độc lập.
* Hiểu được vai trò của CIDR block trong việc quy hoạch địa chỉ IP cho VPC.
* Tạo được các subnet theo Availability Zone để chuẩn bị nền tảng mạng cho các tài nguyên phía sau.
* Cấu hình được route table và liên kết subnet đúng theo luồng mạng triển khai.
* Thiết lập được NAT theo nhóm công việc network của workshop.
* Tạo được các Security Groups cần thiết cho hệ thống.
* Cấu hình được inbound rule và outbound rule theo từng lớp tài nguyên.
* Chuẩn bị được DB Subnet Group để triển khai Amazon RDS trong VPC.
* Tạo được RDS PostgreSQL theo đúng thứ tự sau khi hoàn tất network và security.
* Kiểm tra được endpoint, port và trạng thái hoạt động của RDS.
* Khởi tạo được database/schema ban đầu để ứng dụng có thể sử dụng ở bước triển khai ECS.
* Hoàn thành đúng nhóm công việc VPC Networking, Security Groups và RDS Database; nguồn tham khảo dùng tài liệu trong Cloud Journey/AWS Study Group.