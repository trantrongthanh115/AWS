---
title: "Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

**Mục tiêu tuần:**
- Khởi tạo hàm AWS Lambda viết bằng Python để sinh kết quả dự báo doanh số.
- Tải cấu hình mô hình động từ S3 vào môi trường thực thi của hàm serverless.
- Triển khai API Gateway để xuất các API dự báo dưới dạng REST API.
- Thiết lập lịch trình Amazon EventBridge để tự động hóa dự báo hàng ngày.
- Đánh giá luồng kích hoạt và ghi log hoạt động trong CloudWatch.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Tạo hàm `forecast-lambda` mới và gán các quyền IAM cho phép đọc file từ S3. | 15/6 |
| Thứ Ba | Lập trình logic cho hàm Lambda để tải mô hình `model.pkl` và thực thi suy luận dữ liệu. | 16/6 |
| Thứ Tư | Tích hợp API Gateway để ánh xạ các endpoint HTTP (ví dụ `/predict`) với hàm Lambda. | 17/6 |
| Thứ Năm | Cấu hình bộ lập lịch tự động Amazon EventBridge chạy định kỳ vào lúc 12:00 AM UTC mỗi ngày. | 18/6 |
| Thứ Sáu | Kiểm thử liên thông hệ thống suy luận không máy chủ và kiểm tra logs trên CloudWatch. | 19/6 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Hàm Lambda đã được khởi tạo thành công và cấu hình chính sách bảo mật phù hợp.
  - Bài học: Chỉ cấp quyền `s3:GetObject` cho Lambda thay vì toàn quyền giúp hạn chế rủi ro lộ lọt dữ liệu mô hình.
- **Thứ Ba:**
  - Kết quả đạt được: Logic dự báo hoạt động tốt, thời gian tải mô hình tối ưu.
  - Bài học: Tải file mô hình và import các thư viện bên ngoài hàm handler chính giúp giảm thiểu độ trễ khởi động lạnh (cold start).
- **Thứ Tư:**
  - Kết quả đạt được: Endpoint API được xuất bản thành công. Kiểm thử phản hồi JSON chính xác bằng cURL.
  - Bài học: API Gateway cung cấp giao diện quản lý API chuyên nghiệp, hỗ trợ cấu hình CORS và giới hạn số lượng request tự động.
- **Thứ Năm:**
  - Kết quả đạt được: Đăng ký thành công cron job trên EventBridge Scheduler.
  - Bài học: Sử dụng EventBridge Scheduler giúp chạy tác vụ định kỳ mà không cần duy trì một máy chủ cron truyền thống 24/7.
- **Thứ Sáu:**
  - Kết quả đạt được: Hệ thống tự động kích hoạt dự báo đúng giờ và ghi nhận kết quả lưu vào database thành công.
  - Bài học: Phân tích log của CloudWatch giúp xác định thời gian chạy thực tế của Lambda để tối ưu cấu hình RAM và timeout.
