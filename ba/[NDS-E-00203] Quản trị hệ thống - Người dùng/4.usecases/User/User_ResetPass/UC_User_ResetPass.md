# Use Case: User_ResetPass (Reset mật khẩu người dùng)

## User Story
- Với vai trò là **Quản trị viên/CVSTP/CVBTP**, tôi muốn reset mật khẩu cho người dùng thuộc danh sách quản lý của mình để giúp họ khôi phục quyền truy cập vào hệ thống.

## Acceptance Criteria
- Chỉ cho phép Quản trị viên, CVSTP, CVBTP có quyền reset mật khẩu cho người dùng thuộc danh sách quản lý của mình.
- Khi reset mật khẩu, hệ thống sẽ tự động tạo mật khẩu mới và gửi về email của người dùng. **Mật khẩu mặc định được thiết lập từ hệ thống BR13 Rule Dùng chung/business_rules.md**
- Hiển thị thông báo thành công/thất bại sau khi thực hiện reset mật khẩu.

## Tác nhân chính
- Quản trị viên hệ thống
- Công chứng viên Sở Tư pháp (CVSTP)
- Công chứng viên Bộ Tư pháp (CVBTP)

## Tiền điều kiện
- Người dùng (Quản trị viên/CVSTP/CVBTP) đã đăng nhập hệ thống.
- Người dùng có quyền quản lý danh sách người dùng cần reset mật khẩu.

## Luồng chính
1. Người dùng (Quản trị viên/CVSTP/CVBTP) đăng nhập hệ thống.
2. Người dùng truy cập chức năng "Quản lý người dùng" từ menu.
3. Hệ thống hiển thị danh sách người dùng (**SCR_User_List**).
4. Người dùng tìm kiếm hoặc chọn người dùng để thực hiện reset mật khẩu.
5. Nếu tìm kiếm thành công:
   - Hệ thống hiển thị kết quả tìm kiếm hoặc thông tin người dùng đã chọn.
   - Hệ thống hiển thị trang xác nhận reset mật khẩu (**SCR_User_ResetPass**).
     * Trang hiển thị:
       - Thông tin tài khoản người dùng cần reset mật khẩu
       - Lưu ý: Mật khẩu mới sẽ được gửi về email của người dùng
   - Nếu người dùng xác nhận reset mật khẩu:
     * Hệ thống reset mật khẩu theo quy tắc BR13.
     * Hệ thống gửi email thông báo mật khẩu mới cho người dùng.
     * Hệ thống hiển thị thông báo "Reset mật khẩu thành công".
     * Hệ thống ghi log lịch sử reset mật khẩu.
   - Nếu người dùng không xác nhận:
     * Hệ thống quay về danh sách người dùng.
6. Nếu không tìm thấy người dùng:
   - Hệ thống hiển thị thông báo "Không tìm thấy người dùng, vui lòng thử lại".
7. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Lỗi hệ thống khi reset mật khẩu**:
  1. Người dùng xác nhận reset mật khẩu.
  2. Hệ thống không thể reset mật khẩu.
  3. Hệ thống hiển thị thông báo "Reset mật khẩu thất bại, vui lòng thử lại".
  4. Người dùng ở lại trang xác nhận reset mật khẩu.

- **Lỗi hệ thống khi gửi email**:
  1. Hệ thống reset mật khẩu thành công.
  2. Hệ thống không thể gửi email thông báo mật khẩu mới.
  3. Hệ thống hiển thị thông báo "Reset mật khẩu thành công nhưng không thể gửi email thông báo".
  4. Hệ thống ghi log lịch sử reset mật khẩu.

## Hậu điều kiện
- Nếu thành công: Mật khẩu của người dùng được reset theo quy tắc BR13 và thông báo mật khẩu mới được gửi về email của họ.
- Nếu thất bại: Hiển thị thông báo lỗi, mật khẩu của người dùng không được thay đổi.

## Liên kết
- Activity Diagram: [AD_User_ResetPass.puml]
- Form liên quan: [SCR_User_List.md], [SCR_User_ResetPass.md]
- Entity liên quan: **ENT_NguoiDung**
- Business Rule: [BR13 - Quy tắc đặt mật khẩu mặc định]