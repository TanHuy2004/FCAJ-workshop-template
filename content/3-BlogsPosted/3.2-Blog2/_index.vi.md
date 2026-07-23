---
title: "Blog 2"
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---
# AgentCore Harness: Từ ý tưởng đến một AI Agent hoạt động chỉ với hai API

Khi xây dựng một AI Agent, gọi mô hình ngôn ngữ thường không phải phần khó nhất. Phần phức tạp nằm ở agent loop, kết nối công cụ, quản lý bộ nhớ, trạng thái phiên, danh tính, observability và môi trường thực thi an toàn.

**Amazon Bedrock AgentCore Harness** đóng gói các thành phần này thành một dịch vụ được quản lý, giúp developer tập trung vào logic nghiệp vụ thay vì tự xây dựng toàn bộ lớp orchestration và hạ tầng.

---

## 1. Hai API cốt lõi

Một agent có thể được đưa vào hoạt động thông qua hai API chính:

* **CreateHarness:** Định nghĩa model, system prompt, tools, skills, memory và giới hạn thực thi của agent.
* **InvokeHarness:** Gửi yêu cầu, chạy agent và nhận kết quả trả về.

Sau khi được định nghĩa, agent có thể tự phân tích yêu cầu, lựa chọn công cụ phù hợp, thực thi công cụ và phản hồi cho ứng dụng. AgentCore quản lý vòng lặp xử lý phía sau.

---

## 2. AgentCore Harness quản lý những gì?

Mỗi phiên làm việc có thể chạy trong môi trường cô lập với filesystem và shell riêng. Harness đồng thời cung cấp các thành phần quan trọng như:

* Memory và trạng thái hội thoại giữa các phiên.
* Identity, quyền truy cập và observability qua Amazon CloudWatch.
* AgentCore Gateway để truy cập API, AWS Lambda và công cụ được quản trị.
* MCP server, AgentCore Browser và AgentCore Code Interpreter.
* Khả năng lựa chọn hoặc thay đổi model mà không gắn logic agent vào một model duy nhất.

Các công cụ chủ yếu được khai báo bằng cấu hình, giúp giảm lượng glue code mà đội phát triển phải duy trì.

---

## 3. Ví dụ AWS Support Agent

Một AWS Support Agent có thể được cấu hình để:

* Đọc log từ Amazon CloudWatch.
* Tìm kiếm tài liệu AWS.
* Phân tích nguyên nhân lỗi và đề xuất hướng xử lý.
* Tạo support case khi cần thiết.

Thay vì tự viết agent loop, xử lý tool calling, xây container và triển khai runtime, developer chủ yếu định nghĩa model, hướng dẫn hoạt động cùng các công cụ mà agent được phép sử dụng.

---

## 4. Harness hay Runtime?

**AgentCore Harness** phù hợp khi agent hoạt động theo luồng phổ biến: nhận yêu cầu, suy luận, gọi công cụ và trả kết quả. Cách này ưu tiên tốc độ phát triển và sự đơn giản.

**AgentCore Runtime** phù hợp hơn khi cần tự chọn framework, xây dựng graph hoặc workflow đặc biệt, can thiệp sâu vào orchestration hay sử dụng logic và hook tùy chỉnh.

Nói ngắn gọn: **Harness ưu tiên tốc độ**, còn **Runtime ưu tiên khả năng tùy chỉnh**.

---

## 5. Kết luận

AgentCore Harness không có nghĩa là xây AI Agent hoàn toàn không cần code. Developer vẫn phải thiết kế prompt, tools, dữ liệu, IAM role và cơ chế kiểm soát hành động. Tuy nhiên, khi orchestration, memory, identity, môi trường thực thi và observability được cung cấp dưới dạng dịch vụ quản lý, đội phát triển có thể dành nhiều thời gian hơn cho bài toán thực tế.

Thay vì tự xây dựng phần “khung xương” của agent, chúng ta có thể bắt đầu với **CreateHarness** để định nghĩa và **InvokeHarness** để đưa agent vào hoạt động.

---

## Tham khảo thêm

Đọc bài viết chính thức của AWS:
[Amazon Bedrock AgentCore harness is now generally available: Go from idea to production-grade agent in minutes](https://aws.amazon.com/blogs/machine-learning/amazon-bedrock-agentcore-harness-is-now-generally-available-go-from-idea-to-production-grade-agent-in-minutes/)

**#AWS #AmazonBedrock #AgentCore #AgenticAI #GenerativeAI**