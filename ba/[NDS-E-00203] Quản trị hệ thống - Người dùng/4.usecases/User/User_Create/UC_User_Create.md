# Use Case: User_Create (Thêm mới tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn thêm mới tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn thêm mới tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 1 và cấp 2 thuộc quyền quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn thêm mới tài khoản người dùng để quản lý thông tin trong phạm vi đơn vị cấp 2.

## Acceptance Criteria
- Cho phép người dùng thêm mới tài khoản người dùng từ danh sách.
- Mật khẩu của tài khoản mặc định theo quy tắc được quy định tại BR13 (**Business_rules.md**)
- Hiển thị form thêm mới với các trường thông tin: Họ và tên, Email, Vai trò, Đơn vị, Tên tài khoản, Mật khẩu.
- Đơn vị mặc định thuộc đơn vị của người có quyền truy cập danh sách. Người dùng có thể chọn lại đơn vị cùng cấp và có quyền tạo tài khoản tương ứng.
- Hệ thống tự động gợi ý tên tài khoản theo cú pháp: tên+viết tắt từ đầu tiên của họ và tên đệm.
- Nếu tên tài khoản gợi ý đã tồn tại, hệ thống tự động thêm số thứ tự (ví dụ: anhnh1).
- Người dùng có thể chỉnh sửa tên tài khoản gợi ý.
- Mật khẩu được tự sinh mặc định bởi hệ thống.
- Kiểm tra dữ liệu hợp lệ trước khi tạo tài khoản:
  + Tên tài khoản không được để trống, không trùng tài khoản
  + Email phải đúng định dạng
- Phạm vi tạo tài khoản theo cấp đơn vị của người dùng:
  + Admin: Có thể tạo tài khoản cho tất cả các đơn vị
  + CVBTP: Có thể tạo tài khoản cho đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Có thể tạo tài khoản cho đơn vị cấp 2
- Hiển thị thông báo thành công khi tạo tài khoản thành công.
- Hiển thị thông báo lỗi khi tạo tài khoản thất bại.

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý tài khoản người dùng.
- Người dùng đang ở màn hình danh sách tài khoản người dùng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng thuộc đơn vị" (**SCR_User_List**).
2. Người dùng chọn thao tác "Thêm mới tài khoản".
3. Hệ thống hiển thị form thêm mới tài khoản.
4. Người dùng nhập thông tin người dùng (Họ và tên, Email, Đơn vị thuộc danh sách người dùng có quyền truy cập).
5. Hệ thống tự động gợi ý tên tài khoản theo cú pháp: tên+viết tắt từ đầu tiên của họ và tên đệm.
6. Nếu tên tài khoản gợi ý đã tồn tại, hệ thống tự động thêm số thứ tự (ví dụ: anhnh1).
7. Người dùng có thể chỉnh sửa tài khoản gợi ý.
8. Người dùng chọn thao tác "Lưu thông tin".
9. Hệ thống kiểm tra dữ liệu hợp lệ.
10. Nếu dữ liệu hợp lệ:
    - Hệ thống tạo tài khoản người dùng mới.
    - Nếu tạo tài khoản thành công:
      - Hệ thống hiển thị thông báo "Tạo tài khoản thành công".
      - Chuyển hướng về danh sách (**SCR_User_List**).
11. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Dữ liệu không hợp lệ**:
  1. Hệ thống kiểm tra dữ liệu hợp lệ.
  2. Nếu dữ liệu không hợp lệ:
  3. Hệ thống hiển thị thông báo lỗi dữ liệu.
  4. Người dùng ở lại màn hình thêm mới (**SCR_User_Create**).
- **Lỗi hệ thống khi tạo tài khoản**:
  1. Hệ thống tạo tài khoản người dùng mới.
  2. Nếu tạo tài khoản không thành công:
  3. Hệ thống hiển thị thông báo "Tạo tài khoản thất bại".
  4. Người dùng ở lại màn hình thêm mới (**SCR_User_Create**).
- **Email đã tồn tại**: Nếu tồn tại 1 người dùng đã xác thực bằng email đó, thông báo lỗi email đã tồn tại
- **Số điện thoại đã tồn tại**: Nếu số điện thoại đã tồn tại, thông báo lỗi số điện thoại đã tồn tại

## Hậu điều kiện
- Nếu thành công: Tài khoản người dùng mới được tạo trong hệ thống.
- Nếu thất bại: Không có tài khoản nào được tạo, dữ liệu giữ nguyên trạng thái ban đầu.

## Liên kết
- Activity Diagram: [AD_User_Create.puml]
- Form liên quan: [SCR_User_Create.md]
- Entity liên quan: **ENT_NguoiDung**
- Business Rule: [BR13 - Quy tắc đặt mật khẩu mặc định]