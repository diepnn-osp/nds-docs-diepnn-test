# Use Case: DM_Donvi_Download_Temp (Tải về file mẫu import danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn tải về file mẫu import danh mục đơn vị để chuẩn bị dữ liệu nhập vào hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn tải về file mẫu import danh mục đơn vị để chuẩn bị dữ liệu nhập vào hệ thống.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn tải về file mẫu import danh mục đơn vị để chuẩn bị dữ liệu nhập vào hệ thống.

## Acceptance Criteria
- Cho phép người dùng tải về file mẫu import danh mục đơn vị từ danh sách.
- Lấy file mẫu từ danh mục file quản lý.
- Tải về file mẫu về thiết bị người dùng.
- Hiển thị thông báo thành công khi tải về thành công.
- Hiển thị thông báo lỗi khi tải về thất bại.
- Hiển thị thông báo khi không tìm thấy file mẫu.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách danh mục đơn vị.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị" (**SCR_DM_Donvi_List**).
2. Người dùng chọn thao tác "Tải về file mẫu import".
3. Hệ thống lấy file mẫu từ danh mục file quản lý.
4. Nếu lấy file thành công:
   - Hệ thống tải về file mẫu về thiết bị.
   - Nếu tải về thành công:
     - Hệ thống hiển thị thông báo "Tải về file mẫu thành công".
     - Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
5. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Không tìm thấy file mẫu**:
  1. Hệ thống lấy file mẫu từ danh mục file quản lý.
  2. Nếu không tìm thấy file mẫu:
  3. Hệ thống hiển thị thông báo "Không tìm thấy file mẫu".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
- **Tải về file thất bại**:
  1. Hệ thống tải về file mẫu về thiết bị.
  2. Nếu tải về không thành công:
  3. Hệ thống hiển thị thông báo "Tải về file mẫu thất bại".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).

## Hậu điều kiện
- **Nếu thành công**: Người dùng nhận được file mẫu import danh mục đơn vị.
- **Nếu thất bại**: Người dùng không nhận được file, hiển thị thông báo lỗi tương ứng.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Download_Temp.puml]
- Form liên quan: [SCR_DM_Donvi_Download_Temp.md]
- Entity liên quan: **ENT_DM_Donvi**