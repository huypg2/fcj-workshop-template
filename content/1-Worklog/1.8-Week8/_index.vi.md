---
title: "Worklog Tuần 8"
date: 2026-06-12
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Tuần 8: Serverless Document Management, API Gateway, CloudFront, X-Ray, CloudWatch, Grafana, Web App và HA

### Mục tiêu tuần 8:

* Thực hành xây dựng hệ thống quản lý tài liệu theo hướng Serverless.
* Tích hợp frontend với API Gateway, Lambda, DynamoDB, Amplify, CloudFront và AWS SAM.
* Tìm hiểu giám sát nâng cao bằng X-Ray, CloudWatch và Grafana.
* Tổng hợp kiến thức về Serverless Web App, Elastic Beanstalk, WordPress và các mô hình HA trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu Serverless Document Management System, xây dựng chức năng CRUD Serverless bằng Lambda và DynamoDB. | 08/06/2026 | 08/06/2026 | https://docs.aws.amazon.com/lambda/ |
| Thứ 3 | Tìm hiểu AWS Amplify cho lưu trữ, xác thực người dùng và tích hợp frontend với API Gateway. | 09/06/2026 | 09/06/2026 | https://docs.aws.amazon.com/amplify/ |
| Thứ 4 | Triển khai hệ thống quản lý tài liệu bằng AWS SAM, thiết lập CloudFront để phân phối nội dung và tối ưu truy cập. | 10/06/2026 | 10/06/2026 | https://docs.aws.amazon.com/serverless-application-model/ |
| Thứ 5 | Bổ sung chức năng tìm kiếm, tìm hiểu DevOps cho hệ thống quản lý tài liệu và cách tổ chức pipeline triển khai. | 11/06/2026 | 11/06/2026 | https://docs.aws.amazon.com/cloudfront/ |
| Thứ 6 | Tìm hiểu AWS X-Ray, CloudWatch, Grafana và thực hành workshop CloudWatch nâng cao để theo dõi log, metric, alarm và tracing. | 12/06/2026 | 12/06/2026 | https://docs.aws.amazon.com/xray/ |
| Thứ 7 | Tổng hợp kiến thức về Serverless Web App, Serverless API, ứng dụng chat Serverless và triển khai ứng dụng Node.js bằng Elastic Beanstalk. | 13/06/2026 | 13/06/2026 | https://docs.aws.amazon.com/elasticbeanstalk/ |
| Chủ nhật | Tìm hiểu CI/CD với Elastic Beanstalk, CDK Pipelines, WordPress trên AWS, Web App High Availability, Windows Server HA và SQL Server HA. | 14/06/2026 | 14/06/2026 | https://docs.aws.amazon.com/ |

### Kết quả đạt được tuần 8:

* Hiểu được cách xây dựng hệ thống quản lý tài liệu theo mô hình Serverless, trong đó các chức năng backend được xử lý bằng Lambda và dữ liệu được lưu trong DynamoDB.
* Nắm được cách thiết kế các chức năng CRUD cho tài liệu, bao gồm tạo, đọc, cập nhật và xóa dữ liệu thông qua API.
* Hiểu được AWS Amplify có thể hỗ trợ frontend, xác thực người dùng và tích hợp với các dịch vụ AWS khác.
* Biết cách API Gateway đóng vai trò làm lớp tiếp nhận request từ frontend và chuyển tiếp đến các Lambda function phía sau.
* Nắm được AWS SAM giúp đóng gói, cấu hình và triển khai ứng dụng Serverless theo cách có tổ chức hơn.
* Hiểu được CloudFront có thể cải thiện tốc độ truy cập nội dung và hỗ trợ phân phối frontend hoặc tài nguyên tĩnh hiệu quả hơn.
* Biết cách bổ sung chức năng tìm kiếm vào hệ thống quản lý tài liệu và hiểu được vai trò của tính năng tìm kiếm trong ứng dụng thực tế.
* Nắm được cách DevOps hỗ trợ hệ thống quản lý tài liệu thông qua quy trình build, test và deploy có kiểm soát.
* Hiểu được AWS X-Ray giúp tracing request đi qua nhiều thành phần, hỗ trợ tìm điểm nghẽn hoặc lỗi trong hệ thống phân tán.
* Hiểu được CloudWatch cung cấp log, metric và alarm, giúp theo dõi trạng thái hoạt động của ứng dụng sau khi triển khai.
* Biết Grafana có thể trực quan hóa dữ liệu giám sát, giúp việc quan sát hệ thống dễ hiểu hơn so với chỉ xem log thô.
* Thực hành được kiến thức monitoring nâng cao thông qua CloudWatch workshop và hiểu rõ hơn cách đọc metric khi hệ thống hoạt động.
* Tổng hợp được kiến thức về Serverless Web App, Serverless API và ứng dụng chat Serverless.
* Biết thêm cách Elastic Beanstalk hỗ trợ triển khai ứng dụng Node.js với mức độ quản lý đơn giản hơn so với tự cấu hình toàn bộ hạ tầng.
* Hiểu được CI/CD với Elastic Beanstalk và CDK Pipelines giúp quá trình triển khai ứng dụng tự động và nhất quán hơn.
* Nắm thêm kiến thức về WordPress trên AWS và các mô hình triển khai web app có tính sẵn sàng cao.
* Hiểu được Windows Server HA và SQL Server HA là các hướng triển khai quan trọng đối với workload doanh nghiệp.
* Tổng hợp đầy đủ nội dung của giai đoạn học AWS nền tảng, serverless, devops, monitoring và high availability để chuyển sang giai đoạn triển khai đề tài thực tế.