---
title: "Worklog Tuần 12"
date: 2026-07-12
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 12:

* Hoàn thiện các chức năng backend liên quan đến xử lý hóa đơn, upload ảnh lên Amazon S3 và tích hợp hàng đợi OCR.
* Phát triển, kiểm thử các API review và các chức năng tìm kiếm, lọc nhà hàng trong Phase 3.
* Hoàn thiện giao diện ứng dụng mobile, bao gồm đăng nhập với Amazon Cognito, Home, Thông báo, Favorites, Splash Screen và luồng nhập thông tin người dùng mới.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tham gia phát triển module xử lý hóa đơn phía backend.<br>- Hỗ trợ xây dựng service upload ảnh lên **Amazon S3** và tích hợp với hàng đợi xử lý **OCR**.<br>- Bổ sung test case cho các trường hợp upload thành công, upload thất bại và lỗi trong quá trình xác minh hóa đơn. | 13/07/2026 | 13/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 3 | - Hỗ trợ phát triển các API liên quan đến chức năng review.<br>- Xây dựng integration test kiểm tra toàn bộ luồng từ khi người dùng tạo review đến khi hệ thống xác minh và trả kết quả.<br>- Kiểm tra các trường hợp dữ liệu hợp lệ, dữ liệu không hợp lệ và lỗi phát sinh trong quá trình xử lý review. | 14/07/2026 | 14/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 4 | - Tham gia phát triển tính năng tìm kiếm và lọc nhà hàng cho **Phase 3**.<br>- Hỗ trợ viết integration test cho chức năng xem danh sách, xem chi tiết và tìm kiếm nhà hàng trên môi trường local.<br>- Rà soát kết quả trả về để đảm bảo dữ liệu phù hợp với điều kiện tìm kiếm và bộ lọc. | 15/07/2026 | 15/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 5 | - Tham gia phát triển giao diện ứng dụng mobile.<br>- Xây dựng màn hình đăng nhập tích hợp với **Amazon Cognito**, xử lý lỗi đăng nhập và điều hướng sau khi xác thực thành công.<br>- Hỗ trợ phát triển màn hình **Home**, tab **Thông báo** và màn hình nhập thông tin cho người dùng mới sau khi đăng ký. | 16/07/2026 | 16/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6 | - Phối hợp với thành viên backend để cập nhật luồng lưu thông tin hồ sơ người dùng phù hợp với quy trình đăng ký mới.<br>- Chỉnh sửa và hoàn thiện giao diện các màn hình **Favorites** và **Splash Screen**; cập nhật icon ứng dụng và điều chỉnh giao diện theo thiết kế chung.<br>- Hỗ trợ phát hiện, khắc phục lỗi trong giai đoạn kiểm thử cuối; rà soát chức năng, refactor và dọn dẹp mã nguồn để chuẩn bị kết thúc đợt thực tập. | 17/07/2026 | 17/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |

### Kết quả đạt được tuần 12:

* Tham gia hoàn thiện module xử lý hóa đơn phía backend, bao gồm service upload ảnh lên **Amazon S3** và tích hợp với hàng đợi xử lý **OCR**.

* Bổ sung các test case cho chức năng upload và xác minh hóa đơn, bao phủ các trường hợp upload thành công, upload thất bại và lỗi trong quá trình xác minh.

* Hỗ trợ phát triển các API review và xây dựng integration test kiểm tra luồng tạo review, xác minh và trả kết quả cho người dùng.

* Tham gia phát triển tính năng tìm kiếm, lọc nhà hàng cho **Phase 3** và bổ sung integration test cho chức năng xem danh sách, xem chi tiết và tìm kiếm nhà hàng trên môi trường local.

* Hoàn thiện một số màn hình mobile như đăng nhập với **Amazon Cognito**, **Home**, tab **Thông báo**, màn hình nhập thông tin người dùng mới, **Favorites** và **Splash Screen**.

* Cập nhật icon ứng dụng, điều chỉnh giao diện theo thiết kế chung và phối hợp xử lý các lỗi phát sinh trong giai đoạn kiểm thử cuối.

* Rà soát chức năng, refactor và dọn dẹp mã nguồn để chuẩn bị cho việc kết thúc đợt thực tập.
