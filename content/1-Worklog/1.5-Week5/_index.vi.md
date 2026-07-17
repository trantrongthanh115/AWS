---
title: "Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

**Mục tiêu tuần:**
- Cung cấp các máy chủ ảo EC2 chạy mã nguồn web trong các private subnets.
- Cấu hình Target Group và định nghĩa các điều kiện kiểm tra sức khỏe HTTP (health checks).
- Thiết lập Auto Scaling Group (ASG) với các chính sách mở rộng tự động.
- Kiểm tra tính liên thông mạng đầu cuối từ bộ cân bằng tải đến máy chủ web.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Khởi chạy máy chủ ảo EC2 trong subnet riêng tư để bảo mật mã nguồn ứng dụng web. | 18/5 |
| Thứ Ba | Tạo Target Group `WebApp-TG` (cổng 3000) và cấu hình đường dẫn kiểm tra sức khỏe. | 19/5 |
| Thứ Tư | Liên kết Target Group với listener cổng 80 của bộ cân bằng tải Application Load Balancer. | 20/5 |
| Thứ Năm | Triển khai Auto Scaling Group `WebApp-ASG` với cấu hình tối thiểu 1, mong muốn 2, tối đa 4 instance. | 21/5 |
| Thứ Sáu | Kiểm tra định tuyến đường dẫn và xác minh lưu lượng truy cập được chia đều cho các instance hoạt động. | 22/5 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Máy chủ web khởi chạy thành công, không thể truy cập trực tiếp bằng IP công cộng.
  - Bài học: Di chuyển tài nguyên tính toán vào mạng riêng tư giúp bảo vệ mã nguồn ứng dụng khỏi các cuộc quét IP tự động.
- **Thứ Ba:**
  - Kết quả đạt được: Target Group được khởi tạo và gửi yêu cầu health check định kỳ mỗi 30 giây.
  - Bài học: Cơ chế health check giúp cô lập các máy chủ bị treo một cách tự động, nâng cao độ tin cậy của dịch vụ.
- **Thứ Tư:**
  - Kết quả đạt được: Kết nối thành công ALB và Target Group, các yêu cầu cổng 80 được chuyển tiếp đến cổng 3000 nội bộ.
  - Bài học: Ánh xạ cổng dịch vụ giúp phân tách cổng giao tiếp bên ngoài và cổng chạy ứng dụng bên trong instance.
- **Thứ Năm:**
  - Kết quả đạt được: ASG đi vào hoạt động. Thiết lập cảnh báo tự động thêm instance nếu CPU trung bình vượt quá 70%.
  - Bài học: Tự động co giãn (Auto Scaling) giúp cân bằng giữa bài toán tối ưu chi phí và đảm bảo hiệu năng khi lượng truy cập tăng vọt.
- **Thứ Sáu:**
  - Kết quả đạt được: Kiểm tra liên thông mạng thành công, người dùng truy cập qua tên miền Load Balancer đã nhận được phản hồi.
  - Bài học: Thực hiện kiểm thử tích hợp là bước bắt buộc để xác định các quy tắc bảo mật (Security Groups) không chặn nhầm luồng dữ liệu hợp lệ.
