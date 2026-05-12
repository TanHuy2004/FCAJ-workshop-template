---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}


### Mục tiêu tuần 2:

* Hiểu cách hoạt động của VPC Peering trong Amazon Web Services.
* Biết cách kết nối hai VPC để các tài nguyên có thể giao tiếp nội bộ với nhau.
* Hiểu và cấu hình các thành phần mạng cơ bản.
* Thực hành tạo và cấu hình EC2 Instance để kiểm tra kết nối mạng giữa các VPC.
### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Đọc và hiểu cách kết nối hai VPC khác nhau <br>&emsp; + Tạo 2 VPC khác nhau tập <br>&emsp; + Tạo mạng con <br>&emsp; + Tạo cổng internet <br>&emsp; + Tạo bảng định tuyến                                                                                            | 27/04/2026   | 27/04/2026      | <https://cloudjourney.awsstudygroup.com/> <br> <https://www.youtube.com/watch?v=bOIq3-2D17Y> |
| 3   | - Tạo Security Group <br> - Tìm hiểu inbound rules và outbound rules <br> - Bảo mật EC2 bằng Security Group                                           | 28/04/2026   | 28/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Tạo máy chủ EC2 <br> - Thiết lập địa chỉ IP tĩnh <br> - Tạo cổng NAT <br> - Kiểm tra ping amazon.com | 29/04/2026   | 29/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Cập nhật Network ACL: (NACLs) <br>&emsp; + Sửa inbound rule <br>&emsp; + Lưu lại phần chỉnh sửa                  | 30/04/2026   | 30/04/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Tạo Peering Connection - Cấu hình bảng - Kích hoạt CROSS-PEER DNS                                                                                       | 1/05/2026   | 1/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 2:

* Hiểu được cách thiết lập và kết nối giữa hai VPC khác nhau trong Amazon Web Services.

* Thực hiện thành công:
  * Tạo VPC
  * Tạo Subnet
  * Tạo Internet Gateway
  * Cấu hình Route Table

* Tạo và cấu hình Security Group của EC2 Instance.
* Triển khai thành công EC2 Instance và cấu hình địa chỉ IP tĩnh cho máy chủ.

* Thiết lập NAT Gateway để EC2 trong private subnet truy cập Internet.
* Kiểm tra kết nối mạng thành công ping đến amazon.com.
* Kích hoạt Cross-Peer DNS giúp các EC2 Instance có thể phân giải tên miền nội bộ giữa các VPC.
* Hiểu được quy trình triển khai, cấu hình, bảo mật và quản lý hệ thống mạng cơ bản trên AWS.

