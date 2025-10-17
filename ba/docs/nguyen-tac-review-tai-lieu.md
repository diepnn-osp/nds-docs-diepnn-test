# Nguyên tắc chung

- Luôn rà soát lỗi chính tả
- Đồng bộ naming convention:
  - Tên file phải nhất quán: AD_[TênChứcNăng].puml, UC_[TênChứcNăng].md, SCR_[TênChứcNăng].md
  - Tên chức năng phải đồng bộ giữa các file liên quan
- Tham chiếu chéo:
  - File UC phải có link đến file AD và SCR tương ứng
  - File AD phải có title rõ ràng, đồng bộ với UC
- Entity reference:
  - Khi đề cập đến entity trong file UC/SCR, phải theo format **ENT_TenEntity**

## Quy tắc cho Activity Diagram (.puml)

### Cấu trúc file

- Bắt đầu với `@startuml AD_[TênChứcNăng]`
- Có `!pragma layout smetana`
- Có `title Activity Diagram: [Tên chức năng]`
- Kết thúc với `@enduml`

### Nội dung

- Phải có `start` và `stop`
- Các action phải rõ ràng, ngắn gọn
- Sử dụng if/else cho các điều kiện rẽ nhánh
- Sử dụng switch/case cho các lựa chọn

### Tham chiếu

- Khi chuyển hướng màn hình, phải có reference đến file SCR tương ứng

## Quy tắc cho Use Case (.md)

### Cấu trúc file

- Bắt đầu với `# Use Case: [Tên chức năng]`
- Phải có các section: User Story, Acceptance Criteria, Tác nhân chính, Tiền điều kiện, Luồng chính, Luồng phụ/Ngoại lệ, Hậu điều kiện, Liên kết

### User Story

- Phải theo format: "Với vai trò là **[Vai trò]**, tôi muốn [mục đích] để [lợi ích]"

### Acceptance Criteria

- Bắt đầu với động từ ở dạng khẳng định
- Rõ ràng, có thể kiểm chứng được

### Luồng chính

- Đánh số thứ tự (1., 2., 3., ...)
- Mỗi bước phải rõ ràng, ngắn gọn và tập trung mô tả luồng chính của hệ thống
- Khi reference đến UC khác, phải có format `(**UC_TenChucNang**)`

### Luồng phụ/Ngoại lệ

- Mô tả rõ điều kiện xảy ra và cách xử lý đối với các luồng phụ

### Liên kết

- Phải có link đến Activity Diagram: `[AD_TenChucNang.puml]`
- Phải có link đến Screen: `[SCR_TenChucNang.md]`
- Phải có Entity liên quan: **ENT_TenEntity**

## Quy tắc cho Screen (.md)

### Cấu trúc file

- Bắt đầu với `# Màn hình: [Tên màn hình]`
- Có thể có mô tả ngắn gọn về màn hình (1-2 dòng)
- Phải có các section theo thứ tự:
  1. **Điều kiện tiên quyết**
  2. **Nguyên mẫu**
  3. **Thành phần** (bao gồm subsection **Chức năng** nếu có)

**Lưu ý về cấp độ heading**:
- "Điều kiện tiên quyết", "Nguyên mẫu", "Thành phần" là section cấp 2 (`##`)
- "Chức năng" là subsection cấp 3 (`###`) của "Thành phần" (KHÔNG phải section cấp 2)

### Điều kiện tiên quyết

- Phải mô tả rõ quyền truy cập và các điều kiện cần thiết
- Đặt ở đầu tiên để người đọc biết điều kiện trước khi đọc chi tiết màn hình

### Nguyên mẫu

- Gắn các link figma (có thể có hoặc chưa)
- Nếu chưa có, để `[]`

### Thành phần

- Sử dụng table để mô tả các trường thông tin
- Đặt tên subsection theo loại thành phần: "Form nhập liệu", "Bảng kết quả", "Popup xác nhận", v.v.
- Table phải có các cột:
  - **Bắt buộc cho tất cả**: Trường thông tin, Control, Field, Mô tả
  - **Tùy chọn** (theo loại màn hình):
    - Max length (với form nhập/sửa)
    - Bắt buộc (Y/N) (với form nhập/sửa)
    - Giá trị mặc định (với form nhập/sửa)
    - Cho phép sửa (Y/N) (với form sửa/chi tiết)

**Quy tắc cho cột "Mô tả"**:
- Rõ ràng, ngắn gọn
- Có reference đến Business Rules khi cần: **BR9.7**
- Có placeholder cho input fields: Mặc định "Nhập/Chọn [tên label]", nếu khác ghi rõ trong mô tả

### Chức năng

- **Là subsection (`###`) của "Thành phần"**, KHÔNG phải section độc lập cấp 2
- Sử dụng table để mô tả các nút/chức năng
- Table phải có các cột: Tên, Loại, Mô tả
- Trong cột "Mô tả":
  - Khi reference đến Màn hình khác, phải có format `(**SCR_TenChucNang**)`
  - Khi reference đến Use Case, phải có format `(**UC_TenChucNang**)`
