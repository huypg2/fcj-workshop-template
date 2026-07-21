---
title: "Event 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch “FCJ Community Day - From Zero to Cloud Hero”

## 1. Tổng quan sự kiện

**FCJ Community Day - From Zero to Cloud Hero** là sự kiện chia sẻ nhiều nội dung thực tế liên quan đến phát triển ứng dụng, vận hành hệ thống, trí tuệ nhân tạo và an toàn thông tin trên nền tảng AWS. Các chủ đề trong chương trình giúp người tham dự có thêm góc nhìn về cách xây dựng hệ thống hiện đại, từ giao tiếp thời gian thực, đóng gói ứng dụng, xử lý dữ liệu cho LLM, phát hiện tấn công mạng đến định hướng phát triển nghề nghiệp trong lĩnh vực hạ tầng và DevOps.

Sự kiện không chỉ tập trung vào lý thuyết, mà còn gắn với các mô hình triển khai thực tế, công cụ phổ biến và kinh nghiệm làm việc trong môi trường công nghệ.


## 2. Nội dung chương trình

Trong sự kiện, các diễn giả đã chia sẻ nhiều chủ đề khác nhau.

**Nguyễn Quốc Bảo** trình bày chủ đề **“Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets”**. Phần chia sẻ làm rõ cách các client trong game có thể giao tiếp theo thời gian thực trên môi trường cloud. Nội dung nhấn mạnh vai trò của WebSocket và AWS API Gateway trong việc duy trì kết nối hai chiều, phù hợp với các ứng dụng multiplayer cần phản hồi nhanh.

**Bảo Huỳnh** trình bày chủ đề **“Docker – A containerization technology”**. Nội dung tập trung giải thích cách Docker đóng gói ứng dụng cùng môi trường chạy, giúp việc triển khai trở nên nhất quán hơn. Bài chia sẻ cũng so sánh container với máy ảo, qua đó làm nổi bật ưu điểm về tốc độ khởi động, khả năng tiết kiệm tài nguyên và tính linh hoạt trong DevOps.

**Việt Phát** trình bày chủ đề **“GraphRAG: Build GraphRAG applications using Amazon Bedrock and Amazon Neptune”**. Phần trình bày giới thiệu hướng xây dựng ứng dụng AI bằng cách kết hợp Amazon Bedrock với Amazon Neptune. Nội dung cho thấy Knowledge Graph và Vector Database có thể hỗ trợ LLM truy xuất thông tin theo ngữ cảnh tốt hơn, từ đó nâng cao độ chính xác của câu trả lời.

**Lê Hoàng Gia Đại** trình bày chủ đề **“WAF + ML for Cyber Attack Detection: Machine Learning-based Network Intrusion Detection System (NIDS) on AWS”**. Nội dung xoay quanh việc ứng dụng Machine Learning vào phát hiện tấn công mạng trên AWS. Diễn giả trình bày cách kết hợp mô hình LightGBM với AWS WAF để nhận diện các hành vi bất thường và tăng cường khả năng bảo vệ hệ thống.

**Trần Trung Vinh** trình bày chủ đề **“From IT Helpdesk to Senior Sysadmin”**. Phần chia sẻ tập trung vào hành trình phát triển nghề nghiệp trong lĩnh vực quản trị hệ thống. Nội dung giúp người tham dự hiểu rõ hơn về quá trình chuyển từ công việc IT Helpdesk sang Senior Sysadmin, cũng như các kỹ năng cần có khi vận hành hạ tầng On-Premise và tiếp cận tư duy quản trị hệ thống hiện đại.

## 3. Những điểm đáng chú ý

Điểm nổi bật đầu tiên của sự kiện là phần chia sẻ về WebSocket trên AWS. Nội dung này cho thấy các ứng dụng real-time như game multiplayer, chat hoặc hệ thống cập nhật trạng thái có thể được xây dựng theo hướng serverless, giảm bớt việc quản lý máy chủ và tăng khả năng mở rộng.

Phần Docker cũng rất thực tế vì container là công nghệ quan trọng trong triển khai ứng dụng hiện nay. Việc hiểu image, container, layer, volume và network giúp quá trình đóng gói, chạy thử và triển khai ứng dụng trở nên ổn định hơn giữa các môi trường.

Một điểm đáng chú ý khác là GraphRAG. Nội dung này giúp mở rộng góc nhìn về GenAI, đặc biệt là cách kết hợp LLM với dữ liệu có quan hệ. Việc dùng Knowledge Graph giúp hệ thống AI hiểu rõ hơn mối liên kết giữa các thực thể, thay vì chỉ dựa vào đoạn văn bản tương đồng.

Ngoài ra, phần bảo mật với AWS WAF và Machine Learning cho thấy xu hướng kết hợp nhiều lớp phòng thủ trong hệ thống hiện đại. Không chỉ chặn request theo rule, hệ thống còn có thể phân tích dữ liệu để phát hiện các hành vi bất thường.

Phần chia sẻ về lộ trình IT Helpdesk đến Senior Sysadmin giúp người tham dự hiểu rằng để phát triển trong lĩnh vực hạ tầng và DevOps, cần xây dựng nền tảng từng bước, bắt đầu từ kỹ năng xử lý sự cố, quản trị hệ thống, mạng máy tính đến tự động hóa và cloud.

## 4. Những điều học được

Sau sự kiện, tôi hiểu rõ hơn về vai trò của AWS trong các hệ thống hiện đại. AWS không chỉ hỗ trợ triển khai ứng dụng web thông thường, mà còn có thể áp dụng cho game real-time, ứng dụng AI, hệ thống bảo mật và hạ tầng vận hành quy mô lớn.

Tôi cũng học được rằng Docker là một công cụ quan trọng khi làm dự án phần mềm. Việc đóng gói ứng dụng bằng container giúp giảm lỗi khác biệt môi trường, hỗ trợ triển khai nhanh và phù hợp với các mô hình DevOps.

Bên cạnh đó, tôi biết thêm về GraphRAG và cách Knowledge Graph có thể hỗ trợ LLM xử lý thông tin tốt hơn. Đây là một hướng tiếp cận hữu ích khi xây dựng các ứng dụng AI cần độ chính xác và ngữ cảnh cao.

Về bảo mật, tôi nhận ra rằng hệ thống cần có nhiều lớp bảo vệ. Việc kết hợp AWS WAF với Machine Learning có thể giúp phát hiện cả những mẫu tấn công đã biết và những hành vi bất thường chưa được định nghĩa rõ bằng rule.

Đối với định hướng nghề nghiệp, sự kiện giúp tôi hiểu rằng kỹ năng nền tảng rất quan trọng. Muốn đi xa trong Cloud hoặc DevOps cần rèn luyện Linux, Networking, Docker, CI/CD, Infrastructure as Code, monitoring và kỹ năng phân tích lỗi.

## 5. Ứng dụng sau sự kiện

Sau sự kiện, tôi có thể áp dụng kiến thức Docker vào việc đóng gói các service trong dự án, giúp ứng dụng chạy ổn định hơn khi chuyển từ môi trường local sang môi trường triển khai.

Tôi cũng có thể tìm hiểu thêm về WebSocket trên AWS để áp dụng cho các chức năng cần cập nhật dữ liệu theo thời gian thực, chẳng hạn như dashboard trạng thái hệ thống, thông báo hoặc theo dõi tiến trình xử lý.

Với kiến thức về GraphRAG, tôi có thêm định hướng khi tìm hiểu các ứng dụng GenAI có sử dụng dữ liệu riêng. Việc kết hợp Amazon Bedrock, Amazon Neptune và Knowledge Graph là một hướng phù hợp cho các hệ thống cần truy xuất thông tin có quan hệ phức tạp.

Về bảo mật, tôi có thể tiếp tục nghiên cứu AWS WAF, CloudWatch, SNS và các mô hình phát hiện bất thường để hiểu rõ hơn cách giám sát, cảnh báo và bảo vệ hệ thống trên cloud.

Ngoài ra, phần chia sẻ về lộ trình nghề nghiệp giúp tôi có kế hoạch học tập rõ hơn, tập trung vào nền tảng hệ thống, mạng, Linux, container, CI/CD và cloud trước khi đi sâu vào các công nghệ nâng cao.

## 6. Cảm nhận cá nhân

Sự kiện **FCJ Community Day - From Zero to Cloud Hero** mang lại nhiều kiến thức thực tế và có tính ứng dụng cao. Các chủ đề tuy thuộc nhiều mảng khác nhau nhưng đều liên quan đến việc xây dựng, triển khai, vận hành và bảo vệ hệ thống hiện đại.

Tôi ấn tượng với cách các diễn giả trình bày từ góc nhìn thực tế, giúp nội dung dễ hiểu hơn và không bị quá lý thuyết. Đặc biệt, các phần về Docker, WebSocket, GraphRAG và bảo mật trên AWS giúp tôi có thêm nhiều ý tưởng để áp dụng vào dự án cá nhân cũng như quá trình học Cloud.

## 7. Tổng kết

Tổng thể, sự kiện giúp tôi mở rộng kiến thức về AWS, Docker, WebSocket, GraphRAG, Machine Learning trong bảo mật và lộ trình phát triển nghề nghiệp trong lĩnh vực hệ thống. Sau sự kiện, tôi nhận thấy rằng một hệ thống hiện đại không chỉ cần code chạy đúng, mà còn cần kiến trúc phù hợp, khả năng mở rộng, quy trình triển khai ổn định, cơ chế giám sát và lớp bảo mật hiệu quả.

#### Một số hình ảnh khi tham gia sự kiện

![Event 3](/images/b8.jpg)
![Event 3](/images/b9.jpg)
![Event 3](/images/b10.jpg)

> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
