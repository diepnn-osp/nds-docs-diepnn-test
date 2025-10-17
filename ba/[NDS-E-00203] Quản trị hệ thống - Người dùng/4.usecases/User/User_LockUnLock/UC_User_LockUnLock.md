# Use Case: User_LockUnLock (Khóa/Mở khóa tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn khóa/mở khóa tài khoản người dùng để quản lý trạng thái truy cập của người dùng trong hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn khóa/mở khóa tài khoản người dùng trong phạm vi quản lý để kiểm soát truy cập.
- Với vai trò là **Chuyên viên STP**, tôi muốn khóa/mở khóa tài khoản người dùng trong phạm vi quản lý để kiểm soát truy cập.

## Acceptance Criteria
- Hệ thống cho phép người dùng chọn một hoặc nhiều tài khoản để thực hiện khóa/mở khóa.
- Hệ thống hiển thị form xác nhận khóa/mở khóa tài khoản với các lựa chọn: Khóa hoặc Mở khóa.
- Người dùng phải nhập lý do khóa/mở khóa tài khoản (bắt buộc).
- Nếu tài khoản đang ở trạng thái Hoạt động và người dùng chọn Khóa:
  + Hệ thống cập nhật trạng thái tài khoản thành "Khóa".
  + Hệ thống ghi log lịch sử khóa tài khoản.
  + Hệ thống hiển thị thông báo "Khóa tài khoản thành công".
- Nếu tài khoản đang ở trạng thái Khóa và người dùng chọn Mở khóa:
  + Hệ thống cập nhật trạng thái tài khoản thành "Hoạt động".
  + Hệ thống ghi log lịch sử mở khóa tài khoản.
  + Hệ thống hiển thị thông báo "Mở khóa tài khoản thành công".
- Nếu tài khoản đã bị khóa trước đó và người dùng chọn Khóa:
  + Hệ thống hiển thị thông báo "Tài khoản đã bị khóa trước đó".
- Nếu tài khoản đang ở trạng thái hoạt động và người dùng chọn Mở khóa:
  + Hệ thống hiển thị thông báo "Tài khoản đang ở trạng thái hoạt động".
- Nếu người dùng không chọn tài khoản nào:
  + Hệ thống hiển thị thông báo "Vui lòng chọn ít nhất một tài khoản".
- Sau khi thực hiện thành công, hệ thống cập nhật lại danh sách người dùng.

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng truy cập vào chức năng "Danh sách tài khoản người dùng".

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng".
2. Người dùng chọn một hoặc nhiều tài khoản trong danh sách.
3. Người dùng chọn chức năng "Khóa/Mở khóa tài khoản".
4. Hệ thống hiển thị form xác nhận khóa/mở khóa tài khoản.
5. Người dùng chọn hành động (Khóa hoặc Mở khóa).
6. Người dùng nhập lý do khóa/mở khóa.
7. Người dùng xác nhận thực hiện.
8. Nếu hành động là Khóa:
   - Nếu tài khoản đang ở trạng thái Hoạt động:
     * Hệ thống cập nhật trạng thái tài khoản thành "Khóa".
     * Hệ thống ghi log lịch sử khóa tài khoản.
     * Hệ thống hiển thị thông báo "Khóa tài khoản thành công".
   - Nếu tài khoản đã bị khóa trước đó:
     * Hệ thống hiển thị thông báo "Tài khoản đã bị khóa trước đó".
9. Nếu hành động là Mở khóa:
   - Nếu tài khoản đang ở trạng thái Khóa:
     * Hệ thống cập nhật trạng thái tài khoản thành "Hoạt động".
     * Hệ thống ghi log lịch sử mở khóa tài khoản.
     * Hệ thống hiển thị thông báo "Mở khóa tài khoản thành công".
   - Nếu tài khoản đang ở trạng thái hoạt động:
     * Hệ thống hiển thị thông báo "Tài khoản đang ở trạng thái hoạt động".
10. Hệ thống cập nhật lại danh sách người dùng.
11. Kết thúc.

## Luồng phụ/ Ngoại lệ
- Nếu người dùng không chọn tài khoản nào: hiển thị thông báo "Vui lòng chọn ít nhất một tài khoản".
- Nếu khóa tài khoản thất bại: hiển thị thông báo "Khóa tài khoản thất bại".
- Nếu mở khóa tài khoản thất bại: hiển thị thông báo "Mở khóa tài khoản thất bại".

## Hậu điều kiện
- Nếu thành công: Trạng thái tài khoản người dùng được cập nhật (Khóa hoặc Mở khóa), lịch sử khóa/mở khóa được ghi lại, danh sách người dùng được cập nhật.
- Nếu thất bại: Trạng thái tài khoản không thay đổi, hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_User_LockUnLock.puml]
- Form liên quan: [SCR_User_LockUnlock.md]
- Entity liên quan: **ENT_NguoiDung**