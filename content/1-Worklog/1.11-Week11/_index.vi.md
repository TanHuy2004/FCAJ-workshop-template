---
title: "Worklog Tuần 11"
date: 2026-07-05
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 11:

* Bổ sung kiểm thử cho cơ chế xác thực JWT và luồng đăng nhập người dùng.
* Xây dựng dịch vụ kiểm tra khoảng cách GPS phục vụ chống gian lận.
* Hoàn thiện cấu hình anti-fraud, test helper và CI để tự động chạy migration cùng bộ test.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Viết unit test cho **CognitoIdentityProvider** để kiểm tra các trường hợp xác thực JWT.<br>- Tạo helper sinh JWT bằng cặp khóa RSA trong bộ nhớ để phục vụ test mà không cần kết nối Cognito.<br>- Kiểm tra các tình huống token hợp lệ, token không hợp lệ và dữ liệu xác thực không đúng. | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 3 | - Viết integration test cho chức năng đăng nhập trên Express.<br>- Kiểm tra luồng lấy thông tin người dùng sau khi đăng nhập.<br>- Sử dụng **trusted-local header** để giả lập người dùng trong môi trường test. | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 4 | - Bổ sung integration test cho các trường hợp người dùng hợp lệ, tài khoản bị khóa **SUSPENDED** và request không có token.<br>- Cải thiện test helper để tạo dữ liệu test thuận tiện và linh hoạt hơn.<br>- Đảm bảo dữ liệu test có thể tái sử dụng cho nhiều kịch bản kiểm thử. | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 5 | - Xây dựng service tính khoảng cách GPS bằng công thức **Haversine**.<br>- Trả về khoảng cách giữa người dùng và nhà hàng, đồng thời kiểm tra khoảng cách có nằm trong ngưỡng cho phép hay không.<br>- Tạo file cấu hình **antiFraud.js** để quản lý các tham số chống gian lận và cho phép cấu hình ngưỡng khoảng cách GPS thông qua biến môi trường. | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6 | - Bổ sung kiểm tra dữ liệu đầu vào hợp lệ cho GPS service.<br>- Viết unit test cho GPS service với các trường hợp khoảng cách bằng 0, trong ngưỡng, ngoài ngưỡng, đúng ngưỡng và dữ liệu đầu vào không hợp lệ.<br>- Cập nhật GitHub Actions để tự động chạy migration cơ sở dữ liệu và bộ test Vitest; chạy toàn bộ unit test thành công. | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/@AWSStudyGroup/videos> |

### Kết quả đạt được tuần 11:

* Hoàn thành unit test cho **CognitoIdentityProvider**, bao phủ các trường hợp xác thực JWT quan trọng và sử dụng helper sinh JWT bằng RSA trong bộ nhớ.

* Hoàn thành integration test cho chức năng đăng nhập và lấy thông tin người dùng trên Express, bao gồm người dùng hợp lệ, tài khoản **SUSPENDED** và request không có token.

* Xây dựng thành công GPS service sử dụng công thức **Haversine** để tính khoảng cách giữa người dùng và nhà hàng, đồng thời kiểm tra khoảng cách theo ngưỡng cho phép.

* Tạo file cấu hình **antiFraud.js** để quản lý tham số chống gian lận và hỗ trợ cấu hình ngưỡng khoảng cách GPS thông qua biến môi trường.

* Bổ sung unit test cho GPS service với nhiều kịch bản khác nhau và kiểm tra dữ liệu đầu vào không hợp lệ.

* Cập nhật GitHub Actions để tự động chạy migration cơ sở dữ liệu và bộ test Vitest, đồng thời cải thiện test helper giúp việc tạo dữ liệu test thuận tiện hơn.
