---
title: "Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

**Mục tiêu tuần:**
- Khởi tạo và cấu hình Amazon CloudFront Distribution để phân phối tài nguyên tĩnh.
- Tích hợp AWS Web Application Firewall (WAF) để bảo vệ các endpoint.
- Triển khai bộ cân bằng tải Application Load Balancer (ALB) trên nhiều Availability Zones.
- Cấu hình các quy tắc định tuyến, listener và chuyển tiếp lưu lượng mạng.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Khởi tạo trình cấu hình Amazon CloudFront, tạo phân phối `WebApp-Distribution` mới. | 11/5 |
| Thứ Ba | Thiết lập cấu hình Origin cho CloudFront trỏ tới endpoint của API Gateway. | 12/5 |
| Thứ Tư | Tối ưu hóa các chính sách lưu đệm (cache policies), cấu hình chuyển tiếp Header và thời gian TTL tùy chỉnh. | 13/5 |
| Thứ Năm | Tích hợp AWS WAF với các quy tắc giới hạn tần suất (Rate Limiting) để chống các cuộc tấn công DDoS. | 14/5 |
| Thứ Sáu | Cung cấp bộ cân bằng tải `WebApp-ALB` hướng internet trên hai Availability Zones (`ap-southeast-1a` và `1b`). | 15/5 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Hoàn thành cấu hình phân phối CloudFront cơ sở để tối ưu hóa truyền tải.
  - Bài học: Sử dụng mạng phân phối nội dung (CDN) giúp giảm thiểu đáng kể độ trễ truy cập nội dung tĩnh bằng cách đưa dữ liệu đến gần người dùng.
- **Thứ Ba:**
  - Kết quả đạt được: Cấu hình chuyển tiếp thành công các yêu cầu API từ CloudFront đến API Gateway.
  - Bài học: Cấu hình Origin phải khớp với giao thức bảo mật (HTTPS) và domain để tránh lỗi kết nối.
- **Thứ Tư:**
  - Kết quả đạt được: Thiết lập xong cache policy, cho phép lưu đệm tệp tĩnh nhưng bỏ qua cache đối với các API đăng nhập/xác thực.
  - Bài học: Việc phân tách chính sách cache giúp bảo mật thông tin phiên làm việc của người dùng.
- **Thứ Năm:**
  - Kết quả đạt được: Kích hoạt WAF thành công, thiết lập ngưỡng chặn IP nếu gửi quá số yêu cầu quy định trong 5 phút.
  - Bài học: Ngăn chặn lưu lượng truy cập độc hại từ biên giúp giảm tải tính toán cho các máy chủ web phía sau.
- **Thứ Sáu:**
  - Kết quả đạt được: Load Balancer hoạt động ổn định, kiểm tra phân giải tên miền DNS của ALB thành công.
  - Bài học: ALB phải phân bổ trên nhiều AZ khác nhau để đảm bảo khả năng dự phòng nếu một trung tâm dữ liệu gặp sự cố.
