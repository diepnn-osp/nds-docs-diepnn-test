# Use Case: DM_Donvi_Export (Xuất danh sách danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn xuất danh sách danh mục đơn vị để có thể làm việc ngoại tuyến với dữ liệu.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn xuất danh sách danh mục đơn vị để có thể làm việc ngoại tuyến với dữ liệu.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn xuất danh sách danh mục đơn vị theo đơn vị của mình để có thể làm việc ngoại tuyến với dữ liệu.

## Acceptance Criteria
- Cho phép người dùng xuất danh sách danh mục đơn vị từ danh sách.
- Lấy dữ liệu danh sách theo phạm vi truy cập của người dùng.
- Tạo file xuất danh sách (Excel/CSV).
- Tải về file xuất về thiết bị người dùng.
- Hiển thị thông báo thành công khi xuất thành công.
- Hiển thị thông báo lỗi khi xuất thất bại.
- Hiển thị thông báo khi không có dữ liệu để xuất.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách danh mục đơn vị.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị" (**SCR_DM_Donvi_List**).
2. Người dùng chọn thao tác "Xuất danh sách".
3. Hệ thống lấy dữ liệu danh sách danh mục đơn vị theo phạm vi truy cập của người dùng.
4. Nếu lấy dữ liệu thành công:
   - Hệ thống tạo file xuất danh sách (Excel/CSV).
   - Nếu tạo file thành công:
     - Hệ thống tải về file xuất về thiết bị.
     - Nếu tải về thành công:
       - Hệ thống hiển thị thông báo "Xuất danh sách thành công".
       - Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
5. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Không có dữ liệu để xuất**:
  1. Hệ thống lấy dữ liệu danh sách danh mục đơn vị.
  2. Nếu không có dữ liệu:
  3. Hệ thống hiển thị thông báo "Không có dữ liệu để xuất".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
- **Lỗi hệ thống khi tạo file**:
  1. Hệ thống tạo file xuất danh sách (Excel/CSV).
  2. Nếu tạo file không thành công:
  3. Hệ thống hiển thị thông báo "Lỗi hệ thống không thể tạo file xuất".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).
- **Tải về file thất bại**:
  1. Hệ thống tải về file xuất về thiết bị.
  2. Nếu tải về không thành công:
  3. Hệ thống hiển thị thông báo "Tải về file thất bại".
  4. Người dùng ở lại màn hình danh sách (**SCR_DM_Donvi_List**).

## Hậu điều kiện
- **Nếu thành công**: Người dùng nhận được file xuất danh sách danh mục đơn vị theo phạm vi truy cập.
- **Nếu thất bại**: Người dùng không nhận được file, hiển thị thông báo lỗi tương ứng.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Export.puml]
- Form liên quan: [SCR_DM_Donvi_Export.md]
- Entity liên quan: **ENT_DM_Donvi**