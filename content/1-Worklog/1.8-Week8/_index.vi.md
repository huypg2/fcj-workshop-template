---
title: "Worklog Tuần 8"
date: 2026-06-12
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 8:

* **Chủ đề:** Hiện đại hóa ứng dụng và chuyển đổi Microservices.
* Tuần này tập trung vào hiện đại hóa hệ thống cũ, chuyển đổi microservices và kiến trúc hướng sự kiện.
* Nắm các hướng hiện đại hóa ứng dụng trên AWS.
* Hiểu quá trình chuyển đổi từ Monolith sang Microservices.
* Làm quen với Serverless, event-driven architecture, xác thực SPA, AI Services và DynamoDB nâng cao.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 05/06/2026 | - Tìm hiểu hiện đại hóa ứng dụng trên AWS. <br> - Kết quả: Nắm được các hướng nâng cấp hệ thống cũ để phù hợp hơn với môi trường Cloud. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 06/06/2026 | - Tìm hiểu Serverless - DevAx Series. <br> - Kết quả: Hiểu cách xây dựng ứng dụng không cần quản lý máy chủ trực tiếp. | 06/06/2026 | 06/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 07/06/2026 | - Tìm hiểu di chuyển từ Monolith sang Microservices. <br> - Kết quả: Biết lý do cần tách ứng dụng lớn thành nhiều service nhỏ theo chức năng. | 07/06/2026 | 07/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 08/06/2026 | - Tìm hiểu xây dựng Microservices và CI/CD cho phát hành ứng dụng. <br> - Kết quả: Nắm được cách service phát triển độc lập và triển khai tự động. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 09/06/2026 | - Tìm hiểu tái cấu trúc dữ liệu và quy trình. <br> - Kết quả: Hiểu rằng chuyển đổi kiến trúc cần điều chỉnh cả dữ liệu, workflow và giao tiếp giữa service. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 10/06/2026 | - Tìm hiểu kiến trúc hướng sự kiện và xác thực ứng dụng đơn trang. <br> - Kết quả: Nắm được giao tiếp bất đồng bộ qua event và cách quản lý đăng nhập cho SPA. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 11/06/2026 | - Tìm hiểu AI Services trên AWS và DynamoDB nâng cao. <br> - Kết quả: Biết cách mở rộng chức năng ứng dụng bằng AI và tối ưu thiết kế dữ liệu NoSQL. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 8:

* Nắm được các hướng hiện đại hóa ứng dụng trên AWS, bao gồm cải tiến kiến trúc, tối ưu triển khai, nâng cao khả năng mở rộng và giảm phụ thuộc vào hạ tầng truyền thống.
* Hiểu mô hình Serverless và vai trò của các dịch vụ như Lambda, API Gateway, DynamoDB trong việc xây dựng ứng dụng mà không cần quản lý máy chủ trực tiếp.
* Nắm được lý do cần chuyển đổi từ Monolith sang Microservices, đặc biệt khi hệ thống lớn dần, khó bảo trì, khó mở rộng và cần triển khai từng chức năng độc lập.
* Biết cách chia nhỏ ứng dụng thành các service theo nghiệp vụ, mỗi service có trách nhiệm riêng, dữ liệu riêng và có thể phát triển hoặc triển khai độc lập.
* Hiểu rằng chuyển đổi kiến trúc không chỉ là tách code mà còn cần tái cấu trúc dữ liệu, quy trình xử lý và cách các thành phần giao tiếp với nhau.
* Nắm được lợi ích của kiến trúc hướng sự kiện trong việc giảm phụ thuộc trực tiếp giữa các service, hỗ trợ xử lý bất đồng bộ và tăng khả năng mở rộng hệ thống.
* Hiểu được cách xác thực ứng dụng đơn trang cần quản lý token, phiên đăng nhập và phân quyền người dùng để bảo vệ API.
* Biết cách tích hợp AI Services vào ứng dụng để mở rộng khả năng xử lý dữ liệu, tự động hóa tác vụ hoặc bổ sung tính năng thông minh.
* Nắm được một số nội dung nâng cao của DynamoDB như thiết kế khóa, tối ưu truy vấn và lựa chọn mô hình dữ liệu phù hợp với nhu cầu truy cập.