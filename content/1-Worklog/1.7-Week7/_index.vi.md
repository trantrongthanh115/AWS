---
title: "Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

**Mục tiêu tuần:**
- Xây dựng quy trình tự động hóa ETL dữ liệu lớn sử dụng AWS Glue.
- Tạo IAM Service Role cho phép AWS Glue truy cập tài nguyên VPC.
- Cấu hình và triển khai tác vụ Glue Job `Raw Ingestion` để nạp dữ liệu giao dịch vào RDS.
- Cấu hình và triển khai tác vụ Glue Job `Feature Engineering` để tính toán biến trễ (lags) và biến thống kê.
- Theo dõi trạng thái thực thi của các tác vụ ETL trên giao diện điều khiển và qua CloudWatch.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai ( Lên văn phòng) | Tạo IAM Service Role cho AWS Glue với đầy đủ quyền đọc/ghi S3, kết nối RDS và ghi log vào CloudWatch. | 1/6 |
| Thứ Ba | Tạo các bucket Amazon S3 đóng vai trò là "landing zone" lưu trữ các file giao dịch CSV thô. | 2/6 |
| Thứ Tư | Cấu hình Glue Job `Raw Ingestion`, viết mã nguồn PySpark để phân tách và nạp file CSV vào database `fashion-rds`. | 3/6 |
| Thứ Năm | Cấu hình Glue Job `Feature Engineering`, viết mã nguồn PySpark tính toán các đặc trưng chuỗi thời gian (trễ 7 ngày, trung bình trượt). | 4/6 |
| Thứ Sáu | Chạy thử nghiệm toàn bộ pipeline ETL từ console và xác minh dữ liệu đặc trưng đã được ghi vào database. | 5/6 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai ( Lên văn phòng ):**
  - Kết quả đạt được: Tạo xong IAM Role cho AWS Glue. Thiết lập cấu hình mạng VPC Connection thành công.
  - Bài học: Tác vụ AWS Glue cần các quyền mạng cụ thể để có thể tự động tạo Network Interface kết nối vào VPC riêng tư của RDS.
- **Thứ Ba:**
  - Kết quả đạt được: Buckets S3 sẵn sàng hoạt động. Đã tải lên các file dữ liệu giao dịch mẫu.
  - Bài học: Sử dụng S3 làm Landing Zone giúp tách biệt lưu trữ dữ liệu thô khỏi các cơ sở dữ liệu xử lý trực tuyến.
- **Thứ Tư:**
  - Kết quả đạt được: Chạy thành công tác vụ nạp dữ liệu, toàn bộ dữ liệu lịch sử giao dịch đã nằm trong database `fashion-rds`.
  - Bài học: Sử dụng JDBC connector trong Spark giúp tối ưu tốc độ ghi dữ liệu lớn vào cơ sở dữ liệu quan hệ.
- **Thứ Năm:**
  - Kết quả đạt được: Cơ sở dữ liệu `training-db` đã được cập nhật đầy đủ các trường đặc trưng chuỗi thời gian.
  - Bài học: Thực hiện kỹ nghệ đặc trưng dữ liệu lớn ngay trên Spark giúp giải phóng tài nguyên CPU cho máy chủ chạy mô hình ML.
- **Thứ Sáu:**
  - Kết quả đạt được: Các Glue jobs kết thúc với trạng thái Succeeded. Hệ thống ghi nhận kết quả xử lý chính xác.
  - Bài học: Giám sát log trong CloudWatch là cách tốt nhất để phát hiện các lỗi tràn bộ nhớ (OOM) hoặc kết nối mạng bị từ chối của Spark.
