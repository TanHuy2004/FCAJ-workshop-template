---
title: "Worklog Tuần 10"
date: 2026-06-28
weight: 1
chapter: false
pre: " <b> 1.10. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần:

* Thiết lập môi trường phát triển và xây dựng nền tảng backend cho dự án.
* Tìm hiểu kiến trúc hệ thống, cơ sở dữ liệu và quy trình phát triển phần mềm của dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Thiết lập môi trường phát triển.<br>- Cài đặt Docker Compose để khởi chạy PostgreSQL, Redis, LocalStack và pgAdmin.<br>- Kiểm tra kết nối cơ sở dữ liệu. | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 3 | - Thiết kế cơ sở dữ liệu PostgreSQL.<br>- Tạo các bảng dữ liệu chính.<br>- Kích hoạt các extension cần thiết và thiết lập cơ chế migration để quản lý cơ sở dữ liệu. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 4 | - Xây dựng bộ khung backend theo kiến trúc phân tầng với Express và ESModules.<br>- Tổ chức mã nguồn theo từng module và áp dụng quy ước đặt tên thống nhất.<br>- Tìm hiểu và triển khai Repository Harness, hoàn thành story **TB-HARNESS**. | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 5 | - Nghiên cứu kiến trúc dự án.<br>- Xây dựng cơ chế soft delete cho bảng nhà hàng.<br>- Bổ sung các trường phục vụ quản lý dữ liệu.<br>- Tìm hiểu mô hình phân quyền của hệ thống. | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6 | - Nghiên cứu thiết kế các bảng vai trò, phân quyền và quản lý trạng thái tài khoản.<br>- Tìm hiểu quy trình làm việc, coding convention và cấu trúc story packet.<br>- Thực hành phân tích story mẫu để chuẩn bị triển khai các tính năng tiếp theo. | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |

### Kết quả đạt được:

* Thiết lập thành công môi trường phát triển với Docker Compose và triển khai các dịch vụ PostgreSQL, Redis, LocalStack và pgAdmin.

* Thiết kế cơ sở dữ liệu PostgreSQL ban đầu, tạo các bảng chính, cấu hình extension và cơ chế migration để quản lý thay đổi cơ sở dữ liệu.

* Xây dựng bộ khung backend theo kiến trúc phân tầng với Express và ESModules, đồng thời triển khai Repository Harness và hoàn thành story **TB-HARNESS**.

* Hiểu kiến trúc dự án, triển khai cơ chế soft delete cho bảng nhà hàng và nghiên cứu mô hình phân quyền của hệ thống.

* Làm quen với coding convention, quy trình phát triển phần mềm và phương pháp phân tích story packet để chuẩn bị cho việc phát triển các tính năng tiếp theo.