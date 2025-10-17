# Use Case: User_Search (Tìm kiếm thông tin tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn tìm kiếm thông tin tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn tìm kiếm thông tin tài khoản người dùng để thực hiện công việc trong phạm vi quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn tìm kiếm thông tin tài khoản người dùng để thực hiện công việc trong phạm vi quản lý.

## Acceptance Criteria
- Cho phép người dùng tìm kiếm thông tin tài khoản người dùng từ danh sách.
- Hệ thống hỗ trợ tìm kiếm theo các tiêu chí: Tên tài khoản, Họ và tên, Email.
- Kiểm tra tiêu chí tìm kiếm hợp lệ trước khi thực hiện tìm kiếm.
- Tìm kiếm chỉ thực hiện trong phạm vi quyền truy cập của người dùng:
  + Admin: Tìm kiếm trong tất cả tài khoản trong hệ thống
  + CVBTP: Tìm kiếm trong tài khoản thuộc đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Tìm kiếm trong tài khoản thuộc đơn vị cấp 2
- Hiển thị danh sách kết quả tìm kiếm với các trường: STT, Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái.
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống phải cung cấp phân trang (10 bản ghi 1 trang).
- Từ danh sách kết quả, người dùng có thể thực hiện các thao tác tùy theo phân quyền:
  + Xem chi tiết
  + Sửa (nếu có quyền)
  + Xóa (nếu có quyền)
  + Đổi mật khẩu (nếu có quyền)
  + Gán/Xóa vai trò (nếu có quyền)
- Hiển thị thông báo khi không tìm thấy kết quả phù hợp.
- Hiển thị thông báo lỗi khi tìm kiếm thất bại.

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách tài khoản người dùng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng" (**SCR_User_List**).
2. Người dùng nhập tiêu chí tìm kiếm (Tên tài khoản, Họ và tên, Email).
3. Người dùng chọn thao tác "Tìm kiếm".
4. Hệ thống kiểm tra tiêu chí tìm kiếm hợp lệ.
5. Nếu tiêu chí tìm kiếm hợp lệ:
   - Hệ thống tìm kiếm tài khoản người dùng theo phạm vi quyền.
   - Nếu tìm kiếm thành công:
     + Nếu có kết quả tìm kiếm:
       * Hiển thị danh sách kết quả tìm kiếm với các trường: STT, Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái.
       * Nếu số lượng bản ghi lớn hơn 10, hệ thống thực hiện phân trang, 10 bản ghi mỗi trang.
     + Nếu không có kết quả tìm kiếm:
       * Hiển thị thông báo "Không tìm thấy tài khoản phù hợp".
   - Nếu tìm kiếm không thành công:
     + Hiển thị thông báo "Tìm kiếm thất bại, vui lòng thử lại".
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Tiêu chí tìm kiếm không hợp lệ**:
  1. Hệ thống kiểm tra tiêu chí tìm kiếm hợp lệ.
  2. Nếu tiêu chí tìm kiếm không hợp lệ:
  3. Hệ thống hiển thị thông báo lỗi tìm kiếm.
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).
- **Tìm kiếm thất bại**:
  1. Hệ thống tìm kiếm tài khoản người dùng theo phạm vi quyền.
  2. Nếu tìm kiếm không thành công:
  3. Hệ thống hiển thị thông báo "Tìm kiếm thất bại, vui lòng thử lại".
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).
- **Không tìm thấy kết quả**:
  1. Hệ thống tìm kiếm tài khoản người dùng theo phạm vi quyền.
  2. Nếu không có kết quả tìm kiếm:
  3. Hệ thống hiển thị thông báo "Không tìm thấy tài khoản phù hợp".
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).

## Hậu điều kiện
- Nếu thành công: Người dùng xem được danh sách kết quả tìm kiếm tài khoản người dùng theo phạm vi quyền.
- Nếu thất bại: Không hiển thị kết quả, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_User_Search.puml]
- Form liên quan: [SCR_User_List.md]
- Entity liên quan: **ENT_NguoiDung**