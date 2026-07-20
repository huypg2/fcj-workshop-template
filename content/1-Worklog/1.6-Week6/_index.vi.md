---
title: "Worklog Tuần 6"
date: 2026-05-29
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Tuần 6: Docker, Amazon ECS, CI/CD, DevOps workflow, storage hybrid và workflow orchestration

### Mục tiêu tuần 6:

* Tìm hiểu Docker và cách đóng gói ứng dụng thành container.
* Nắm được các thành phần chính của Amazon ECS và cách triển khai container trên AWS.
* Làm quen với CI/CD bằng AWS CodePipeline và tư duy DevOps.
* Tìm hiểu thêm các dịch vụ hỗ trợ lưu trữ hybrid, giám sát mạng và điều phối workflow.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tìm hiểu Docker, image, container, Dockerfile và lợi ích của việc container hóa ứng dụng. | 25/05/2026 | 25/05/2026 | https://000015.awsstudygroup.com/vi/ |
| Thứ 3 | Thực hành container hóa ứng dụng để ứng dụng có thể chạy ổn định giữa môi trường local, test và Cloud. | 26/05/2026 | 26/05/2026 | https://000015.awsstudygroup.com/vi/<br>https://000067.awsstudygroup.com/vi/ |
| Thứ 4 | Tìm hiểu Amazon ECS, cluster, task definition, task, service và các khái niệm liên quan đến triển khai container. | 27/05/2026 | 27/05/2026 | https://000016.awsstudygroup.com/vi/ |
| Thứ 5 | Tìm hiểu triển khai hạ tầng ECS bằng AWS CDK, cách mô tả cluster, service, task definition bằng mã nguồn. | 28/05/2026 | 28/05/2026 | https://000118.awsstudygroup.com/vi/ |
| Thứ 6 | Tìm hiểu AWS CodePipeline và quy trình CI/CD gồm lấy source code, build, test, deploy và theo dõi trạng thái pipeline. | 29/05/2026 | 29/05/2026 | https://000017.awsstudygroup.com/vi/<br>https://000023.awsstudygroup.com/vi/<br>https://000152.awsstudygroup.com/vi/ |
| Thứ 7 | Tìm hiểu AWS Storage Gateway, Amazon FSx và VPC Flow Logs trong lưu trữ hybrid, lưu trữ file và giám sát lưu lượng mạng. | 30/05/2026 | 30/05/2026 | https://000024.awsstudygroup.com/vi/<br>https://000025.awsstudygroup.com/vi/<br>https://000074.awsstudygroup.com/vi/ |
| Chủ nhật | Tìm hiểu AWS Step Functions và thực hành workshop hiệu suất lưu trữ để hiểu cách điều phối các workflow nhiều bước. | 31/05/2026 | 31/05/2026 | https://000047.awsstudygroup.com/vi/<br>https://000068.awsstudygroup.com/vi/ |

### Kết quả đạt được tuần 6:

* Hiểu được Docker giúp đóng gói ứng dụng cùng môi trường chạy, từ đó giảm lỗi khác biệt giữa local, test và production.
* Nắm được các khái niệm image, container và Dockerfile, làm nền tảng để đóng gói ứng dụng backend cho các hệ thống thực tế.
* Biết cách container hóa ứng dụng ở mức cơ bản và hiểu vì sao container phù hợp với kiến trúc microservices.
* Nắm được các thành phần chính của Amazon ECS như cluster, task definition, task và service.
* Hiểu được ECS giúp chạy và quản lý container trên AWS, phù hợp với các hệ thống cần triển khai nhiều service độc lập.
* Biết cách AWS CDK có thể hỗ trợ mô tả hạ tầng ECS bằng mã nguồn, giúp triển khai dễ lặp lại và dễ quản lý hơn.
* Hiểu được CodePipeline hỗ trợ tự động hóa quy trình CI/CD, từ bước lấy source code đến build, test và deploy.
* Nắm được vai trò của DevOps trong việc rút ngắn thời gian triển khai, giảm thao tác thủ công và tăng tính ổn định khi phát hành ứng dụng.
* Biết Storage Gateway hỗ trợ mô hình lưu trữ hybrid khi cần kết nối hệ thống tại chỗ với AWS.
* Hiểu được Amazon FSx phù hợp với nhu cầu lưu trữ file trong một số môi trường đặc thù, đặc biệt liên quan đến Windows workload.
* Nắm được VPC Flow Logs giúp quan sát lưu lượng mạng, hỗ trợ kiểm tra kết nối và phân tích sự cố trong VPC.
* Hiểu được Step Functions có thể điều phối các quy trình nhiều bước, giúp mô hình hóa workflow rõ ràng và dễ theo dõi.
* Kết nối được kiến thức Docker, ECS, CI/CD, monitoring mạng và workflow orchestration để chuẩn bị cho giai đoạn triển khai ứng dụng thực tế.