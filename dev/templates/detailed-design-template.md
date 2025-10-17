---
project_id: "ID dự án"
project: "Tên dự án"
use_case_id: "ID Use Case"
use_case: "Tên Use Case"
author: "DEV-BOT"
created_date: "Ngày tạo"
last_updated: "Ngày chỉnh sửa"
version: "Phiên bản"
reviewed_by: ""
tags: [Liệt kê các tags liên quan tới Use Case]
related_modules: [Dựa vào mã nguồn liệu kê các modules liên quan tới Use Case]
ai_agent_guidance: "Tài liệu này dùng để hỗ trợ AI trong việc review logic xử lý và generate test case."
input_docs: [Liệt kê danh sách các file paths trỏ tới tài liệu của SA, BA]
---

# Use Case - [Tên Use Case]

## 1. Scope & Objectives

### 1.1. Overview

> Tóm tắt ngắn gọn về use case và lý do thực hiện.

### 1.2. Scope

> Xác định phạm vi áp dụng của use case này (module, hệ thống, chức năng nào).

### 1.3. Objectives

> Các mục tiêu cụ thể khi phát triển Use Case: giải quyết vấn đề gì, cải thiện gì? Liệt kê từng dòng bắt đầu bằng "-".

---

## 2. Basic Design

### 2.1. Functional Requirements

> Các yêu cầu chức năng chính liên quan tới Use Case. Liệt kê từng dòng bắt đầu bằng "-".

### 2.2. Non-Functional Requirements

> Các yêu cầu phi chức năng của Use Case: Hiệu năng, bảo mật, khả năng mở rộng, tính sẵn sàng, v.v... Liệt kê từng dòng bắt đầu bằng "-".

### 2.3. Assumptions & Constraints

> Các giả định và ràng buộc của Use Case. Liệt kê từng dòng.

---

## 3. Detailed Design

### 3.1. Overall Architecture

> Mô tả kiến trúc tổng quan liên quan đến Use Case (có thể dùng sơ đồ kiến trúc high-level).

### 3.2. Class / Module Design

> Liệt kê các class / module theo mẫu.

- **[Tên Class / Module]**
- [Mô tả chức năng]

### 3.3. API/Interface Design

> Liệt kê các API endpoint theo mẫu.

- **[HTTP Method] [Route theo REST convention]**
- Request:
  ```json
  [Liệt kê các thuộc tính và kèm giá trị của request payload ở dạng JSON]
  ```
- Response:
  ```json
  {
  [Liệt kê các thuộc tính và kèm giá trị của response payload ở dạng JSON]
  }
  ```
- Response Code: [HTTP response Status Code]

### 3.4. Data Design

> Liệt kê các database, table liên quan tới Use Case mà có sự thay đổi theo mẫu.

- **Database:** [Tên database]
- **Table:** [Tên table]
- [Tên cột]: [Data type] [Ràng buộc nếu có]

### 3.5. Class Diagram

> Mã startuml Class diagram

### 3.6. Sequence Diagram

> Các sơ đồ sequence mô tả luồng tương tác chi tiết giữa các thành phần hoặc đối tượng trong Use Case.
> Mã startuml Sequence diagram

### 3.7. Security Considerations

> Mô tả các yêu cầu về bảo mật. Liệt kê từng dòng bắt đầu bằng "-".

### 3.8. Error Handling & Exceptions

> Mô tả các yêu cầu về xử lý lỗi / ngoại lệ, message rõ ràng. Liệt kê từng dòng bắt đầu bằng "-".

### 3.9. Integration Requirements

> Mô tả các yêu cầu về tích hợp với các service, module. Liệt kê từng dòng bắt đầu bằng "-".

---

## 4. Appendix

> Mô tả các liên kết / tham chiếu liên quan tới Use Case. Liệt kê từng dòng bắt đầu bằng "-".
