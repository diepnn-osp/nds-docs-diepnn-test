# Use Case: User_List (Xem danh sách tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn xem danh sách tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn xem danh sách tài khoản người dùng theo phân quyền để thực hiện công việc trong phạm vi quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn xem danh sách tài khoản người dùng theo phân quyền để thực hiện công việc trong phạm vi quản lý.

## Acceptance Criteria
- Hệ thống hiển thị danh sách tài khoản người dùng với các trường: STT, Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái.
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống phải cung cấp phân trang (10 bản ghi 1 trang).
- Từ danh sách, người dùng có thể thực hiện các thao tác tùy theo phân quyền:
  + Xem chi tiết (nếu có quyền)
  + Sửa (nếu có quyền)
  + Xóa (nếu có quyền)
  + Đổi mật khẩu (nếu có quyền)
  + Gán/Xóa vai trò (nếu có quyền)
- Hiển thị thông báo lỗi nếu không tải được dữ liệu.
- Danh sách tài khoản người dùng hiển thị theo thứ tự thời gian cập nhật từ mới tới cũ nhất.
- Nếu có lỗi tải dữ liệu, hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Hệ thống cho phép tìm kiếm tài khoản người dùng (chi tiết tại **SCR_User_Search.md**)
- Nếu không có tài khoản người dùng nào trong hệ thống, hiển thị thông báo "Không có dữ liệu tài khoản người dùng".
- Phạm vi hiển thị danh sách theo cấp đơn vị của người dùng:
  + Admin: Xem tất cả tài khoản trong hệ thống
  + CVBTP: Xem tài khoản trong đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Xem tài khoản trong đơn vị cấp 2
  + CCV: Không có quyền xem danh sách

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng".
2. Hệ thống kiểm tra quyền truy cập theo vai trò (Admin, CVBTP, CVSTP, CCV).
3. Nếu có quyền truy cập
   - Hệ thống tải danh sách tài khoản người dùng theo phạm vi quyền.
   - Nếu tải dữ liệu thành công:
     + Nếu có dữ liệu:
       * Sắp xếp theo thời gian cập nhật (mới → cũ).
       * Nếu số lượng bản ghi lớn hơn 10, hệ thống thực hiện phân trang, 10 bản ghi mỗi trang.
       * Hiển thị danh sách với các trường: STT, Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái.
     + Nếu không có dữ liệu:
       * Hiển thị thông báo "Không có dữ liệu tài khoản người dùng".
   - Nếu không tải được dữ liệu:
     + Hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
4. Nếu không có quyền truy cập
   - Hệ thống ẩn menu "Quản lý tài khoản người dùng" khi người dùng đăng nhập.
5. Kết thúc.

## Luồng phụ/ Ngoại lệ
- Nếu có lỗi tải danh sách: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không có dữ liệu: hiển thị thông báo "Không có dữ liệu tài khoản người dùng".
- Nếu không quyền truy cập: ẩn menu "Quản lý tài khoản người dùng" khi người dùng đăng nhập.

## Hậu điều kiện
- Nếu thành công: Người dùng xem được danh sách tài khoản người dùng theo phạm vi quyền.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_User_List.puml]
- Form liên quan: [SCR_User_List.md]
- Entity liên quan: **ENT_NguoiDung**