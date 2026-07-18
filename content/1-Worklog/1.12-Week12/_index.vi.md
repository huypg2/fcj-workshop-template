---
title: "Worklog Tuần 12"
date: 2026-07-10
weight: 12
chapter: false
pre: " <b> 1.12 </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Tuần 12: CloudWatch Alarm, Load Testing, S3 Backup, Verification và Cleanup

### Mục tiêu tuần 12:

* Tạo SNS Topic, CloudWatch Alarm và chạy Load Testing theo đúng nhóm công việc giám sát.
* Cấu hình S3 Backup, KMS, IAM Policy/Role và Export Snapshot.
* Thực hiện Verification và Cleanup để hoàn tất quá trình triển khai.

### Các công việc cần triển khai trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 06/07/2026 | - Tạo SNS Topic cho cảnh báo<br>&emsp; + Tạo kênh nhận thông báo từ hệ thống giám sát<br>&emsp; + Cấu hình thông tin nhận thông báo<br>&emsp; + Chuẩn bị SNS Topic để liên kết với CloudWatch Alarm | 06/07/2026 | 06/07/2026 | https://000077.awsstudygroup.com/ |
| 07/07/2026 | - Tạo CloudWatch Alarm và chạy Load Testing<br>&emsp; + Chọn metric cần theo dõi<br>&emsp; + Gắn alarm với SNS Topic đã tạo<br>&emsp; + Chạy kiểm tra tải để quan sát metric và trạng thái alarm | 07/07/2026 | 07/07/2026 | https://000008.awsstudygroup.com/ |
| 08/07/2026 | - Cấu hình S3 Bucket và KMS cho backup<br>&emsp; + Tạo bucket dùng để lưu dữ liệu backup/export<br>&emsp; + Cấu hình mã hóa bằng KMS<br>&emsp; + Kiểm tra cấu hình lưu trữ và mã hóa sau khi thiết lập | 08/07/2026 | 08/07/2026 | https://000057.awsstudygroup.com/<br>https://000033.awsstudygroup.com/ |
| 09/07/2026 | - Tạo IAM Policy/Role và Export Snapshot<br>&emsp; + Tạo quyền cần thiết cho tác vụ backup/export<br>&emsp; + Cấu hình quyền truy cập S3, KMS và RDS<br>&emsp; + Thực hiện export snapshot và kiểm tra dữ liệu trên S3 | 09/07/2026 | 09/07/2026 | https://000005.awsstudygroup.com/<br>https://000013.awsstudygroup.com/ |
| 10/07/2026 | - Verification và Cleanup tài nguyên<br>&emsp; + Kiểm tra lại các thành phần đã triển khai<br>&emsp; + Xác nhận các bước chính đã hoạt động đúng<br>&emsp; + Xóa hoặc dừng tài nguyên AWS không còn sử dụng | 10/07/2026 | 10/07/2026 | https://000007.awsstudygroup.com/<br>https://cloudjourney.awsstudygroup.com/vi/3-optimize/ |

### Kết quả đạt được tuần 12:

* Tạo được SNS Topic để phục vụ gửi thông báo cảnh báo.
* Cấu hình được thông tin nhận thông báo từ SNS.
* Tạo được CloudWatch Alarm theo metric cần theo dõi.
* Gắn được Alarm với SNS Topic để nhận cảnh báo khi điều kiện được kích hoạt.
* Chạy được bước Load Testing để quan sát sự thay đổi của metric và trạng thái alarm.
* Tạo được S3 Bucket phục vụ lưu trữ dữ liệu backup hoặc export.
* Cấu hình được mã hóa KMS cho dữ liệu lưu trên S3.
* Tạo được IAM Policy/Role phục vụ tác vụ backup/export.
* Cấu hình được quyền truy cập cần thiết đến S3, KMS và RDS.
* Thực hiện được Export Snapshot và kiểm tra dữ liệu xuất ra trong S3.
* Thực hiện Verification để rà soát lại các thành phần đã triển khai.
* Thực hiện Cleanup tài nguyên không còn sử dụng để hạn chế phát sinh chi phí.
* Hoàn thành đúng nhóm công việc CloudWatch Alarm, Load Testing, S3 Backup, Verification và Cleanup; nguồn tham khảo dùng tài liệu trong Cloud Journey/AWS Study Group.