# Use Case: DM_Donvi_Search (Tìm kiếm danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn tìm kiếm danh mục đơn vị để nhanh chóng tìm được thông tin cần quản lý.
- Với vai trò là **Chuyên viên cục BTTP**, tôi muốn tìm kiếm danh mục đơn vị để thực hiện công việc hiệu quả.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn tìm kiếm danh mục đơn vị để thực hiện công việc hiệu quả.

## Acceptance Criteria
- Hiển thị ô tìm kiếm trên màn hình danh sách danh mục đơn vị.
- Cho phép người dùng nhập tiêu chí tìm kiếm.
- Kiểm tra dữ liệu tìm kiếm khi người dùng chọn thao tác tìm kiếm.
- Hiển thị kết quả tìm kiếm khi có dữ liệu phù hợp.
- Hiển thị thông báo "Không tìm thấy kết quả phù hợp" khi không có dữ liệu.
- Cho phép thực hiện các thao tác trên kết quả tìm kiếm tùy theo phân quyền:
  + Sửa (nếu có quyền)
  + Xóa (nếu có quyền)

## Tác nhân chính
- Quản trị viên
- Chuyên viên cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách danh mục đơn vị.

## Luồng chính
1. Người dùng đang ở màn hình danh sách danh mục đơn vị.
2. Hệ thống hiển thị ô tìm kiếm.
3. Người dùng nhập tiêu chí tìm kiếm.
4. Người dùng chọn thao tác tìm kiếm.
5. Hệ thống kiểm tra dữ liệu tìm kiếm.
6. Nếu có dữ liệu tìm kiếm:
   - Hệ thống hiển thị kết quả tìm kiếm.
   - Người dùng có thể thực hiện các thao tác trên kết quả tìm kiếm tùy theo phân quyền.
7. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Không tìm thấy kết quả**:
  1. Hệ thống kiểm tra dữ liệu tìm kiếm.
  2. Nếu không có dữ liệu phù hợp:
  3. Hệ thống hiển thị thông báo "Không tìm thấy kết quả phù hợp".
  4. Người dùng có thể nhập lại tiêu chí tìm kiếm khác.

## Hậu điều kiện
- **Nếu thành công**: Người dùng xem được kết quả tìm kiếm danh mục đơn vị phù hợp.
- **Nếu thất bại**: Hiển thị thông báo không tìm thấy kết quả phù hợp.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Search.puml]
- Form liên quan: [SCR_DM_Donvi_Search.md]
- Entity liên quan: **ENT_DM_Donvi**
