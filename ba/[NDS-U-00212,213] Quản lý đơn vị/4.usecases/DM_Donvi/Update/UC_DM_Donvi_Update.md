# Use Case: DM_Donvi_Update (Chỉnh sửa thông tin danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn chỉnh sửa thông tin danh mục đơn vị để cập nhật dữ liệu chính xác.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn chỉnh sửa thông tin danh mục đơn vị để cập nhật dữ liệu chính xác.
- Với vai trò là **Chuyên viên tại Sở Tư Pháp**, tôi muốn chỉnh sửa thông tin danh mục đơn vị để cập nhật dữ liệu chính xác.

## Acceptance Criteria
- Hiển thị form chỉnh sửa thông tin danh mục đơn vị khi người dùng chọn chức năng chỉnh sửa.
- Người dùng nhập thông tin:
   - Mã danh mục **(không cho phép chỉnh sửa)**
   - Tên danh mục
   - Loại đơn vị
- Kiểm tra dữ liệu hợp lệ (tên danh mục không được để trống).
- Lưu danh mục khi dữ liệu hợp lệ.
- Hiển thị thông báo "Chỉnh sửa thông tin danh mục đơn vị thành công".
- Chuyển hướng về trang danh sách danh mục sau khi lưu thành công.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư Pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục đơn vị.
- Danh mục đơn vị cần chỉnh sửa đã tồn tại trong hệ thống.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị".
2. Người dùng chọn chỉnh sửa danh mục đã có trong danh sách.
3. Hệ thống hiển thị form nhập thông tin chỉnh sửa.
4. Người dùng nhập thông tin chỉnh sửa danh mục.
5. Người dùng chọn thao tác.
6. Người dùng chọn thao tác **Lưu thông tin**.
7. Hệ thống kiểm tra dữ liệu hợp lệ.
8. Nếu hợp lệ, hệ thống ghi nhận dữ liệu danh mục đơn vị.
9. Hệ thống kiểm tra ghi thành công:
   - Nếu thành công: Hiển thị thông báo "Chỉnh sửa thông tin danh mục đơn vị thành công".
   - Chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
10. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Luồng hủy thao tác**:
  1. Người dùng chọn thao tác **Đóng**.
  2. Hệ thống xác nhận hủy thao tác.
  3. Nếu người dùng chọn "Đồng ý": Hủy thao tác và chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
  4. Nếu người dùng chọn "Không": Ở lại màn hình chỉnh sửa (**SCR_DM_Donvi_Update**).
- **Kiểm tra dữ liệu không hợp lệ**:
  1. Người dùng chọn thao tác **Lưu thông tin** với dữ liệu không hợp lệ.
  2. Hệ thống hiển thị cảnh báo lỗi "Nhập thiếu thông tin bắt buộc".
  3. Người dùng ở lại màn hình chỉnh sửa (**SCR_DM_Donvi_Update**).
- **Lỗi hệ thống khi ghi dữ liệu**:
  1. Khi ghi nhận dữ liệu xảy ra lỗi hệ thống.
  2. Hệ thống hiển thị thông báo lỗi hệ thống.
  3. Người dùng ở lại màn hình chỉnh sửa (**SCR_DM_Donvi_Update**).

## Hậu điều kiện
- **Nếu thành công**: Danh mục đơn vị được cập nhật trong hệ thống.
- **Nếu thất bại**: Danh mục không được cập nhật, dữ liệu giữ nguyên trạng thái ban đầu.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Update.puml]
- Form liên quan: [SCR_DM_Donvi_Update.md]
- Entity liên quan: **ENT_DM_Donvi**
