---
title: "Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

**Mục tiêu tuần:**
- Đăng ký thành công tài khoản AWS cá nhân và nhận $100 credit ban đầu từ chương trình.
- Thực hiện 5 bài thực hành hướng dẫn trên AWS Console để kiếm thêm $100 credit khuyến mại ($20 cho mỗi bài hoàn thành).
- Trực tiếp làm quen với giao diện và cách hoạt động của 5 dịch vụ AWS cơ bản: EC2, Bedrock, Budgets, Lambda, và RDS.
- Hiểu rõ nguyên tắc quản lý chi phí, cấu hình bảo mật và quy trình dọn dẹp tài nguyên sau khi thực hành.

**Các công việc cần triển khai trong tuần này:**

| Thứ | Công việc | Ngày |
|---|---|---|
| Thứ Hai | Đăng ký tài khoản & Cấu hình bảo mật. Kích hoạt xác thực đa lớp (MFA) cho tài khoản root, tạo tài khoản IAM Admin và nhóm người dùng. | 20/4 |
| Thứ Ba | Task 1: Khởi tạo, kiểm tra trạng thái hoạt động và xóa máy ảo thử nghiệm Amazon EC2 (`FCA-Test-Server`) sử dụng Key Pair tự tạo. | 21/4 |
| Thứ Tư | Task 2: Yêu cầu quyền truy cập mô hình Claude 3 Haiku trong Amazon Bedrock và thực hành tạo prompt trên giao diện Text Playground. | 22/4 |
| Thứ Năm | Task 3: Thiết lập hạn mức cảnh báo ngân sách $20 trong AWS Budgets, cấu hình thông báo tự động khi chạm ngưỡng 80% chi phí. | 23/4 |
| Thứ Sáu | Task 4 & 5: Triển khai hàm Lambda Serverless qua blueprint, cung cấp cơ sở dữ liệu PostgreSQL trên RDS và dọn dẹp toàn bộ tài nguyên. | 24/4 |

**Kết quả đạt được trong tuần là gì:**
- **Thứ Hai:**
  - Kết quả đạt được: Kích hoạt tài khoản AWS thành công và cấu hình bảo mật tài khoản root bằng MFA. Tạo nhóm người dùng IAM với quyền admin phân quyền chi tiết.
  - Bài học: Việc bảo vệ tài khoản root và phân quyền chi tiết cho người dùng IAM là nguyên tắc bảo mật tối quan trọng trên cloud.
- **Thứ Ba:**
  - Kết quả đạt được: Khởi chạy thành công máy chủ t3.micro, kiểm tra trạng thái hoạt động và terminate máy chủ an toàn.
  - Bài học: Quá trình khởi tạo tài nguyên rất nhanh chóng nhưng sẽ tính phí liên tục. Cần rèn luyện thói quen terminate tài nguyên thực hành ngay lập tức.
- **Thứ Tư:**
  - Kết quả đạt được: Yêu cầu mở khóa thành công mô hình Claude 3 Haiku và nhận phản hồi văn bản trong Text Playground.
  - Bài học: Quyền truy cập mô hình AI được AWS quản lý nghiêm ngặt nhằm tuân thủ chính sách AI có trách nhiệm. Các dịch vụ Managed AI giúp trừu tượng hóa hạ tầng.
- **Thứ Năm:**
  - Kết quả đạt được: Tạo cảnh báo chi phí thành công, cấu hình nhận thông báo tự động qua Email thông qua Amazon SNS.
  - Bài học: Thiết lập ngân sách là bước bảo vệ tài khoản đầu tiên, giúp cảnh báo kịp thời trước khi chi phí tích lũy quá lớn.
- **Thứ Sáu:**
  - Kết quả đạt được: Khởi chạy hàm Lambda thành công thông qua blueprint, chạy thử Function URL, khởi tạo database PostgreSQL trên RDS và dọn dẹp an toàn.
  - Bài học: Serverless tự động co giãn và giữ chi phí ở mức $0 khi không hoạt động. RDS PostgreSQL yêu cầu xóa các instance con trước khi xóa cụm database.
