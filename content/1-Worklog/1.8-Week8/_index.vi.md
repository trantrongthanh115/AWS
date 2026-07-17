---
title: "Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

**Mục tiêu tuần:**
- Khởi chạy một instance EC2 chuyên dụng cho các tác vụ huấn luyện mô hình Machine Learning.
- Viết script Python để truy xuất các bảng đặc trưng từ cơ sở dữ liệu `training-db`.
- Huấn luyện và đánh giá mô hình hồi quy dự báo nhu cầu bán hàng thời trang.
- Đo lường các chỉ số kiểm thử (MAE, RMSE) và xuất tham số mô hình.
- Tự động hóa quá trình đẩy mô hình đã huấn luyện lên lưu trữ tại Amazon S3.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai ( Lên văn phòng ) | Khởi chạy máy ảo `ML-Training-Server` trên EC2, cài đặt môi trường Python 3.10 và các trình điều khiển database. | 8/6 |
| Thứ Ba | Cài đặt các thư viện phục vụ học máy bao gồm Psycopg2, Pandas và Scikit-Learn vào môi trường ảo. | 9/6 |
| Thứ Tư | Viết mã nguồn `train.py` kết nối trực tiếp đến PostgreSQL `training-db` để đọc dữ liệu đặc trưng chuỗi thời gian. | 10/6 |
| Thứ Năm | Thực hiện chạy huấn luyện mô hình bằng thuật toán Random Forest Regressor, đo lường sai số MAE. | 11/6 |
| Thứ Sáu | Viết mã sử dụng thư viện boto3 để tự động lưu và tải file mô hình (`model.pkl`) lên bucket S3 bảo mật. | 12/6 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai ( Lên văn phòng ):**
  - Kết quả đạt được: Máy chủ huấn luyện đã sẵn sàng trong VPC.
  - Bài học: Tách biệt tài nguyên tính toán huấn luyện mô hình giúp tránh tình trạng cạn kiệt tài nguyên CPU trên các máy chủ ứng dụng chính.
- **Thứ Ba:**
  - Kết quả đạt được: Hoàn thành thiết lập môi trường, kiểm tra kết nối với DB driver thành công.
  - Bài học: Ràng buộc phiên bản thư viện trong file `requirements.txt` giúp tránh các lỗi không tương thích khi triển khai tự động.
- **Thứ Tư:**
  - Kết quả đạt được: Tối ưu các truy vấn đọc dữ liệu đặc trưng theo lô vào bộ nhớ đệm.
  - Bài học: Sử dụng các bộ lọc index theo thời gian giúp tăng tốc độ đọc dữ liệu và giảm thiểu tải cho database.
- **Thứ Năm:**
  - Kết quả đạt được: Mô hình huấn luyện thành công với sai số tuyệt đối trung bình (MAE) nằm trong ngưỡng sai số cho phép.
  - Bài học: Đánh giá mô hình trên tập kiểm thử (validation set) độc lập là bước bắt buộc để phát hiện hiện tượng quá khớp (overfitting).
- **Thứ Sáu:**
  - Kết quả đạt được: Xác nhận file mô hình đã được lưu trữ an toàn trên S3 và phân quyền cho phép các dịch vụ khác đọc dữ liệu.
  - Bài học: Lưu trữ mô hình trên S3 giúp các microservices hoặc hàm serverless có thể tải và sử dụng mô hình động mà không phụ thuộc lẫn nhau.
