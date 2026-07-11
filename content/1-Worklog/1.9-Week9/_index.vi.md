---
title: "Worklog Tuần 9"
date: 2026-06-19
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 9:

* **Chủ đề:** Thực hành Serverless với dự án Book Store.
* Tuần này áp dụng kiến trúc Serverless vào dự án Book Store từ frontend, backend đến xác thực và giám sát.
* Xây dựng backend Serverless với Lambda, S3 và DynamoDB.
* Phát triển frontend kết nối API Serverless.
* Nắm cách triển khai bằng AWS SAM, xác thực Cognito, xử lý sự kiện và GraphQL.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 12/06/2026 | - Tìm hiểu tổng quan Serverless - Book Store Series. <br> - Kết quả: Hình dung được kiến trúc tổng thể của ứng dụng Book Store. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 13/06/2026 | - Xây dựng backend Serverless với Lambda, S3 và DynamoDB. <br> - Kết quả: Nắm được cách xử lý logic, lưu trữ file và lưu dữ liệu ứng dụng. | 13/06/2026 | 13/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 14/06/2026 | - Phát triển frontend cho API Serverless. <br> - Kết quả: Biết cách frontend gửi request đến API và hiển thị dữ liệu trả về. | 14/06/2026 | 14/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 15/06/2026 | - Tìm hiểu AWS SAM để tự động hóa triển khai. <br> - Kết quả: Biết cách định nghĩa, build và deploy tài nguyên Serverless bằng template. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 16/06/2026 | - Tìm hiểu Amazon Cognito, tên miền tùy chỉnh và SSL. <br> - Kết quả: Nắm được xác thực người dùng và cấu hình truy cập an toàn qua HTTPS. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 17/06/2026 | - Tìm hiểu SQS, SNS và CI/CD cho ứng dụng Serverless. <br> - Kết quả: Biết cách xử lý sự kiện bất đồng bộ và tự động hóa triển khai. | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 18/06/2026 | - Tìm hiểu giám sát Serverless và AWS AppSync. <br> - Kết quả: Nắm được cách theo dõi Lambda/API và xây dựng API GraphQL linh hoạt. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 9:

* Nắm được kiến trúc tổng thể của một ứng dụng Book Store theo mô hình Serverless, bao gồm frontend, API, xử lý nghiệp vụ, lưu trữ dữ liệu và xác thực người dùng.
* Hiểu cách Lambda đảm nhận logic backend, DynamoDB lưu trữ dữ liệu ứng dụng và S3 lưu trữ file hoặc nội dung tĩnh trong hệ thống.
* Biết cách frontend giao tiếp với API Serverless, gửi request, nhận response và hiển thị dữ liệu cho người dùng cuối.
* Nắm được vai trò của AWS SAM trong việc mô tả, build và deploy tài nguyên Serverless, giúp quá trình triển khai nhất quán hơn so với thao tác thủ công.
* Hiểu cách Amazon Cognito hỗ trợ đăng ký, đăng nhập, xác thực người dùng và bảo vệ các API yêu cầu quyền truy cập.
* Biết cách cấu hình tên miền tùy chỉnh và SSL để ứng dụng có địa chỉ truy cập chuyên nghiệp hơn và đảm bảo kết nối an toàn bằng HTTPS.
* Nắm được cách SQS và SNS hỗ trợ xử lý sự kiện bất đồng bộ, giúp tách rời các thành phần và cải thiện độ ổn định của ứng dụng.
* Hiểu vai trò của CI/CD trong việc tự động hóa cập nhật ứng dụng Serverless, giảm lỗi khi deploy và hỗ trợ phát hành nhanh hơn.
* Biết cách dùng CloudWatch để theo dõi log, metric, lỗi thực thi Lambda và nắm được cách AppSync hỗ trợ xây dựng API GraphQL cho truy vấn dữ liệu linh hoạt.