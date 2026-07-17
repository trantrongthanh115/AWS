---
title: "Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

**Mục tiêu tuần:**
- Triển khai hệ thống giám sát chi phí đa lớp bao gồm ngân sách 3 tầng và cảnh báo thanh toán CloudWatch.
- Kích hoạt tính năng AWS Cost Anomaly Detection và thiết lập quy tắc gắn thẻ tài nguyên chuẩn hóa.
- Soạn thảo và thử nghiệm các lệnh CLI để kiểm tra và dọn dẹp các tài nguyên đám mây có chi phí cao.
- Nghiên cứu các mô hình kiến trúc đám mây cốt lõi, hạ tầng toàn cầu và các nguyên tắc bảo mật.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Cấu hình hạn mức ngân sách 3 tầng (Hàng tháng, Cảnh báo, Bảo vệ hàng ngày) và thiết lập Billing Alarms trong CloudWatch qua SNS. | 27/4 |
| Thứ Ba | Kích hoạt AWS Cost Anomaly Detection (ngưỡng tác động $5 hàng ngày) và thống nhất quy chuẩn gắn thẻ tài nguyên (`Project`, `Environment`, `Author`). | 28/4 |
| Thứ Tư | Thực hành các lệnh AWS CLI để kiểm kê tài nguyên: tìm kiếm EC2/RDS đang chạy, ổ đĩa EBS độc lập và Elastic IP chưa liên kết. | 29/4 |
| Thứ Năm | Nghiên cứu đặc tính điện toán đám mây (elasticity, OpEx vs CapEx), so sánh các mô hình dịch vụ (IaaS, PaaS, SaaS) và hạ tầng toàn cầu (Regions, AZs, Edge). | 30/4 |
| Thứ Sáu | Đánh giá Mô hình trách nhiệm chung AWS, các phương pháp bảo mật IAM tối ưu (least privilege, MFA, JSON policies) và đặc tính của S3. | 1/5 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Ngân sách cảnh báo $20 và ngân sách bảo vệ hàng ngày $5 đã hoạt động. CloudWatch alarms được liên kết để gửi email/SMS cảnh báo.
  - Bài học: Giám sát đa lớp giúp phát hiện sớm bất thường, trong đó cảnh báo ngày giúp ngăn chặn chi tiêu ngoài tầm kiểm soát trong vòng 24 giờ.
- **Thứ Ba:**
  - Kết quả đạt được: Kích hoạt thành công bộ giám sát bất thường dựa trên máy học. Áp dụng gắn thẻ cho các tài nguyên EC2 và S3 đang thử nghiệm.
  - Bài học: Gắn thẻ tài nguyên là bắt buộc để phân bổ chi phí trong Cost Explorer, giúp dễ dàng lọc và tìm kiếm nguồn phát sinh chi phí.
- **Thứ Tư:**
  - Kết quả đạt được: Chạy thành công các kịch bản CLI sử dụng lệnh `aws ec2` và `aws rds` để liệt kê các tài nguyên đang hoạt động hoặc bị bỏ quên.
  - Bài học: Sử dụng CLI và chuẩn bị sẵn quy trình Teardown khẩn cấp là kỹ năng sống còn để kiểm soát chi phí tối ưu trên cloud.
- **Thứ Năm:**
  - Kết quả đạt được: Hoàn thành tài liệu phân loại các dịch vụ AWS tương ứng với các mô hình IaaS, PaaS và SaaS.
  - Bài học: Việc triển khai ứng dụng trên nhiều Availability Zones (AZs) khác nhau giúp đảm bảo tính sẵn sàng cao và khả năng chống chịu lỗi.
- **Thứ Sáu:**
  - Kết quả đạt được: Thiết lập thành công các IAM policies tùy chỉnh viết bằng JSON tuân thủ chặt chẽ nguyên lý phân quyền tối thiểu.
  - Bài học: Bảo mật trong đám mây (cấu hình OS, Security Groups, IAM credentials) thuộc trách nhiệm trực tiếp của người dùng.
