# Use Case: User_Identify (Xác thực người dùng qua email)

## User Story
- Với vai trò là **Người dùng**, tôi muốn xác thực tài khoản của mình qua email để đảm bảo an toàn và bảo mật cho tài khoản.

## Acceptance Criteria
- Hệ thống chỉ yêu cầu xác thực khi quản trị hệ thống bật cấu hình này.
- Người dùng chưa xác thực sẽ không thể truy cập bất kỳ tính năng nào của hệ thống.
- Nếu người dùng chưa có email, hệ thống yêu cầu cập nhật email trước khi xác thực.
- Mã OTP gồm 6 chữ số và có thời hạn sử dụng 5 phút.
- Form nhập mã OTP có 6 ô riêng biệt, mỗi ô chỉ cho phép nhập 1 số.
- Cho phép gửi lại mã OTP với tính năng đếm ngược 5 phút.
- Giới hạn chỉ gửi được tối đa 3 lần OTP trong vòng 15 phút.
- Nếu quá giới hạn gửi OTP, hệ thống sẽ hiển thị thông báo lỗi và yêu cầu đợi 15 phút để gửi lại.
- Nếu xác thực OTP sai quá 5 lần, người dùng sẽ bị đăng xuất khỏi hệ thống.
- Xác thực thành công sẽ cập nhật email và đánh dấu tài khoản đã xác thực.
- Người dùng có thể thay đổi email trong quá trình xác thực.

## Tác nhân chính
- Tất cả người dùng đã đăng nhập hệ thống

## Tiền điều kiện
- Người dùng đã đăng nhập vào hệ thống.
- Quản trị hệ thống đã bật cấu hình yêu cầu xác thực người dùng.

## Luồng chính
1. Người dùng đăng nhập vào hệ thống.
2. Hệ thống kiểm tra cấu hình xác thực của quản trị hệ thống.
3. Hệ thống kiểm tra trạng thái xác thực của người dùng.
4. Nếu người dùng chưa xác thực:
   - Hệ thống hiển thị popup yêu cầu xác thực email.
   - Nếu người dùng đã có email trong hệ thống, hệ thống tự động điền email vào ô nhập liệu.
   - Nếu người dùng chưa có email, hệ thống hiển thị thông báo yêu cầu cập nhật email.
5. Người dùng nhập email (nếu cần) và nhấn nút "Xác thực".
6. Hệ thống kiểm tra số lần gửi OTP trong 15 phút gần nhất.
   - Nếu đã gửi quá 3 lần:
     * Hệ thống hiển thị thông báo "Đã quá giới hạn gửi OTP. Vui lòng thử lại sau 15 phút."
     * Người dùng phải đợi 15 phút để có thể gửi OTP mới.
   - Nếu chưa quá giới hạn:
     * Hệ thống gửi mã OTP (6 chữ số) về email của người dùng theo template:
       - Tiêu đề email: Mã OTP xác thực người dùng
       - Nội dung email: Mã xác thực OTP của bạn là: {{OTP_CODE}} Mã có hiệu lực trong 5 phút. Vui lòng nhập mã này vào hệ thống để tiếp tục. Nếu bạn không yêu cầu xác thực, vui lòng bỏ qua email này.
     * Hệ thống hiển thị popup nhập mã OTP với thông báo đã gửi mã đến email.
7. Popup có 6 ô nhập riêng biệt, mỗi ô chỉ cho phép nhập 1 số.
8. Popup có 6 ô nhập riêng biệt, mỗi ô chỉ cho phép nhập 1 số.
9. Người dùng nhập mã OTP vào 6 ô và nhấn nút "Xác nhận".
10. Hệ thống kiểm tra mã OTP:
    - Nếu mã đúng và còn hiệu lực (trong 5 phút):
     * Hệ thống cập nhật email của người dùng vào thông tin tài khoản.
     * Hệ thống đánh dấu tài khoản đã xác thực.
     * Hệ thống đóng popup xác thực.
     * Hệ thống hiển thị thông báo "Xác thực thành công".
     * Hệ thống cho phép người dùng truy cập các tính năng của hệ thống.
   - Nếu mã không đúng hoặc đã hết hạn:
     * Hệ thống hiển thị thông báo "Mã OTP không đúng hoặc đã hết hạn".
     * Hệ thống cho phép người dùng nhập lại mã hoặc gửi lại mã mới.
10. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Người dùng không có email**:
  1. Hệ thống hiển thị thông báo yêu cầu cập nhật email.
  2. Người dùng không cập nhật email.
  3. Hệ thống không cho phép truy cập bất kỳ tính năng nào.
  4. Popup xác thực không thể đóng cho đến khi người dùng cập nhật email và xác thực thành công.

- **Mã OTP hết hạn**:
  1. Người dùng nhập mã OTP đã hết hạn (sau 5 phút).
  2. Hệ thống hiển thị thông báo "Mã OTP đã hết hạn".
  3. Hệ thống cho phép người dùng gửi lại mã mới.
  4. Hệ thống gửi mã OTP mới (6 chữ số) về email.

- **Giới hạn gửi OTP**:
  1. Người dùng yêu cầu gửi mã OTP.
  2. Hệ thống kiểm tra số lần gửi OTP trong 15 phút gần nhất.
  3. Nếu đã gửi quá 3 lần:
     * Hệ thống hiển thị thông báo "Đã quá giới hạn gửi OTP. Vui lòng thử lại sau 15 phút."
     * Người dùng phải đợi 15 phút để có thể gửi OTP mới.
  4. Nếu chưa quá giới hạn:
     * Hệ thống gửi mã OTP và tăng bộ đếm số lần gửi.

- **Gửi lại mã OTP**:
  1. Người dùng nhấn nút "Gửi lại" trên popup nhập mã OTP.
  2. Hệ thống kiểm tra giới hạn gửi OTP (tối đa 3 lần trong 15 phút).
  3. Nếu chưa quá giới hạn và hết thời gian đếm ngược 5 phút:
     * Hệ thống kích hoạt nút "Gửi lại".
     * Người dùng có thể nhấn để gửi mã OTP mới về email.
     * Hệ thống hiển thị thông báo "Đã gửi lại mã OTP mới".
  4. Nếu đã quá giới hạn gửi OTP:
     * Hệ thống hiển thị thông báo "Đã quá giới hạn gửi OTP. Vui lòng thử lại sau 15 phút."
  5. Trong thời gian đếm ngược 5 phút, nút "Gửi lại" ở trạng thái không khả dụng.

- **Xác thực OTP sai quá 5 lần**:
  1. Người dùng nhập sai mã OTP lần thứ 5.
  2. Hệ thống hiển thị thông báo "Bạn đã xác thực sai quá 5 lần. Vui lòng đăng nhập lại."
  3. Hệ thống tự động đăng xuất tài khoản người dùng.
  4. Người dùng phải đăng nhập lại vào hệ thống.

- **Lỗi hệ thống khi gửi email**:
  1. Hệ thống không thể gửi email chứa mã OTP.
  2. Hệ thống hiển thị thông báo "Lỗi hệ thống, không thể gửi email xác thực. Vui lòng thử lại sau."
  3. Người dùng ở lại popup nhập email để thử lại.

- **Người dùng cập nhật email mới**: Hệ thống đánh dấu lại là người dùng chưa xác thực email và hiển thị popup yêu cầu xác thực.
- **Email đã tồn tại**: Nếu tồn tại 1 người dùng đã xác thực bằng email đó, thông báo lỗi email đã tồn tại

## Hậu điều kiện
- Nếu thành công: Tài khoản người dùng được xác thực, email được cập nhật, người dùng có thể truy cập các tính năng của hệ thống.
- Nếu thất bại: Người dùng không thể truy cập các tính năng của hệ thống cho đến khi xác thực thành công.

## Liên kết
- Activity Diagram: [AD_User_Identify.puml]
- Screen liên quan: [SCR_User_Identify.md]
- Entity liên quan: **ENT_NguoiDung**