# Use Case: User_UpdateInfo (Cập nhật thông tin tài khoản người dùng)

## User Story
- Với vai trò là **Người dùng đã đăng nhập**, tôi muốn cập nhật thông tin tài khoản của chính mình để đảm bảo thông tin cá nhân luôn chính xác.

## Acceptance Criteria
- Cho phép tất cả người dùng đã đăng nhập đều có quyền cập nhật thông tin tài khoản của chính mình.
- Các thông tin không được cập nhật: Tên tài khoản, Đơn vị, Vai trò, Trạng thái.
- Hiển thị thông báo thành công/thất bại sau khi thực hiện cập nhật thông tin.

## Tác nhân chính
- Tất cả người dùng đã đăng nhập hệ thống

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng đang ở trang chủ hoặc trang quản lý tài khoản cá nhân.

## Luồng chính
1. Người dùng đăng nhập hệ thống.
2. Người dùng truy cập chức năng "Thông tin tài khoản" từ menu.
3. Người dùng chọn cập nhật thông tin tài khoản.
4. Hệ thống hiển thị trang cập nhật thông tin (**SCR_User_UpdateInfo**).
   - Các thông tin không được cập nhật:
     * Tên tài khoản (chỉ xem)
     * Đơn vị (chỉ xem)
     * Vai trò (chỉ xem)
     * Trạng thái (chỉ xem)
5. Nếu người dùng nhấn "Lưu":
   - Nếu thông tin hợp lệ:
     * Hệ thống cập nhật thông tin tài khoản.
     * Hệ thống hiển thị thông báo "Cập nhật thông tin thành công".
     * Hệ thống ghi log lịch sử cập nhật thông tin.
     * Hệ thống chuyển về trang chủ.
   - Nếu thông tin không hợp lệ:
     * Hệ thống hiển thị thông báo lỗi chi tiết.
6. Nếu người dùng nhấn "Hủy":
   - Hệ thống chuyển về trang chủ.
7. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Lỗi hệ thống khi cập nhật thông tin**:
  1. Người dùng nhấn "Lưu".
  2. Hệ thống không thể cập nhật thông tin.
  3. Hệ thống hiển thị thông báo "Cập nhật thông tin thất bại, vui lòng thử lại".
  4. Người dùng ở lại trang cập nhật thông tin.

## Hậu điều kiện
- Nếu thành công: Thông tin tài khoản của người dùng được cập nhật và ghi lại lịch sử cập nhật.
- Nếu thất bại: Hiển thị thông báo lỗi, thông tin tài khoản của người dùng không được thay đổi.

## Liên kết
- Activity Diagram: [AD_User_UpdateInfo.puml]
- Form liên quan: [SCR_User_UpdateInfo.md]
- Entity liên quan: **ENT_NguoiDung**