---
title: "Worklog Tuần 9"
date: 2026-06-19
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Tuần 9: Xây dựng giao diện Frontend cho hệ thống theo dõi kết quả kiểm thử

### Mục tiêu tuần 9:

* Xây dựng giao diện Frontend phục vụ việc theo dõi hệ thống sau quá trình kiểm thử tải.
* Thiết kế bố cục hiển thị các thông số chính của hệ thống.
* Tạo các màn hình hiển thị kết quả test, trạng thái request và thống kê hiệu năng.
* Chuẩn bị giao diện để tích hợp với Backend/API ở các bước tiếp theo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | - Phân tích yêu cầu giao diện Frontend<br>&emsp; + Xác định các thông tin cần hiển thị sau khi chạy kiểm thử tải<br>&emsp; + Xác định các nhóm dữ liệu như tổng request, request thành công, request lỗi, thời gian phản hồi và trạng thái hệ thống<br>&emsp; + Lên bố cục tổng quan cho màn hình dashboard | 15/06/2026 | 15/06/2026 |  |
| Thứ 3 | - Xây dựng giao diện dashboard chính<br>&emsp; + Tạo layout cho trang hiển thị kết quả kiểm thử<br>&emsp; + Thiết kế các thẻ thống kê như Total Requests, Success Rate, Error Rate và Response Time<br>&emsp; + Sắp xếp bố cục giao diện rõ ràng, dễ theo dõi | 16/06/2026 | 16/06/2026 |  |
| Thứ 4 | - Xây dựng bảng hiển thị lịch sử test<br>&emsp; + Tạo bảng danh sách các lần kiểm thử đã thực hiện<br>&emsp; + Hiển thị các thông tin như thời gian test, số lượng request, số user ảo, tỉ lệ lỗi và kết quả<br>&emsp; + Bổ sung trạng thái Passed/Failed để dễ đánh giá kết quả | 17/06/2026 | 17/06/2026 |  |
| Thứ 5 | - Xây dựng khu vực hiển thị biểu đồ và thông số hệ thống<br>&emsp; + Tạo khu vực biểu đồ cho response time, throughput và error rate<br>&emsp; + Hiển thị thông tin liên quan đến CPU, memory, số lượng task và trạng thái service<br>&emsp; + Chuẩn bị cấu trúc dữ liệu giả lập để kiểm tra giao diện trước khi kết nối API | 18/06/2026 | 18/06/2026 |  |
| Thứ 6 | - Hoàn thiện giao diện và kiểm tra hiển thị<br>&emsp; + Rà soát lại màu sắc, khoảng cách, font chữ và bố cục giao diện<br>&emsp; + Kiểm tra khả năng hiển thị trên nhiều kích thước màn hình<br>&emsp; + Chuẩn bị giao diện để tích hợp với Backend/API trong các bước triển khai tiếp theo | 19/06/2026 | 19/06/2026 |  |

### Kết quả đạt được tuần 9:

* Xác định được các thông tin cần hiển thị trên giao diện Frontend.
* Thiết kế được bố cục dashboard phục vụ theo dõi kết quả kiểm thử tải.
* Xây dựng được các thẻ thống kê tổng quan như tổng request, request thành công, request lỗi và thời gian phản hồi.
* Xây dựng được bảng lịch sử các lần kiểm thử.
* Hiển thị được các thông tin như thời gian test, số lượng request, số user ảo, tỉ lệ lỗi và trạng thái kết quả.
* Xây dựng được khu vực biểu đồ phục vụ theo dõi response time, throughput và error rate.
* Chuẩn bị được khu vực hiển thị thông số hệ thống như CPU, memory, task count và service status.
* Tạo được dữ liệu giả lập để kiểm tra giao diện trước khi tích hợp API.
* Kiểm tra và điều chỉnh lại bố cục, màu sắc, khoảng cách và khả năng hiển thị của giao diện.
* Hoàn thiện giao diện Frontend cơ bản để phục vụ việc theo dõi kết quả kiểm thử và tích hợp với Backend ở các bước tiếp theo.