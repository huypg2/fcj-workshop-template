---
title: "Worklog Tuần 7"
date: 2026-06-05
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 7:

* **Chủ đề:** Container, CI/CD và luồng công việc DevOps.
* Tuần này tập trung vào đóng gói ứng dụng, điều phối container và xây dựng pipeline triển khai liên tục.
* Tìm hiểu Docker, Amazon ECS và hạ tầng ECS bằng CDK.
* Nắm quy trình CI/CD với AWS CodePipeline.
* Làm quen với Storage Gateway, FSx, VPC Flow Logs, Step Functions và hiệu suất lưu trữ.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 29/05/2026 | - Tìm hiểu Docker và cách container hóa ứng dụng. <br> - Kết quả: Biết cách đóng gói ứng dụng cùng thư viện phụ thuộc để chạy ổn định trên nhiều môi trường. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 30/05/2026 | - Tìm hiểu Amazon ECS. <br> - Kết quả: Nắm được cluster, task definition, service và cách ECS quản lý container. | 30/05/2026 | 30/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 31/05/2026 | - Tìm hiểu CDK cho ECS. <br> - Kết quả: Biết cách mô tả hạ tầng ECS bằng code để triển khai nhất quán hơn. | 31/05/2026 | 31/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 01/06/2026 | - Tìm hiểu AWS CodePipeline và CI/CD. <br> - Kết quả: Nắm được luồng tự động hóa từ source code, build, test đến deploy. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 02/06/2026 | - Tìm hiểu AWS Storage Gateway và Amazon FSx. <br> - Kết quả: Hiểu cách kết nối lưu trữ on-premises với Cloud và lưu trữ file cho môi trường Windows. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 03/06/2026 | - Tìm hiểu VPC Flow Logs và AWS Step Functions. <br> - Kết quả: Biết cách giám sát lưu lượng mạng và điều phối quy trình xử lý nhiều bước. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 04/06/2026 | - Thực hiện workshop hiệu suất lưu trữ. <br> - Kết quả: Hiểu thêm cách lựa chọn dịch vụ lưu trữ phù hợp theo nhu cầu hiệu năng và truy cập. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 7:

* Nắm được lợi ích của Docker trong việc đóng gói ứng dụng, đảm bảo môi trường chạy nhất quán và giảm lỗi phát sinh do khác biệt cấu hình giữa các máy.
* Hiểu được các thành phần chính của Amazon ECS như cluster, task definition, container, service và cách ECS hỗ trợ triển khai ứng dụng container trên AWS.
* Biết cách sử dụng AWS CDK để mô tả hạ tầng ECS bằng code, giúp quá trình tạo cluster, service và load balancer dễ tái sử dụng hơn.
* Nắm được vai trò của CI/CD trong DevOps, hiểu cách CodePipeline kết nối các bước lấy source code, build, test và deploy để giảm thao tác thủ công.
* Hiểu cách tự động hóa triển khai giúp giảm lỗi khi release ứng dụng, tăng tốc độ cập nhật và hỗ trợ quy trình làm việc nhóm hiệu quả hơn.
* Làm quen với Storage Gateway như một giải pháp kết nối lưu trữ tại chỗ với Cloud, phù hợp với môi trường hybrid hoặc hệ thống cần đồng bộ dữ liệu.
* Nắm được vai trò của Amazon FSx trong lưu trữ file cho hệ thống Windows và các ứng dụng cần file system được quản lý.
* Biết cách VPC Flow Logs hỗ trợ giám sát lưu lượng mạng, phân tích kết nối bị chặn và phát hiện các luồng truy cập bất thường.
* Hiểu cách Step Functions điều phối workflow nhiều bước, giúp quản lý các quy trình xử lý phức tạp có sự tham gia của nhiều dịch vụ AWS.