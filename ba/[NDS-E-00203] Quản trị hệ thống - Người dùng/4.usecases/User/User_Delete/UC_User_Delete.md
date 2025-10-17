# Use Case: User_Delete (Xóa tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn xóa tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn xóa tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 1 và cấp 2 thuộc quyền quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn xóa tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 2.

## Acceptance Criteria
- Cho phép người dùng xóa tài khoản người dùng từ danh sách.
- Hiển thị popup xác nhận xóa tài khoản trước khi thực hiện xóa.
- Popup xác nhận hiển thị thông báo xác nhận xóa, thông tin cơ bản của tài khoản, nút "Xác nhận" và nút "Hủy".
- Việc xóa tài khoản là xóa mềm: cập nhật trạng thái tài khoản về "Không sử dụng", DB vẫn lưu thông tin tài khoản.
- Người dùng có quyền truy cập danh sách thì có quyền xóa tài khoản trong danh sách đó.
- Phạm vi xóa tài khoản theo cấp đơn vị của người dùng:
  + Admin: Có thể xóa tất cả tài khoản trong hệ thống
  + CVBTP: Có thể xóa tài khoản trong đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Có thể xóa tài khoản trong đơn vị cấp 2
- Hiển thị thông báo thành công khi xóa tài khoản thành công.
- Hiển thị thông báo lỗi khi xóa tài khoản thất bại.
- Sau khi xóa thành công, hệ thống tự động tải lại danh sách tài khoản người dùng.

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách tài khoản người dùng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng" (**SCR_User_List**).
2. Người dùng chọn tài khoản người dùng cần xóa.
3. Người dùng chọn thao tác "Xóa tài khoản".
4. Hệ thống hiển thị popup xác nhận xóa tài khoản (**SCR_User_Delete**).
5. Popup xác nhận hiển thị thông báo xác nhận xóa, thông tin cơ bản của tài khoản, nút "Xác nhận" và nút "Hủy".
6. Người dùng chọn "Xác nhận".
7. Hệ thống cập nhật trạng thái tài khoản về "Không sử dụng" (xóa mềm).
8. Nếu cập nhật trạng thái thành công:
   - Hệ thống hiển thị thông báo "Xóa tài khoản thành công".
   - Hệ thống đóng popup xác nhận.
   - Hệ thống tải lại danh sách tài khoản người dùng (**SCR_User_List**).
9. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Người dùng chọn "Hủy" trong popup xác nhận**:
  1. Hệ thống hiển thị popup xác nhận xóa tài khoản.
  2. Người dùng chọn "Hủy".
  3. Hệ thống đóng popup xác nhận.
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).
- **Lỗi hệ thống khi cập nhật trạng thái**:
  1. Hệ thống cập nhật trạng thái tài khoản về "Không sử dụng".
  2. Nếu cập nhật trạng thái không thành công:
  3. Hệ thống hiển thị thông báo "Xóa tài khoản thất bại".
  4. Hệ thống đóng popup xác nhận.
  5. Người dùng ở lại màn hình danh sách (**SCR_User_List**).

## Hậu điều kiện
- Nếu thành công: Trạng thái tài khoản người dùng được cập nhật thành "Không sử dụng" trong hệ thống.
- Nếu thất bại: Trạng thái tài khoản người dùng không thay đổi, dữ liệu giữ nguyên trạng thái ban đầu.

## Liên kết
- Activity Diagram: [AD_User_Delete.puml]
- Form liên quan: [SCR_User_Delete.md]
- Entity liên quan: **ENT_NguoiDung**