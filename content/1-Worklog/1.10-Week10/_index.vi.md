---
title: "Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

**Mục tiêu tuần:**
- Thiết kế giao diện cho Cổng thông tin bán lẻ thời trang Global Fashion Retail Web Portal.
- Triển khai xác thực bảo mật dựa trên Token JWT với thời hạn hết hạn phiên là 8 giờ.
- Tích hợp xác thực đa lớp (2FA TOTP) sử dụng mã QR Code kết nối Google Authenticator.
- Triển khai phân quyền truy cập (RBAC) phân tách các quyền Admin, Manager và Associate.
- Tích hợp biểu đồ trực quan hóa doanh thu thực tế đối chiếu với chỉ số dự báo của mô hình ML.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Thiết kế giao diện Dashboard Cổng thông tin thời trang sử dụng React và Tailwind CSS. | 22/6 |
| Thứ Ba | Lập trình module xác thực ở backend để cấp phát và kiểm tra chữ ký token JWT phiên đăng nhập. | 23/6 |
| Thứ Tư | Viết mã giao diện đăng ký 2FA, sinh mã QR Code để quét ứng dụng Google Authenticator. | 24/6 |
| Thứ Năm | Thiết lập phân quyền chức năng (RBAC) giới hạn ranh giới hiển thị bảng điều khiển theo vai trò người dùng. | 25/6 |
| Thứ Sáu | Tích hợp biểu đồ trực quan hóa so sánh doanh số bán hàng thực tế và đường dự báo của mô hình. | 26/6 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Hoàn thành thiết kế giao diện thân thiện, tương thích tốt trên các thiết bị di động.
  - Bài học: Thiết kế UI sạch sẽ và trực quan giúp người quản lý vận hành kho hàng đưa ra quyết định nhanh chóng.
- **Thứ Ba:**
  - Kết quả đạt được: Bảo mật thành công các route API backend, từ chối mọi truy cập có JWT hết hạn hoặc không hợp lệ.
  - Bài học: Sử dụng JWT giúp backend không phải truy vấn database liên tục để kiểm tra phiên làm việc trên mỗi request.
- **Thứ Tư:**
  - Kết quả đạt được: Tích hợp thành công mã OTP xác thực và bắt buộc điền khi người dùng đăng nhập.
  - Bài học: Xác thực 2FA là chốt chặn bảo mật trọng yếu để ngăn chặn truy cập trái phép kể cả khi mật khẩu bị rò rỉ.
- **Thứ Năm:**
  - Kết quả đạt được: Phân quyền thành công các chức năng: nhân viên chỉ được xem báo cáo kho, quản trị viên được kích hoạt huấn luyện mô hình.
  - Bài học: Phân quyền RBAC giúp bảo vệ tính toàn vẹn của dữ liệu và ngăn chặn nhân viên thông thường chạy các tác vụ tốn tài nguyên.
- **Thứ Sáu:**
  - Kết quả đạt được: Hiển thị biểu đồ dạng đường nét đứt biểu thị dữ liệu dự báo đè lên dữ liệu giao dịch thực tế trực quan.
  - Bài học: Biểu đồ trực quan hóa dữ liệu lịch sử kết hợp dự báo giúp nhà bán lẻ đưa ra chiến lược đặt hàng chính xác.
