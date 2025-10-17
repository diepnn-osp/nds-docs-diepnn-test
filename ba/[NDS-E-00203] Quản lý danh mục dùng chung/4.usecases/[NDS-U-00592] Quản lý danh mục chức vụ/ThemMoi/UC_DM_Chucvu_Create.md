# Use Case: DM_Chucvu_Create (Thêm mới danh mục chức vụ)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn thêm mới danh mục chức vụ.

## Acceptance Criteria
- Hệ thống hiển thị form thêm mới danh mục chức vụ.
- Người dùng nhập thông tin: 
   - Mã danh mục **Tự sinh theo hệ thống, không cho chỉnh sửa**
   - Tên danh mục. 
- Hệ thống kiểm tra dữ liệu hợp lệ (tên danh mục không trùng lặp, các trường bắt buộc).
- Nếu hợp lệ: Lưu danh mục.
- Hiển thị thông báo "Thêm mới danh mục thành công".

## Tác nhân chính
- Quản trị viên

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục.

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới danh mục chức vụ** từ menu (**DM_Chucvu_Create**).
2. Hệ thống hiển thị form thêm mới danh mục (**DM_Chucvu_Create**).
3. Người dùng nhập các thông tin cần thiết.
4. Người dùng bấm nút **Lưu thông tin**.
5. Hệ thống kiểm tra dữ liệu:
   - Nếu hợp lệ: Lưu dữ liệu danh mục.
   - Hiển thị thông báo "Thêm mới danh mục thành công".
   - Quay về danh sách (**DM_Chucvu_List**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Người dùng chọn **Hủy**: Form đóng, không lưu dữ liệu.
- Nhập thiếu thông tin bắt buộc: Hiển thị cảnh báo lỗi.
- Lỗi hệ thống: Hiển thị thông báo lỗi, không lưu dữ liệu.

## Hậu điều kiện
- Nếu thành công: Danh mục chức vụ được lưu trong hệ thống.
- Nếu thất bại: Không có dữ liệu nào được thêm.

## Liên kết
- Activity Diagram: [AD_DM_Chucvu_Create.puml]
- Form liên quan: [SCR_DM_Chucvu_Create.md]
- Entity liên quan: **ENT_DM_Chucvu**
