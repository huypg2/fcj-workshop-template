---
title: "Worklog Tuần 3"
date: 2026-05-10
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Tuần 3: Mạng nâng cao, CloudFront, Lambda@Edge, Windows workload, Migration và Disaster Recovery

### Mục tiêu tuần 3:

* Củng cố kiến thức networking trên AWS và hiểu rõ hơn cách thiết kế mạng cho hệ thống.
* Tìm hiểu CloudFront, CDN và Lambda@Edge để tối ưu phân phối nội dung.
* Nắm được cách triển khai workload Windows và dịch vụ thư mục trên AWS.
* Tìm hiểu các chiến lược migration và disaster recovery khi đưa hệ thống lên Cloud.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thực hành workshop về networking trên AWS, ôn lại VPC, subnet, route table, security group, network ACL và cách phân tách tài nguyên theo lớp mạng. | 04/05/2026 | 04/05/2026 | https://docs.aws.amazon.com/vpc/ |
| Thứ 3 | Tìm hiểu Amazon CloudFront, CDN, edge location, origin, cache behavior và cách giảm độ trễ khi phân phối nội dung đến người dùng. | 05/05/2026 | 05/05/2026 | https://docs.aws.amazon.com/cloudfront/ |
| Thứ 4 | Tìm hiểu Lambda@Edge và cách xử lý một số logic gần người dùng hơn để tối ưu request, response và trải nghiệm truy cập. | 06/05/2026 | 06/05/2026 | https://docs.aws.amazon.com/lambda/latest/dg/lambda-edge.html |
| Thứ 5 | Tìm hiểu ứng dụng Windows trên AWS, môi trường Windows Server và AWS Managed Microsoft AD cho hệ thống doanh nghiệp. | 07/05/2026 | 07/05/2026 | https://docs.aws.amazon.com/directoryservice/ |
| Thứ 6 | Tìm hiểu các chiến lược migration như rehost, replatform, refactor, repurchase, retain và retire khi dịch chuyển hệ thống lên AWS. | 08/05/2026 | 08/05/2026 | https://aws.amazon.com/cloud-migration/ |
| Thứ 7 | Tìm hiểu AWS VM Import/Export, AWS Database Migration Service và Schema Conversion Tool trong quá trình di chuyển máy ảo và database. | 09/05/2026 | 09/05/2026 | https://docs.aws.amazon.com/dms/ |
| Chủ nhật | Tìm hiểu AWS Elastic Disaster Recovery và cách xây dựng phương án phục hồi hệ thống khi xảy ra sự cố. | 10/05/2026 | 10/05/2026 | https://docs.aws.amazon.com/drs/ |

### Kết quả đạt được tuần 3:

* Ôn lại và củng cố được kiến thức mạng trên AWS, đặc biệt là vai trò của VPC trong việc cô lập tài nguyên và kiểm soát luồng kết nối.
* Hiểu rõ hơn cách subnet, route table, security group và network ACL phối hợp với nhau để tạo nên mô hình mạng an toàn.
* Nắm được vai trò của CloudFront trong việc phân phối nội dung qua edge location, giúp giảm độ trễ cho người dùng ở nhiều khu vực khác nhau.
* Hiểu được cache behavior, origin và CDN có thể giúp giảm tải cho máy chủ gốc, đồng thời cải thiện tốc độ truy cập nội dung.
* Nắm được Lambda@Edge có thể xử lý logic tại edge location, phù hợp với các tình huống cần tùy biến request hoặc response gần người dùng.
* Biết thêm cách AWS hỗ trợ Windows workload, Windows Server và Managed Microsoft AD trong môi trường doanh nghiệp.
* Hiểu được các chiến lược migration khác nhau, từ cách di chuyển đơn giản như rehost đến hướng cải tiến sâu hơn như refactor.
* Nắm được vai trò của VM Import/Export khi cần đưa máy ảo hiện có lên AWS.
* Hiểu được AWS DMS và SCT hỗ trợ quá trình di chuyển database và chuyển đổi schema giữa các hệ quản trị khác nhau.
* Nắm được tầm quan trọng của disaster recovery trong hệ thống thực tế, đặc biệt đối với ứng dụng yêu cầu tính sẵn sàng cao.
* Biết AWS Elastic Disaster Recovery giúp giảm thời gian khôi phục và hỗ trợ chuẩn bị kế hoạch ứng phó khi hệ thống gặp sự cố.


