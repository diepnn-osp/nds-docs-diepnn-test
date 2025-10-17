# Use Case: DM_BenLQ_Update (Chỉnh sửa thông tin danh mục bên liên quan)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn Chỉnh sửa thông tin danh mục bên liên quan.

## Acceptance Criteria
- Hệ thống hiển thị form chỉnh sửa thông tin danh mục bên liên quan.
- Người dùng nhập thông tin: 
   - Mã danh mục **Disable**
   - Tên danh mục. 
- Hệ thống kiểm tra dữ liệu hợp lệ (tên danh mục không trùng lặp, các trường bắt buộc phải được điền đầy đủ).
- Nếu hợp lệ: Lưu danh mục.
- Hiển thị thông báo "Chỉnh sửa thông tin danh mục thành công".
- Người dùng có thể xóa danh mục ở thao tác Xóa (điều kiện: Danh mục chưa được sử dụng).

## Tác nhân chính
- Quản trị viên

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục.

## Luồng chính
1. Người dùng chọn chức năng **Chỉnh sửa danh mục bên liên quan** từ menu (**DM_BenLQ_Update**).
2. Hệ thống hiển thị form chỉnh sửa danh mục (**DM_BenLQ_Update**).
3. Người dùng nhập các thông tin cần thiết.
4. Người dùng bấm nút **Lưu thông tin**.
5. Hệ thống kiểm tra dữ liệu:
   - Nếu hợp lệ: Lưu dữ liệu danh mục.
   - Hiển thị thông báo "Chỉnh sửa thông tin danh mục thành công".
   - Quay về danh sách (**DM_BenLQ_List**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Người dùng chọn **Hủy**: Form đóng, không lưu dữ liệu.
- Nhập thiếu thông tin bắt buộc: Hiển thị cảnh báo lỗi.
- Lỗi hệ thống: Hiển thị thông báo lỗi, không lưu dữ liệu.

## Hậu điều kiện
- Nếu thành công: Danh mục bên liên quan được lưu trong hệ thống.
- Nếu thất bại: Dữ liệu danh mục không được cập nhật.

## Liên kết
- Activity Diagram: [AD_DM_BenLQ_Update.puml]
- Form liên quan: [SCR_DM_BenLQ_Update.md]
- Entity liên quan: **ENT_DM_BenLQ**
