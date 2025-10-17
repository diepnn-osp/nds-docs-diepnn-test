# Use Case: User_ChangePass (Đổi mật khẩu tài khoản người dùng)

## User Story
- Với vai trò là **Người dùng đã đăng nhập**, tôi muốn đổi mật khẩu của chính mình để đảm bảo an toàn cho tài khoản.

## Acceptance Criteria
- Cho phép tất cả người dùng đã đăng nhập đều có quyền đổi mật khẩu của chính mình.
- Yêu cầu nhập mật khẩu cũ để xác thực.
- Yêu cầu nhập mật khẩu mới và xác nhận mật khẩu mới.
- Mật khẩu mới phải tuân thủ chính sách mật khẩu của hệ thống.
- Ghi log lịch sử đổi mật khẩu.
- Hiển thị thông báo lỗi nếu không đổi được mật khẩu.

## Tác nhân chính
- Tất cả người dùng đã đăng nhập hệ thống

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng đang ở trang quản lý tài khoản cá nhân.

## Luồng chính
1. Người dùng truy cập chức năng "Quản lý tài khoản cá nhân".
2. Người dùng nhấn nút "Đổi mật khẩu".
3. Hệ thống hiển thị form đổi mật khẩu cá nhân (**SCR_User_ChangePass**).
4. Form hiển thị: Tên tài khoản (không cho phép sửa), Mật khẩu cũ, Mật khẩu mới, Xác nhận mật khẩu mới.
5. Người dùng nhập mật khẩu cũ.
6. Người dùng nhập mật khẩu mới.
7. Người dùng nhập xác nhận mật khẩu mới.
8. Người dùng nhấn nút "Xác nhận".
9. Hệ thống kiểm tra mật khẩu cũ.
10. Nếu mật khẩu cũ đúng:
    - Hệ thống kiểm tra mật khẩu mới và xác nhận có khớp nhau không.
    - Nếu khớp:
      * Hệ thống kiểm tra mật khẩu mới có tuân thủ chính sách mật khẩu không.
      * Nếu tuân thủ:
        - Hệ thống cập nhật mật khẩu mới cho tài khoản.
        - Hệ thống ghi log lịch sử đổi mật khẩu.
        - Hệ thống hiển thị thông báo "Đổi mật khẩu thành công".
        - Hệ thống đóng form, quay về trang chủ.
      * Nếu không tuân thủ:
        - Hệ thống hiển thị thông báo "Mật khẩu mới không tuân thủ chính sách mật khẩu".
        - Hệ thống hiển thị yêu cầu về mật khẩu (độ dài, ký tự đặc biệt, v.v.).
    - Nếu không khớp:
      * Hệ thống hiển thị thông báo "Mật khẩu mới và xác nhận không khớp".
11. Nếu mật khẩu cũ không đúng:
    - Hệ thống hiển thị thông báo "Mật khẩu cũ không đúng".
12. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Lỗi hệ thống khi đổi mật khẩu**:
  1. Người dùng xác nhận đổi mật khẩu.
  2. Hệ thống không thể cập nhật mật khẩu.
  3. Hệ thống hiển thị thông báo "Đổi mật khẩu thất bại, vui lòng thử lại".
  4. Người dùng ở lại form đổi mật khẩu.

## Hậu điều kiện
- Nếu thành công: Mật khẩu tài khoản người dùng được cập nhật, hệ thống ghi log lịch sử đổi mật khẩu.
- Nếu thất bại: Mật khẩu không được thay đổi, hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_User_ChangePass.puml]
- Form liên quan: [SCR_User_ChangePass.md]
- Entity liên quan: **ENT_NguoiDung**