---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 3:

* Hiểu và triển khai mô hình kết nối mạng Hybrid Cloud trên AWS.
* Thiết lập Amazon Web Services Transit Gateway để kết nối nhiều VPC.
* Cấu hình Hybrid DNS bằng Amazon Web Services Route 53 Resolver nhằm phân giải tên miền giữa AWS và môi trường nội bộ.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu khái niệm và chức năng của Transit Gateway. <br> - Tạo các VPC                                                                                             | 04/05/2026   | 04/05/2026      |<https://cloudjourney.awsstudygroup.com/>  <br> <https://www.youtube.com/@AWSStudyGroup/videos>  |
| 3   | - Tạo Transit Gateway <br> - Cấu hình ASN, DNS support <br>- Tạo Transit Gateway Attachments để kết nối các VPC. <br>- Tạo Transit Gateway Route Tables.                                          | 05/05/2026   | 05/05/2026      | <https://cloudjourney.awsstudygroup.com/>  <br> <https://www.youtube.com/@AWSStudyGroup/videos>  |
| 4   | - Cấu hình route table cho từng subnet. <br> - Thêm route từ các VPC đến Transit Gateway. <br> - Kiểm tra khả năng kết nối giữa các VPC bằng ping  | 06/05/2026   | 06/05/2026      | <https://cloudjourney.awsstudygroup.com/>   <br> <https://www.youtube.com/@AWSStudyGroup/videos>|
| 5   | - Khởi tạo hạ tầng bằng CloudFormation Templates. <br> - Cấu hình Security Group cho DNS, RDP và SSH. <br> - Tạo Route 53 Outbound Endpoint và Resolver Rules.                  | 07/05/2026   | 07/05/2026      | <https://cloudjourney.awsstudygroup.com/>  <br> <https://www.youtube.com/@AWSStudyGroup/videos> |
| 6   | - Tạo Route 53 Inbound Endpoints. <br> - Kiểm tra hoạt động của routing và DNS.e <br> - Dọn dẹp tài nguyên để tránh phát sinh chi phí: <br>&emsp; + Xóa Resolver Rules <br>&emsp; + Xóa Endpoints <br>&emsp; + Xóa Transit Gateway Attachments <br>&emsp; + Xóa Transit Gateway và Route Tables.                                                                                  | 08/05/2026   | 08/05/2026      | <https://cloudjourney.awsstudygroup.com/>  <br> <https://www.youtube.com/@AWSStudyGroup/videos> |


### Kết quả đạt được tuần 3:

* Triển khai thành công Amazon Web Services Transit Gateway để kết nối nhiều VPC trong cùng hệ thống mạng.

* Thiết lập routing giữa các VPC thông qua Transit Gateway và kiểm tra kết nối thành công bằng ping.

* Khởi tạo hạ tầng bằng CloudFormation Templates phục vụ mô hình Hybrid DNS.

* Thiết lập thành công Hybrid DNS bằng Amazon Web Services Route 53 Resolver.

* Tạo và cấu hình:

  * Route 53 Outbound Endpoint
  * Route 53 Inbound Endpoint
  * Resolver Rules

* Dọn dẹp tài nguyên sau khi hoàn thành bài lab để tránh phát sinh chi phí.


