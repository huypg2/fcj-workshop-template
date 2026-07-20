---
title: "Worklog Tuần 5"
date: 2026-05-22
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Tuần 5: Bảo mật Cloud, sao lưu dữ liệu, độ tin cậy, messaging, quota và tối ưu chi phí

### Mục tiêu tuần 5:

* Tìm hiểu các dịch vụ bảo mật và kiểm soát truy cập nâng cao trên AWS.
* Nắm được cách mã hóa dữ liệu, quản lý secret, phát hiện dữ liệu nhạy cảm và giám sát rủi ro.
* Tìm hiểu các dịch vụ hỗ trợ backup, kết nối mạng, messaging và tăng độ tin cậy hệ thống.
* Làm quen với Service Quotas, Savings Plans, Reserved Instances và các phương pháp tối ưu chi phí.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu AWS Single Sign-On, IAM Permission Boundaries, IAM Policies và IAM Conditions để quản lý truy cập nâng cao. | 18/05/2026 | 18/05/2026 | https://000012.awsstudygroup.com/vi/<br>https://000030.awsstudygroup.com/vi/<br>https://000044.awsstudygroup.com/vi/ |
| Thứ 3 | Tìm hiểu AWS Security Hub, GuardDuty, VPC Endpoints và các phương pháp bảo mật tốt nhất cho Amazon S3. | 19/05/2026 | 19/05/2026 | https://000018.awsstudygroup.com/vi/<br>https://000098.awsstudygroup.com/vi/<br>https://000111.awsstudygroup.com/vi/<br>https://000069.awsstudygroup.com/vi/ |
| Thứ 4 | Tìm hiểu AWS WAF, AWS KMS, Amazon Macie và AWS Secrets Manager trong bảo vệ ứng dụng, mã hóa dữ liệu và quản lý thông tin xác thực. | 20/05/2026 | 20/05/2026 | https://000026.awsstudygroup.com/vi/<br>https://000033.awsstudygroup.com/vi/<br>https://000090.awsstudygroup.com/vi/<br>https://000096.awsstudygroup.com/vi/ |
| Thứ 5 | Tìm hiểu Amazon Cognito, cơ chế xác thực người dùng và cách quản lý đăng nhập cho ứng dụng web hoặc mobile. | 21/05/2026 | 21/05/2026 | https://000141.awsstudygroup.com/vi/ |
| Thứ 6 | Tìm hiểu AWS Backup, EBS Data Lifecycle Manager và EC2 Image Builder để chuẩn bị phương án sao lưu và chuẩn hóa image máy chủ. | 22/05/2026 | 22/05/2026 | https://000013.awsstudygroup.com/vi/<br>https://000088.awsstudygroup.com/vi/<br>https://000099.awsstudygroup.com/vi/ |
| Thứ 7 | Tìm hiểu VPC Peering, AWS Transit Gateway, Amazon SQS và Amazon SNS để tăng khả năng kết nối mạng và xử lý bất đồng bộ. | 23/05/2026 | 23/05/2026 | https://000019.awsstudygroup.com/vi/<br>https://000020.awsstudygroup.com/vi/<br>https://000077.awsstudygroup.com/vi/ |
| Chủ nhật | Tìm hiểu Service Quotas, Savings Plans, Reserved Instances và các nguyên tắc tối ưu chi phí khi vận hành tài nguyên AWS. | 24/05/2026 | 24/05/2026 | https://000063.awsstudygroup.com/vi/<br>https://000042.awsstudygroup.com/vi/<br>https://000034.awsstudygroup.com/vi/ |

### Kết quả đạt được tuần 5:

* Hiểu được bảo mật trên AWS không chỉ nằm ở mật khẩu tài khoản mà còn liên quan đến IAM, network, encryption, logging và quản lý dữ liệu nhạy cảm.
* Nắm được AWS Single Sign-On hỗ trợ quản lý đăng nhập tập trung, phù hợp với môi trường có nhiều người dùng hoặc nhiều tài khoản.
* Hiểu được Permission Boundaries, IAM Policies và IAM Conditions giúp giới hạn quyền chi tiết hơn trong các tình huống thực tế.
* Biết Security Hub có thể tổng hợp trạng thái bảo mật từ nhiều dịch vụ, hỗ trợ đánh giá rủi ro tập trung hơn.
* Nắm được GuardDuty giúp phát hiện hành vi bất thường, hỗ trợ cảnh báo khi có dấu hiệu rủi ro trong tài khoản hoặc workload.
* Hiểu được VPC Endpoints giúp truy cập một số dịch vụ AWS qua mạng riêng, giảm phụ thuộc vào Internet public.
* Nắm được các phương pháp bảo mật S3 như kiểm soát quyền public, bucket policy, encryption và nguyên tắc không mở dữ liệu nhạy cảm ra ngoài.
* Biết AWS WAF giúp bảo vệ ứng dụng web trước một số kiểu tấn công phổ biến như rule-based filtering hoặc chặn request bất thường.
* Hiểu được KMS hỗ trợ quản lý khóa mã hóa, Secrets Manager hỗ trợ quản lý thông tin xác thực và Macie hỗ trợ phát hiện dữ liệu nhạy cảm.
* Hiểu được Cognito có thể dùng để xác thực người dùng cho ứng dụng web/mobile mà không phải tự xây toàn bộ hệ thống đăng nhập.
* Nắm được AWS Backup, EBS Lifecycle Manager và EC2 Image Builder giúp chuẩn hóa việc backup, vòng đời dữ liệu và image hệ thống.
* Hiểu được VPC Peering và Transit Gateway hỗ trợ kết nối nhiều mạng VPC hoặc hệ thống với nhau trong kiến trúc lớn.
* Nắm được SQS và SNS hỗ trợ xử lý bất đồng bộ, giúp tách rời các thành phần trong hệ thống và tăng độ tin cậy khi tải tăng.
* Biết Service Quotas giúp theo dõi giới hạn dịch vụ để tránh lỗi khi hệ thống mở rộng.
* Hiểu được Savings Plans và Reserved Instances là các hướng tối ưu chi phí quan trọng khi workload chạy ổn định trong thời gian dài.
* Tổng hợp được kiến thức về bảo mật, độ tin cậy, backup, messaging và chi phí để áp dụng vào thiết kế hệ thống thực tế sau này.



