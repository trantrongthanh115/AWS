---
title: "Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

**Mục tiêu tuần:**
- Nghiên cứu yêu cầu dự án Ứng dụng Web bán lẻ thời trang & Pipeline Machine Learning.
- Nắm rõ kiến trúc hệ thống tổng quan và mô hình kiến trúc Decoupled.
- Thiết kế phân bổ sơ đồ mạng subnet và phân vùng bảo mật qua Security Groups.
- Định nghĩa cấu trúc các bảng cơ sở dữ liệu và luồng đi của dữ liệu dự báo.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Phân tích bài toán kinh doanh về tối ưu hóa hàng tồn kho và dự báo nhu cầu mua sắm sản phẩm thời trang. | 4/5 |
| Thứ Ba | Nghiên cứu Sơ đồ kiến trúc hệ thống, phân chia rõ ranh giới giữa Web Application & APIs và ML Pipeline. | 5/5 |
| Thứ Tư | Lập bản đồ cấu trúc mạng VPC bao gồm các subnets công khai/riêng tư, CloudFront, ALB và vùng cơ sở dữ liệu an toàn. | 6/5 |
| Thứ Năm | Thiết kế lược đồ cơ sở dữ liệu quan hệ cho dữ liệu giao dịch (`fashiondb`) và đặc trưng huấn luyện (`trainingdb`). | 7/5 |
| Thứ Sáu | Khởi tạo cấu trúc mã nguồn dự án và lên lộ trình triển khai chi tiết cho 10 giai đoạn của workshop. | 8/5 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Hoàn thành tài liệu phân tích nghiệp vụ, xác định việc sử dụng dữ liệu chuỗi thời gian để dự báo doanh số.
  - Bài học: Việc thấu hiểu bài toán nghiệp vụ giúp định hướng chính xác các quyết định thiết kế kiến trúc hạ tầng kỹ thuật.
- **Thứ Ba:**
  - Kết quả đạt được: Thống nhất mô hình kiến trúc, tách biệt giao diện tương tác người dùng khỏi các tác vụ xử lý dữ liệu nặng.
  - Lesson: Kiến trúc Decoupled giúp các tác vụ huấn luyện ML không làm gián đoạn hay ảnh hưởng hiệu năng của Web bán lẻ.
- **Thứ Tư:**
  - Kết quả đạt được: Phác thảo ranh giới bảo mật mạng, quy định các máy chủ web chỉ nhận traffic trung chuyển từ Load Balancer.
  - Bài học: Đưa máy chủ vào subnet riêng tư và giới hạn cổng truy cập là phương pháp bảo mật hạ tầng mạng cơ bản.
- **Thứ Năm:**
  - Kết quả đạt được: Hoàn thiện thiết kế schema các bảng bao gồm thông tin cửa hàng, sản phẩm, giao dịch và các biến trễ thời gian.
  - Bài học: Tách biệt bảng cơ sở dữ liệu giao dịch và bảng phân tích đặc trưng giúp tránh xung đột tài nguyên đọc/ghi.
- **Thứ Sáu:**
  - Kết quả đạt được: Cấu trúc thư mục dự án đã sẵn sàng, phân chia rõ ràng các module dùng chung và module chức năng.
  - Bài học: Quy hoạch cấu trúc thư mục rõ ràng giúp việc phát triển song song của các thành viên không bị chồng chéo.
