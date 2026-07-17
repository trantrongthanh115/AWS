---
title: "Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

**Mục tiêu tuần:**
- Tiến hành kiểm thử hệ thống đầu cuối (E2E) trên toàn bộ cổng thông tin bán lẻ.
- Quay video demo hoạt động của dự án thực tế và tổng hợp hình ảnh báo cáo.
- Thu hồi và xóa bỏ toàn bộ các máy ảo EC2, ASG, Target Group và Load Balancer.
- Giải phóng các cụm cơ sở dữ liệu RDS PostgreSQL và xóa các nhóm subnet VPC.
- Làm sạch và xóa các S3 buckets, Glue jobs, và hàm Lambda để hoàn tất dọn dẹp tài nguyên.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Kiểm thử toàn bộ các kịch bản người dùng (Admin, Manager, Associate) và kiểm tra tính chính xác của dữ liệu dự báo. | 6/7 |
| Thứ Ba | Tiến hành quay video demo ứng dụng chạy thực tế và tải lên thư mục lưu trữ chia sẻ. | 7/7 |
| Thứ Tư | Dọn dẹp EC2: Xóa các instance máy ảo, xóa Target Groups, tắt ASG và hủy cấu hình Load Balancer. | 8/7 |
| Thứ Năm | Dọn dẹp RDS: Tiến hành xóa các instance cơ sở dữ liệu (`fashion-rds`, `training-db`) và giải phóng subnet groups. | 9/7 |
| Thứ Sáu | Làm sạch và xóa các S3 buckets, Glue ETL jobs, hàm Lambda và hoàn thiện báo cáo thực tập cuối kỳ. | 10/7 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Đảm bảo các luồng phân quyền và hiển thị biểu đồ dự báo hoạt động hoàn hảo không phát sinh lỗi.
  - Bài học: Kiểm thử tích hợp hệ thống là bắt buộc để đảm bảo các hệ thống decoupled hoạt động ăn khớp trước khi tắt dự án.
- **Thứ Ba:**
  - Kết quả đạt được: Hoàn thành video demo chạy thực tế ứng dụng phục vụ báo cáo.
  - Bài học: Quay video ghi nhận kết quả chạy là minh chứng trực quan nhất cho sự thành công của hệ thống.
- **Thứ Tư:**
  - Kết quả đạt được: Toàn bộ tài nguyên tính toán và cân bằng tải đã được xóa bỏ, dừng tính phí.
  - Bài học: Tắt Auto Scaling Group trước khi xóa instance là nguyên tắc bắt buộc để tránh ASG tự động tạo máy ảo thay thế.
- **Thứ Năm:**
  - Kết quả đạt được: Giải phóng các cluster RDS thành công, chọn không lưu snapshot để tránh phát sinh thêm phí lưu trữ.
  - Bài học: Cơ sở dữ liệu RDS sẽ liên tục tính phí dung lượng ổ cứng (EBS) đi kèm nếu không được xóa triệt để.
- **Thứ Sáu:**
  - Kết quả đạt được: Tài khoản AWS đã sạch tài nguyên thực hành, không phát sinh chi phí phát sinh. Hoàn thành báo cáo tự đánh giá.
  - Bài học: Thực hành dọn dẹp hạ tầng gọn gàng là thói quen FinOps cơ bản giúp bảo toàn lượng credit được cấp.
