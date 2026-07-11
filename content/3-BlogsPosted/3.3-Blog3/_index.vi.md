---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

# MCP không còn là tất cả trong kiến trúc Agentic AI

Khi nhắc đến AI Agent, nhiều người sẽ nghĩ ngay đến **Model Context Protocol (MCP)** – giao thức giúp Agent kết nối với các công cụ và nguồn dữ liệu. Tuy nhiên, trong bài viết mới về **Amazon Bedrock AgentCore**, AWS cho thấy bức tranh đầy đủ hơn với ba giao thức phục vụ ba mục đích khác nhau.

## Model Context Protocol (MCP)

MCP đóng vai trò là cầu nối giữa Agent và các công cụ như API, cơ sở dữ liệu, Amazon S3 hay các hệ thống nội bộ. Thay vì phải xây dựng tích hợp riêng cho từng mô hình AI, MCP mang đến một chuẩn giao tiếp thống nhất để Agent có thể khám phá và sử dụng các công cụ một cách linh hoạt.

## Agent-to-Agent (A2A)

Khi một Agent không còn đủ để xử lý toàn bộ quy trình nghiệp vụ, A2A cho phép nhiều Agent chuyên biệt phối hợp với nhau. Ví dụ, một Sales Agent có thể làm việc cùng Finance Agent hoặc Support Agent để hoàn thành một yêu cầu của người dùng. Cách tiếp cận này giúp hệ thống dễ mở rộng và phân tách trách nhiệm rõ ràng hơn.

## Agent-User Interaction (AG-UI)

Nếu MCP kết nối Agent với công cụ và A2A kết nối Agent với Agent thì AG-UI tập trung vào trải nghiệm người dùng. Thay vì chỉ phản hồi bằng văn bản, Agent có thể hiển thị bảng dữ liệu, biểu đồ, trạng thái xử lý hoặc các thành phần giao diện tương tác theo thời gian thực.

Có thể tóm tắt ngắn gọn như sau:

```text
MCP = Agent <-> Tools
A2A = Agent <-> Agent
AG-UI = Agent <-> User
```

Điểm mình thấy thú vị là AWS không chỉ tập trung vào việc xây dựng một AI Agent thông minh hơn, mà còn đang chuẩn hóa cách Agent kết nối với công cụ, cộng tác với các Agent khác và tương tác với người dùng. Đây có thể sẽ là nền tảng cho các hệ thống Multi-Agent trong môi trường doanh nghiệp, nơi mỗi Agent đảm nhận một vai trò riêng nhưng vẫn phối hợp thành một quy trình thống nhất.

## Tài liệu tham khảo

* Đọc bài viết gốc của AWS tại: https://aws.amazon.com/vi/blogs/machine-learning/build-generative-ui-for-ai-agents-on-amazon-bedrock-agentcore-with-the-ag-ui-protocol/
