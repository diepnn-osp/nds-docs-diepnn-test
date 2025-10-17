# Use Case: User_View (Xem chi tiết thông tin tài khoản người dùng)

## User Story
- Với vai trò là **Quản trị hệ thống**, tôi muốn xem chi tiết thông tin tài khoản người dùng để quản lý thông tin toàn hệ thống.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn xem chi tiết thông tin tài khoản người dùng theo phân quyền để thực hiện công việc trong phạm vi quản lý.
- Với vai trò là **Chuyên viên STP**, tôi muốn xem chi tiết thông tin tài khoản người dùng theo phân quyền để thực hiện công việc trong phạm vi quản lý.
- Với vai trò là **Công chứng viên**, tôi muốn xem chi tiết thông tin tài khoản của chính mình.

## Acceptance Criteria
- Cho phép người dùng xem chi tiết thông tin tài khoản người dùng từ danh sách.
- Hiển thị popup xem chi tiết với các thông tin: Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái, Thời gian tạo, Thời gian cập nhật gần nhất, Lịch sử đăng nhập gần nhất, Danh sách các vai trò được gán.
- Popup chỉ có thao tác "Đóng".
- Các thao tác quản lý (sửa, xóa, đổi mật khẩu, gán/xóa vai trò) được thực hiện từ danh sách, không phải trong popup.
- Người dùng đã có quyền xem danh sách tài khoản người dùng sẽ tự động có quyền xem chi tiết các tài khoản trong phạm vi quyền của họ.
- Hiển thị thông báo lỗi nếu không tải được thông tin tài khoản.
- Phạm vi hiển thị chi tiết theo cấp đơn vị của người dùng:
  + Admin: Xem chi tiết tất cả tài khoản trong hệ thống
  + CVBTP: Xem chi tiết tài khoản trong đơn vị cấp 1 và cấp 2 thuộc quyền quản lý
  + CVSTP: Xem chi tiết tài khoản trong đơn vị cấp 2
  + CCV: Chỉ xem chi tiết tài khoản của chính mình

## Tác nhân chính
- Quản trị hệ thống
- Chuyên viên Cục BTTP
- Chuyên viên STP
- Công chứng viên

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách tài khoản người dùng.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách tài khoản người dùng" (**SCR_User_List**).
2. Người dùng chọn tài khoản người dùng cần xem chi tiết.
3. Hệ thống tải thông tin chi tiết tài khoản người dùng.
4. Nếu tải dữ liệu thành công:
   - Hệ thống hiển thị popup xem chi tiết thông tin tài khoản người dùng (**SCR_User_View**).
   - Popup hiển thị các thông tin: Tên tài khoản, Họ và tên, Email, Vai trò, Đơn vị, Trạng thái, Thời gian tạo, Thời gian cập nhật gần nhất, Lịch sử đăng nhập gần nhất, Danh sách các vai trò được gán.
   - Popup chỉ có thao tác "Đóng".
   - Người dùng chọn "Đóng" popup.
   - Hệ thống đóng popup xem chi tiết, quay về danh sách tài khoản người dùng (**SCR_User_List**).
5. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Lỗi hệ thống khi tải thông tin**:
  1. Hệ thống tải thông tin chi tiết tài khoản người dùng.
  2. Nếu không tải được thông tin:
  3. Hệ thống hiển thị thông báo "Không tải được thông tin tài khoản, vui lòng thử lại".
  4. Người dùng ở lại màn hình danh sách (**SCR_User_List**).

## Hậu điều kiện
- Nếu thành công: Người dùng xem được thông tin chi tiết tài khoản người dùng trong phạm vi quyền.
- Nếu thất bại: Không hiển thị thông tin chi tiết, hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_User_View.puml]
- Form liên quan: [SCR_User_View.md]
- Entity liên quan: **ENT_NguoiDung**