# Use Case: DM_Donvi_Delete (Xóa danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn xóa danh mục đơn vị để quản lý dữ liệu hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn xóa danh mục đơn vị để quản lý dữ liệu hệ thống.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn xóa danh mục đơn vị để quản lý dữ liệu hệ thống.

## Acceptance Criteria
- Cho phép người dùng chọn danh mục cần xóa từ danh sách.
- Kiểm tra điều kiện xóa (danh mục chưa được sử dụng trong các tính năng nghiệp vụ).
- Hiển thị thông báo lỗi nếu danh mục đã được sử dụng.
- Yêu cầu xác nhận trước khi xóa danh mục.
- Xóa danh mục khi người dùng xác nhận.
- Hiển thị thông báo thành công khi xóa thành công.
- Hiển thị thông báo lỗi hệ thống khi xóa thất bại.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục đơn vị.
- Danh mục đơn vị cần xóa đã tồn tại trong hệ thống.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị" (**SCR_DM_Donvi_List**).
2. Người dùng chọn danh mục cần xóa từ danh sách.
3. Người dùng chọn thao tác xóa.
4. Hệ thống kiểm tra điều kiện xóa.
5. Nếu danh mục chưa được sử dụng:
   - Hệ thống hiển thị hộp thoại xác nhận xóa danh mục.
   - Người dùng chọn "Đồng ý".
   - Hệ thống xóa danh mục.
   - Nếu xóa thành công:
     - Hệ thống hiển thị thông báo "Xóa danh mục thành công".
     - Chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Danh mục đã được sử dụng**:
  1. Hệ thống kiểm tra điều kiện xóa.
  2. Nếu danh mục đã được sử dụng:
  3. Hệ thống hiển thị thông báo "Danh mục đã được sử dụng, không thể xóa".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
- **Người dùng hủy thao tác**:
  1. Hệ thống hiển thị hộp thoại xác nhận xóa danh mục.
  2. Người dùng chọn "Không".
  3. Hệ thống hủy thao tác.
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
- **Lỗi hệ thống khi xóa**:
  1. Hệ thống xóa danh mục.
  2. Nếu xóa không thành công:
  3. Hệ thống hiển thị thông báo lỗi hệ thống.
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).

## Hậu điều kiện
- **Nếu thành công**: Danh mục đơn vị được xóa khỏi hệ thống.
- **Nếu thất bại**: Danh mục không được xóa, dữ liệu giữ nguyên trạng thái ban đầu.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Delete.puml]
- Form liên quan: [SCR_DM_Donvi_Delete.md]
- Entity liên quan: **ENT_DM_Donvi**