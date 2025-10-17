# Use Case: User_Info (Xem thông tin tài khoản người dùng)

## User Story
- Với vai trò là **Người dùng đã đăng nhập**, tôi muốn xem thông tin tài khoản của chính mình để biết các thông tin cá nhân đang được lưu trong hệ thống.

## Acceptance Criteria
- Cho phép tất cả người dùng đã đăng nhập đều có quyền xem thông tin tài khoản của chính mình.
- Hiển thị đầy đủ các thông tin của người dùng theo entity NguoiDung.
- Cung cấp các nút chức năng: Cập nhật thông tin, Đổi mật khẩu, Đóng.
- Chuyển hướng đến các màn hình tương ứng khi người dùng chọn các nút chức năng.

## Tác nhân chính
- Tất cả người dùng đã đăng nhập hệ thống

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng đang ở trang chủ hoặc trang quản lý tài khoản cá nhân.

## Luồng chính
1. Người dùng đăng nhập hệ thống.
2. Người dùng truy cập chức năng "Thông tin tài khoản" từ menu.
3. Hệ thống kiểm tra và tải thông tin tài khoản của người dùng.
4. Nếu tải thông tin thành công:
   - Hệ thống hiển thị trang thông tin tài khoản (**SCR_User_Info**).
   - Người dùng xem thông tin tài khoản.
   - Người dùng chọn một trong các thao tác:
     * Nếu chọn "Cập nhật thông tin":
       - Hệ thống chuyển đến màn hình cập nhật thông tin (**SCR_User_UpdateInfo**).
     * Nếu chọn "Đổi mật khẩu":
       - Hệ thống chuyển đến màn hình đổi mật khẩu (**SCR_User_ChangePass**).
     * Nếu chọn "Đóng":
       - Hệ thống đóng trang thông tin tài khoản.
       - Hệ thống chuyển về trang chủ.
5. Nếu không tải được thông tin:
   - Hệ thống hiển thị thông báo "Không tải được thông tin tài khoản, vui lòng thử lại".
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Lỗi hệ thống khi tải thông tin**:
  1. Người dùng truy cập chức năng "Thông tin tài khoản".
  2. Hệ thống không thể tải thông tin tài khoản.
  3. Hệ thống hiển thị thông báo "Không tải được thông tin tài khoản, vui lòng thử lại".
  4. Người dùng ở lại trang hiện tại.

## Hậu điều kiện
- Nếu thành công: Người dùng xem được thông tin tài khoản của mình và có thể thực hiện các thao tác tiếp theo.
- Nếu thất bại: Hiển thị thông báo lỗi, người dùng không xem được thông tin tài khoản.

## Liên kết
- Activity Diagram: [AD_User_Info.puml]
- Form liên quan: [SCR_User_Info.md], [SCR_User_UpdateInfo.md], [SCR_User_ChangePass.md]
- Entity liên quan: **ENT_NguoiDung**