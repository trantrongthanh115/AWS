---
title: "Các bài blogs đã dịch"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---



Trong quá trình thực tập, mình đã dịch và tóm tắt 5 bài blog kỹ thuật của AWS xoay quanh các chủ đề về data engineering, lưu trữ đám mây và quản lý cơ sở dữ liệu. Mỗi bài được chọn vì có sự liên quan trực tiếp đến các công nghệ và dịch vụ mình làm việc trong suốt chương trình.

---

### [Blog 1 - Xây dựng Pipeline CDC Thời Gian Thực: Từ Amazon Aurora sang Amazon S3 Tables với Debezium và Firehose](3.1-Blog1/)

Blog này hướng dẫn cách xây dựng pipeline Change Data Capture (CDC) thời gian thực, đưa dữ liệu từ Amazon Aurora PostgreSQL sang Amazon S3 Tables dưới định dạng Apache Iceberg. Bài viết giải thích tại sao việc tách biệt workload OLTP và OLAP lại quan trọng, cách Debezium trên MSK Connect bắt các thay đổi từ WAL của PostgreSQL mà hầu như không ảnh hưởng hiệu năng, và cách AWS Lambda đóng vai trò tầng chuyển đổi ánh xạ các mã thao tác Debezium (c/u/d) sang các hành động insert/update/delete của Firehose. Bài viết cũng giới thiệu cách S3 Tables tự động hóa việc quản lý snapshot và nén dữ liệu, cho phép phân tích gần như thời gian thực mà không ảnh hưởng đến cơ sở dữ liệu nguồn.

---

### [Blog 2 - Quản lý dữ liệu trên AWS: Chấm dứt nỗi lo "phân quyền hai nơi" cho S3 và Lake Formation](3.2-Blog2/)

Blog này giới thiệu một tính năng mới của AWS cho phép Data Scientist và ML Engineer truy cập trực tiếp các file thô trên S3 bằng chính quyền hạn AWS Lake Formation hiện có - không cần duy trì song song chính sách IAM/S3 bucket riêng biệt bên cạnh quyền bảng Lake Formation. Bài viết trình bày cách API `GetTemporaryDataLocationCredentials()` mới hoạt động, cách plugin Java tự động hóa việc cấp credentials, và lý do tại sao đây là bước đột phá cho các pipeline ML và Generative AI cần truy cập trực tiếp vào data lake có quản trị.

---

### [Blog 3 - Di chuyển dữ liệu và tiết kiệm chi phí ở quy mô lớn với Amazon S3 File Gateway](3.3-Blog3/)

Blog này giải quyết một vấn đề phổ biến nhưng thường bị bỏ qua trong các dự án chuyển đổi đám mây: khi file được di chuyển từ hệ thống on-premises lên Amazon S3 thông qua S3 File Gateway, timestamp gốc của file bị reset - làm phá vỡ các S3 Lifecycle Policy vốn dựa vào tuổi thật của file. Bài viết trình bày giải pháp tự động hóa kết hợp Robocopy, S3 File Gateway và AWS Lambda để bảo toàn metadata gốc (timestamp, quyền NTFS) và tự động chuyển file vào lớp lưu trữ chi phí thấp phù hợp (như Glacier Deep Archive) dựa trên tuổi thật - tối ưu chi phí lưu trữ ở quy mô lớn trong khi vẫn hỗ trợ truy cập hybrid cloud qua SMB và NFS.