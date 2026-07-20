---
title: "Worklog Tuần 7"
date: 2026-06-05
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Tuần 7: Application Modernization, Microservices, Serverless, Event-driven Architecture và Serverless Book Store

### Mục tiêu tuần 7:

* Tìm hiểu hiện đại hóa ứng dụng trên AWS và hướng chuyển đổi từ Monolith sang Microservices.
* Nắm được kiến trúc Serverless, event-driven architecture và cách thiết kế hệ thống ít phụ thuộc máy chủ.
* Thực hành dự án Serverless Book Store với Lambda, S3, DynamoDB và frontend kết nối API.
* Làm quen với Cognito, SQS, SNS, AppSync, AWS SAM và CI/CD cho ứng dụng Serverless.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu Application Modernization trên AWS, lý do cần hiện đại hóa ứng dụng và các hướng cải tiến hệ thống cũ. | 01/06/2026 | 01/06/2026 | https://aws.amazon.com/application-modernization/ |
| Thứ 3 | Tìm hiểu quá trình chuyển đổi từ Monolith sang Microservices, cách tách service theo chức năng nghiệp vụ và quản lý dữ liệu sau khi tách service. | 02/06/2026 | 02/06/2026 | https://aws.amazon.com/microservices/ |
| Thứ 4 | Tìm hiểu Serverless trong DevAx Series, event-driven architecture, xác thực ứng dụng đơn trang và tích hợp dịch vụ AI trên AWS. | 03/06/2026 | 03/06/2026 | https://aws.amazon.com/serverless/ |
| Thứ 5 | Tìm hiểu DynamoDB nâng cao, thiết kế bảng, truy vấn dữ liệu và các lưu ý khi dùng DynamoDB cho ứng dụng Serverless. | 04/06/2026 | 04/06/2026 | https://docs.aws.amazon.com/dynamodb/ |
| Thứ 6 | Thực hành dự án Serverless Book Store, xây dựng backend Serverless với Lambda, S3 và DynamoDB. | 05/06/2026 | 05/06/2026 | https://docs.aws.amazon.com/lambda/ |
| Thứ 7 | Phát triển frontend kết nối với API Serverless, tìm hiểu AWS SAM để đóng gói và tự động hóa triển khai ứng dụng. | 06/06/2026 | 06/06/2026 | https://docs.aws.amazon.com/serverless-application-model/ |
| Chủ nhật | Tìm hiểu Cognito, SQS, SNS, CI/CD Serverless và AWS AppSync để hoàn thiện các thành phần xác thực, xử lý bất đồng bộ và GraphQL API. | 07/06/2026 | 07/06/2026 | https://docs.aws.amazon.com/appsync/ |

### Kết quả đạt được tuần 7:

* Hiểu được hiện đại hóa ứng dụng là quá trình cải tiến hệ thống cũ để phù hợp hơn với Cloud, dễ mở rộng và dễ vận hành hơn.
* Nắm được sự khác nhau giữa kiến trúc Monolith và Microservices, cũng như lợi ích của việc tách hệ thống theo chức năng nghiệp vụ.
* Hiểu được khi chuyển từ Monolith sang Microservices cần quan tâm đến giao tiếp giữa service, phân tách dữ liệu, triển khai độc lập và giám sát hệ thống.
* Nắm được kiến trúc Serverless giúp giảm nhu cầu quản lý máy chủ, phù hợp với các workload theo sự kiện hoặc lưu lượng không ổn định.
* Hiểu được event-driven architecture giúp các thành phần giao tiếp thông qua sự kiện, giảm phụ thuộc trực tiếp và tăng khả năng mở rộng.
* Biết cách xác thực ứng dụng đơn trang bằng các dịch vụ quản lý người dùng thay vì tự xây toàn bộ hệ thống đăng nhập.
* Nắm thêm kiến thức về tích hợp dịch vụ AI trên AWS và cách các dịch vụ AI có thể được đưa vào ứng dụng thực tế.
* Hiểu sâu hơn về DynamoDB nâng cao, đặc biệt là cách thiết kế key và truy vấn dữ liệu trong ứng dụng Serverless.
* Thực hành được dự án Serverless Book Store, qua đó nắm được cách kết hợp Lambda, S3 và DynamoDB để xây dựng backend.
* Biết cách frontend kết nối với API Serverless và cách tổ chức các thành phần trong một ứng dụng hoàn chỉnh.
* Nắm được AWS SAM hỗ trợ đóng gói, cấu hình và triển khai ứng dụng Serverless một cách nhất quán.
* Hiểu được Cognito dùng cho xác thực, SQS dùng cho hàng đợi, SNS dùng cho thông báo và AppSync dùng cho GraphQL API.
* Nắm được vai trò của CI/CD trong phát hành ứng dụng Serverless, giúp quá trình cập nhật ứng dụng ổn định hơn.
* Tổng hợp được kiến thức về modernization, microservices và serverless để chuẩn bị cho các bài thực hành hệ thống phức tạp hơn.