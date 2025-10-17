# Use Case: UC_Sign_Create (Chỉnh sửa thông tin đăng ký)

## User Story
- Với vai trò là **Công chứng viên / Nhân viên TCHNCC**, tôi muốn có thể Chỉnh sửa thông tin chữ ký số của tổ chức công chứng.

## Acceptance Criteria
- Hệ thống hiển thị form Chỉnh sửa thông tin đăng ký chữ ký số.
- Người dùng cập nhật thông tin: 
   - Công chứng viên (nếu là loại chữ ký số cá nhân)
   - Loại chữ ký số
   - Nhà cung cấp
   - Số serial
   - Ngày hiệu lực
   - Ngày hết hạn 
   - File đính kèm
   - Ghi chú
- Hệ thống kiểm tra dữ liệu hợp lệ (thời gian hiệu lực/hết hạn, file đúng định dạng).
- Nếu hợp lệ: lưu hồ sơ đăng ký ở trạng thái **Mới tạo** hoặc **Chờ duyệt** (tùy vào Lưu nháp hay trình duyệt).
- Người dùng có thể hủy thao tác chỉnh sửa.
- Người dùng chỉ có thể chỉnh sửa bản ghi ở trạng thái **Mới tạo**, **Chờ duyệt**.

## Tác nhân chính
- Công chứng viên  
- Nhân viên TCHNCC  

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền Chỉnh sửa thông tin đăng ký.

## Luồng chính
1. Người dùng chọn chức năng **Chỉnh sửa thông tin đăng ký** bằng cách bấm vào biểu tượng chỉnh sửa trên dòng thông tin đăng ký chữ ký số (**SCR_Sign_List**) hoặc nút "Chỉnh sửa" trong trang chi tiết thông tin đăng ký.
2. Hệ thống hiển thị màn hình chỉnh sửa thông tin đăng ký (**SCR_Sign_Update**).
3. Người dùng chỉnh sửa các thông tin cần thiết.
4. Người dùng bấm nút **Trình duyệt**.
5. Hệ thống kiểm tra dữ liệu:
   - Nếu hợp lệ: lưu dữ liệu vào **ENT_ChuKySo** với trạng thái = "Chờ duyệt".
   - Hiển thị thông báo "Cập nhật thông tin đăng ký chữ ký số thành công".
   - Lịch sử đăng ký thông tin chữ ký số được cập nhật
   - Mở màn hình chi tiết chữ ký số vừa cập nhật (**UC_Sign_Detail**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Người dùng chọn **Hủy**: Hiển thị popup xác nhận hủy thao tác. Nếu xác nhận, form đóng, không lưu dữ liệu, chuyển về màn danh sách. Nếu hủy xác nhận, đóng popup xác nhận
- Nhập thiếu thông tin bắt buộc: Hiển thị cảnh báo lỗi.
- Ngày hết hạn < ngày hiệu lực: Hiển thị lỗi "Ngày hết hạn không hợp lệ".
- Trạng thái khác "Mới tạo" hoặc "Chờ duyệt": Hiển thị lỗi "Thông tin không thể chỉnh sửa".
- File đính kèm sai định dạng: Hiển thị lỗi "File không hợp lệ".
- Lỗi hệ thống: Hiển thị thông báo lỗi "Hệ thống phát sinh lỗi, vui lòng thử lại", không lưu dữ liệu.
- Người dùng chọn **Lưu nháp**: 
   - Hệ thống không thực hiện kiểm tra tính đầy đủ của dữ liệu mà chỉ kiểm tra logic, hệ thống lưu thông tin đăng ký chữ ký số với trạng thái là "Mới tạo".
   - Hiển thị thông báo "Lưu thông tin chữ ký số thành công".
   - Lịch sử đăng ký thông tin chữ ký số được cập nhật
   - Mở màn hình chi tiết chữ ký số vừa lưu (**UC_Sign_Detail**) 


## Hậu điều kiện
- Nếu thành công: Hệ thống cập nhật thông tin
- Nếu thất bại: Không có dữ liệu nào được cập nhật.

## Liên kết
- Activity Diagram: [AD_Sign_Update.puml]
- Form liên quan: [SCR_Sign_Update.md]
- Entity liên quan: **ChuKySo**, **LichSuCapNhat**
