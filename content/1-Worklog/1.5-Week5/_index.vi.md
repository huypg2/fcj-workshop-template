---
title: "Worklog Tuần 5"
date: 2026-05-22
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 5:

* **Chủ đề:** Bảo mật đám mây chuyên sâu và quản lý truy cập.
* Tuần này tập trung vào các cơ chế phòng thủ, bảo vệ dữ liệu, phân quyền và giám sát an ninh trên AWS.
* Tìm hiểu quản lý danh tính, phân quyền và điều kiện truy cập nâng cao.
* Nắm các dịch vụ giám sát, phát hiện rủi ro và bảo vệ ứng dụng web.
* Hiểu cách mã hóa dữ liệu, quản lý secret và xác thực người dùng.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 15/05/2026 | - Tìm hiểu AWS Single Sign-On. <br> - Kết quả: Nắm được cách quản lý đăng nhập tập trung cho nhiều tài khoản và ứng dụng. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 16/05/2026 | - Tìm hiểu IAM Permission Boundaries, Policies và Conditions. <br> - Kết quả: Hiểu cách giới hạn quyền tối đa và đặt điều kiện truy cập chi tiết hơn. | 16/05/2026 | 16/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 17/05/2026 | - Tìm hiểu AWS Security Hub. <br> - Kết quả: Biết cách tổng hợp cảnh báo và đánh giá trạng thái bảo mật của hệ thống. | 17/05/2026 | 17/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 18/05/2026 | - Tìm hiểu VPC Endpoints và bảo mật S3. <br> - Kết quả: Nắm được cách truy cập S3 riêng tư và giảm rủi ro public dữ liệu không cần thiết. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 19/05/2026 | - Tìm hiểu AWS WAF. <br> - Kết quả: Hiểu cách bảo vệ ứng dụng web khỏi SQL Injection, XSS và bot traffic phổ biến. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 20/05/2026 | - Tìm hiểu AWS KMS, Amazon Macie và Secrets Manager. <br> - Kết quả: Biết cách mã hóa dữ liệu, phát hiện dữ liệu nhạy cảm và quản lý secret an toàn. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 21/05/2026 | - Tìm hiểu AWS Firewall Manager, GuardDuty và Amazon Cognito. <br> - Kết quả: Nắm được cách quản trị bảo mật tập trung, phát hiện mối đe dọa và xác thực người dùng. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

* Nắm được bức tranh tổng quan về bảo mật trên AWS, bao gồm quản lý danh tính, phân quyền, mã hóa dữ liệu, bảo vệ ứng dụng và giám sát nguy cơ an ninh.
* Hiểu vai trò của AWS Single Sign-On trong việc quản lý đăng nhập tập trung, giúp đơn giản hóa truy cập khi hệ thống có nhiều tài khoản hoặc nhiều nhóm người dùng.
* Nắm được cách IAM Permission Boundaries, Policies và Conditions hỗ trợ kiểm soát quyền truy cập chi tiết hơn, hạn chế tình trạng cấp quyền quá rộng cho user hoặc role.
* Hiểu vai trò của Security Hub trong việc tổng hợp phát hiện bảo mật từ nhiều dịch vụ, hỗ trợ đánh giá mức độ tuân thủ và phát hiện cấu hình rủi ro.
* Biết cách VPC Endpoints hỗ trợ truy cập S3 qua mạng riêng, giúp giảm phụ thuộc vào Internet và tăng tính bảo mật cho dữ liệu lưu trữ.
* Nắm được các thực hành bảo mật tốt cho Amazon S3 như chặn public access, cấu hình bucket policy, mã hóa dữ liệu và theo dõi hoạt động truy cập.
* Hiểu cách AWS WAF bảo vệ tầng ứng dụng trước các kiểu tấn công phổ biến như SQL Injection, Cross-Site Scripting và bot request.
* Biết vai trò của KMS, Macie và Secrets Manager trong việc bảo vệ dữ liệu, quản lý khóa mã hóa, phát hiện dữ liệu nhạy cảm và lưu trữ thông tin xác thực an toàn.
* Nắm được cách GuardDuty hỗ trợ phát hiện hành vi bất thường và cách Cognito hỗ trợ xác thực người dùng cho ứng dụng web hoặc mobile.



