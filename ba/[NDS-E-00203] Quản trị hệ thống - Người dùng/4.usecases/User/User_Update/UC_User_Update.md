# Use Case: User_Update (Cập nhật thông tin tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn cập nhật thông tin tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn cập nhật thông tin tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 1 và cấp 2 thuộc quyền quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn cập nhật thông tin tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 2.

## Acceptance Criteria
- Cho phép người dùng cập nhật thông tin tài khoản người dùng từ danh sách.
- Hiển thị form cập nhật với các trường thông tin có thể chỉnh sửa: Họ và tên, Email, Vai trò, Đơn vị, Trạng thái.
- Tên tài khoản không được phép chỉnh sửa.
- Kiểm tra dữ liệu hợp lệ trước khi cập nhật tài khoản:
  + Họ và tên không được để trống
  + Email phải đúng định dạng
  + Vai trò phải được chọn
  + Đơn vị phải được chọn
- Người dùng đã có quyền xem danh sách tài khoản người dùng sẽ tự động có quyền cập nhật thông tin các tài khoản trong phạm vi quyền của họ.
- Phạm vi cập nhật thông tin tài khoản theo cấp đơn vị của người dùng:
  + Admin: Có thể cập nhật thông tin tất cả tài khoản trong hệ thống
  + CVBTP: Có thể cập nhật thông tin tài khoản trong đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Có thể cập nhật thông tin tài khoản trong đơn vị cấp 2
- Hiển thị thông báo thành công khi cập nhật thông tin tài khoản thành công.
- Hiển thị thông báo lỗi khi cập nhật thông tin tài khoản thất bại.

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách tài khoản người dùng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng" (**SCR_User_List**).
2. Người dùng chọn tài khoản người dùng cần cập nhật thông tin.
3. Hệ thống tải thông tin chi tiết tài khoản người dùng.
4. Nếu tải dữ liệu thành công:
   - Hệ thống hiển thị form cập nhật thông tin tài khoản người dùng (**SCR_User_Update**).
   - Người dùng chỉnh sửa thông tin tài khoản (Họ và tên, Email, Vai trò, Đơn vị, Trạng thái).
   - Người dùng chọn thao tác "Lưu thông tin".
   - Hệ thống kiểm tra dữ liệu hợp lệ.
   - Nếu dữ liệu hợp lệ:
     - Hệ thống cập nhật thông tin tài khoản người dùng.
     - Nếu cập nhật thành công:
       - Hệ thống hiển thị thông báo "Cập nhật thông tin tài khoản thành công".
       - Chuyển hướng về danh sách (**SCR_User_List**).
5. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Không tải được thông tin tài khoản**:
  1. Hệ thống tải thông tin chi tiết tài khoản người dùng.
  2. Nếu không tải được thông tin:
  3. Hệ thống hiển thị thông báo "Không tải được thông tin tài khoản, vui lòng thử lại".
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).
- **Dữ liệu không hợp lệ**:
  1. Hệ thống kiểm tra dữ liệu hợp lệ.
  2. Nếu dữ liệu không hợp lệ:
  3. Hệ thống hiển thị thông báo lỗi dữ liệu.
  4. Người dùng ở lại màn hình cập nhật (**SCR_User_Update**).
- **Lỗi hệ thống khi cập nhật thông tin**:
  1. Hệ thống cập nhật thông tin tài khoản người dùng.
  2. Nếu cập nhật thông tin không thành công:
  3. Hệ thống hiển thị thông báo "Cập nhật thông tin tài khoản thất bại".
  4. Người dùng ở lại màn hình cập nhật (**SCR_User_Update**).

## Hậu điều kiện
- Nếu thành công: Thông tin tài khoản người dùng được cập nhật trong hệ thống.
- Nếu thất bại: Không có thông tin nào được cập nhật, dữ liệu giữ nguyên trạng thái ban đầu.

## Liên kết
- Activity Diagram: [AD_User_Update.puml]
- Form liên quan: [SCR_User_Update.md]
- Entity liên quan: **ENT_NguoiDung**