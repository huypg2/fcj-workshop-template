---
title: "Worklog Tuần 3"
date: 2026-05-08
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 3:

* **Chủ đề:** Mạng nâng cao, phân phối nội dung và dịch chuyển hạ tầng.
* Tuần này đi sâu vào luồng dữ liệu mạng, tối ưu phân phối nội dung và các chiến lược dịch chuyển hệ thống lên Cloud.
* Củng cố kiến thức networking thông qua workshop thực hành trên AWS.
* Tìm hiểu CloudFront, Lambda@Edge và các giải pháp tối ưu phân phối nội dung.
* Nắm các hướng migration, chuyển máy ảo, chuyển cơ sở dữ liệu và phục hồi sau thảm họa.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 01/05/2026 | - Thực hành workshop networking trên AWS. <br> - Kết quả: Hiểu rõ hơn cách thiết kế VPC, subnet, route table, security group và luồng kết nối giữa các thành phần. | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 02/05/2026 | - Tìm hiểu Amazon CloudFront. <br> - Kết quả: Nắm được cách CDN cache nội dung tại edge location để giảm độ trễ và giảm tải cho origin. | 02/05/2026 | 02/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 03/05/2026 | - Tìm hiểu Lambda@Edge kết hợp với CloudFront. <br> - Kết quả: Biết cách xử lý một số logic request/response gần người dùng hơn. | 03/05/2026 | 03/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 04/05/2026 | - Tìm hiểu ứng dụng Windows trên AWS và AWS Managed Microsoft AD. <br> - Kết quả: Hiểu cách AWS hỗ trợ workload Windows và dịch vụ thư mục cho môi trường doanh nghiệp. | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 05/05/2026 | - Tìm hiểu các chiến lược dịch chuyển lên AWS. <br> - Kết quả: Phân biệt được rehost, replatform, refactor và cách lựa chọn hướng migration phù hợp. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 06/05/2026 | - Tìm hiểu AWS VM Import/Export, AWS DMS và SCT. <br> - Kết quả: Nắm được cách di chuyển máy ảo và cơ sở dữ liệu sang AWS. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 07/05/2026 | - Tìm hiểu AWS Elastic Disaster Recovery. <br> - Kết quả: Hiểu cách chuẩn bị phương án khôi phục hệ thống, giảm downtime và bảo vệ dữ liệu khi có sự cố. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 3:

* Nắm được kiến thức mạng nâng cao hơn trên AWS, đặc biệt là cách phối hợp VPC, subnet, route table, security group và network ACL để kiểm soát luồng dữ liệu.
* Hiểu được vai trò của CloudFront trong tối ưu tốc độ truy cập, giảm độ trễ và giảm tải cho máy chủ gốc thông qua cơ chế cache tại edge location.
* Nắm được cách Lambda@Edge hỗ trợ xử lý logic gần người dùng hơn, phù hợp với các tình huống cần tùy chỉnh request, response hoặc phân phối nội dung động ở mức đơn giản.
* Làm quen với các workload Windows trên AWS, bao gồm máy chủ Windows, dịch vụ thư mục Microsoft AD và nhu cầu tích hợp hệ thống doanh nghiệp hiện có lên Cloud.
* Hiểu được các chiến lược migration phổ biến như rehost, replatform và refactor, từ đó biết rằng việc dịch chuyển lên Cloud cần đánh giá hiện trạng ứng dụng trước khi chọn giải pháp.
* Nắm được cách VM Import/Export hỗ trợ chuyển máy ảo hiện có sang EC2 và cách DMS hỗ trợ di chuyển dữ liệu giữa các hệ quản trị cơ sở dữ liệu.
* Biết vai trò của Schema Conversion Tool trong các trường hợp cần chuyển đổi schema khi thay đổi database engine trong quá trình migration.
* Hiểu được mục tiêu của Elastic Disaster Recovery là giảm thời gian gián đoạn, hỗ trợ sao chép hệ thống và tăng khả năng phục hồi khi xảy ra sự cố nghiêm trọng.
* Có cái nhìn rõ hơn về mối liên hệ giữa networking, CDN, migration và disaster recovery trong việc xây dựng hệ thống Cloud ổn định và sẵn sàng mở rộng.


