---
title: "Worklog Tuần 9"
date: 2026-06-19
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Tuần 9: Xây dựng giao diện Frontend cho hệ thống NextGenPay và hỗ trợ kiểm thử tải API

### Mục tiêu tuần 9:

* Xây dựng giao diện Frontend cho hệ thống thanh toán NextGenPay.
* Thiết kế các màn hình phục vụ tổng quan hệ thống, quản lý tài khoản, thanh toán hóa đơn, lịch sử giao dịch và kiểm thử tải API.
* Xây dựng giao diện gửi yêu cầu thanh toán có hỗ trợ Idempotency Key để kiểm tra cơ chế chống trùng lặp giao dịch.
* Hiển thị phản hồi thanh toán, trạng thái giao dịch và lịch sử giao dịch theo User ID.
* Chuẩn bị giao diện để tích hợp với Backend/API và phục vụ kiểm thử tải hệ thống ở các bước tiếp theo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | - Phân tích yêu cầu giao diện hệ thống NextGenPay<br>&emsp; + Xác định các màn hình chính gồm Tổng quan, Quản lý tài khoản, Thanh toán hóa đơn, Lịch sử giao dịch và Kiểm thử tải API<br>&emsp; + Xác định các thông tin cần hiển thị như trạng thái hệ thống, thông tin tài khoản, dữ liệu giao dịch và kết quả thanh toán<br>&emsp; + Lên bố cục tổng quan cho sidebar, header và khu vực nội dung chính | 15/06/2026 | 15/06/2026 |  |
| Thứ 3 | - Xây dựng bố cục giao diện chính<br>&emsp; + Thiết kế sidebar điều hướng cho các chức năng của hệ thống<br>&emsp; + Xây dựng header hiển thị trạng thái hệ thống và nút cập nhật trạng thái<br>&emsp; + Bổ sung nút chuyển đổi ngôn ngữ để hỗ trợ giao diện song ngữ | 16/06/2026 | 16/06/2026 |  |
| Thứ 4 | - Xây dựng giao diện thanh toán hóa đơn<br>&emsp; + Tạo form nhập Source Account ID, User ID, số tiền giao dịch và loại tiền tệ<br>&emsp; + Bổ sung trường Idempotency Key và nút Gen để tạo khóa chống trùng lặp giao dịch<br>&emsp; + Xây dựng nút thực hiện thanh toán và chuẩn bị dữ liệu gửi sang Backend/API | 17/06/2026 | 17/06/2026 |  |
| Thứ 5 | - Xây dựng khu vực phản hồi thanh toán và kiểm toán giao dịch<br>&emsp; + Hiển thị phản hồi từ cổng thanh toán gồm HTTP Status, Success Status, Message, Payment ID và State<br>&emsp; + Xây dựng chức năng truy vấn giao dịch theo User ID<br>&emsp; + Hiển thị lịch sử giao dịch gồm số tiền, trạng thái và thời gian xử lý | 18/06/2026 | 18/06/2026 |  |
| Thứ 6 | - Hoàn thiện giao diện và chuẩn bị cho kiểm thử tải API<br>&emsp; + Rà soát bố cục, màu sắc, khoảng cách và khả năng hiển thị của giao diện<br>&emsp; + Kiểm tra luồng thao tác gửi yêu cầu thanh toán, nhận phản hồi và xem lịch sử giao dịch<br>&emsp; + Chuẩn bị khu vực Kiểm thử tải API để theo dõi request, trạng thái xử lý và kết quả test ở các bước tiếp theo | 19/06/2026 | 19/06/2026 |  |

### Kết quả đạt được tuần 9:

* Xây dựng được giao diện Frontend cơ bản cho hệ thống NextGenPay.
* Hoàn thiện sidebar điều hướng gồm Tổng quan, Quản lý tài khoản, Thanh toán hóa đơn, Lịch sử giao dịch và Kiểm thử tải API.
* Xây dựng được header hiển thị trạng thái hệ thống và chức năng cập nhật trạng thái.
* Bổ sung được nút chuyển đổi ngôn ngữ để hỗ trợ giao diện song ngữ.
* Xây dựng được màn hình thanh toán hóa đơn với các trường Source Account ID, User ID, số tiền giao dịch, loại tiền tệ và Idempotency Key.
* Bổ sung được chức năng tạo Idempotency Key để hỗ trợ kiểm tra cơ chế chống trùng lặp giao dịch.
* Hiển thị được phản hồi từ cổng thanh toán gồm HTTP Status, Success Status, Message, Payment ID và State.
* Xây dựng được khu vực kiểm toán giao dịch theo User ID.
* Hiển thị được lịch sử giao dịch với số tiền, trạng thái và thời gian giao dịch.
* Chuẩn bị được giao diện Kiểm thử tải API để hỗ trợ theo dõi request, trạng thái xử lý và kết quả kiểm thử ở các bước tiếp theo.
* Hoàn thiện giao diện Frontend để sẵn sàng tích hợp với Backend/API.