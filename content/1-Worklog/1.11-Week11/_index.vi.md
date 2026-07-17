---
title: "Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

**Mục tiêu tuần:**
- Kết nối SSH vào máy chủ EC2 Production và cài đặt các môi trường phụ thuộc.
- Cài đặt Git, Node.js (qua NVM) và công cụ quản lý tiến trình PM2 trên cloud instance.
- Cấu hình các biến môi trường chạy thực tế (`DATABASE_URL`, `API_URL`, `PORT`).
- Triển khai backend và frontend của ứng dụng Web, sử dụng PM2 để chạy nền.
- Cấu hình Nginx làm Proxy ngược (Reverse Proxy) chuyển hướng traffic cổng 80 sang cổng Node.js nội bộ.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Kết nối SSH tới máy ảo EC2 thông qua key pair bảo mật và cập nhật các gói bản vá lỗi OS. | 29/6 |
| Thứ Ba | Cài đặt Git, Node.js (sử dụng trình quản lý phiên bản NVM) và PM2 trên máy chủ. | 30/6 |
| Thứ Tư | Clone dự án từ Github về máy ảo, thiết lập cấu hình file môi trường thực tế `.env`. | 1/7 |
| Thứ Năm | Khởi chạy ứng dụng chạy ngầm trên cổng nội bộ 3000 dưới sự quản lý của PM2. | 2/7 |
| Thứ Sáu | Cài đặt và cấu hình Nginx chuyển hướng cổng 80 về cổng 3000, kiểm tra truy cập qua DNS của Load Balancer. | 3/7 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Đăng nhập thành công qua SSH và tối ưu hóa hệ thống máy chủ.
  - Bài học: Giới hạn quyền SSH ingress trong Security Group chỉ cho một số IP Admin cụ thể giúp bảo vệ máy chủ khỏi brute-force.
- **Thứ Ba:**
  - Kết quả đạt được: Cài đặt xong runtime Node.js và cài đặt PM2 toàn cục.
  - Bài học: Sử dụng NVM giúp dễ dàng chuyển đổi và đồng bộ phiên bản Node.js chạy thực tế giống hệt phiên bản ở local.
- **Thứ Tư:**
  - Kết quả đạt được: Cấu hình các đường dẫn kết nối database RDS an toàn mà không bị lộ lọt credential.
  - Bài học: Việc lưu thông tin bảo mật trong file `.env` thay vì ghi cứng trong mã nguồn là nguyên lý thiết kế ứng dụng an toàn.
- **Thứ Năm:**
  - Kết quả đạt được: Tiến trình backend chạy ổn định, tự động khởi động lại nếu ứng dụng bị crash đột ngột.
  - Bài học: PM2 đóng vai trò quan trọng trong việc giám sát tiến trình và khởi chạy ứng dụng khi máy chủ khởi động lại.
- **Thứ Sáu:**
  - Kết quả đạt được: Nginx proxy ngược thành công. Người dùng ngoài internet đã có thể truy cập website bán lẻ.
  - Bài học: Proxy ngược bảo vệ ứng dụng khỏi các nguy cơ tấn công trực tiếp và cho phép xử lý luồng ghi log hiệu quả hơn.
