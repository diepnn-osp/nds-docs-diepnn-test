# Use Case: UC_Noti_Create (Tạo mới thông báo)

## User Story
- Với vai trò là **Công chứng viên / Nhân viên TCHNCC**, tôi muốn tạo và gửi Thông báo đến nội bộ TCHNCC để truyền đạt thông tin, hướng dẫn hoặc yêu cầu.
- Với vai trò là **Lãnh đạo Sở Tư Pháp, Lãnh đạo Phòng HCBTTP tại Sở TP, Chuyên viên Sở Tư Pháp**, tôi muốn tạo và gửi Thông báo đến nội bộ Sở Tư pháp, các TCHNCC để truyền đạt thông tin, hướng dẫn hoặc yêu cầu.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn tạo và gửi Thông báo đến nội bộ Bộ Tư pháp, Sở tư pháp, các TCHNCC để truyền đạt thông tin, hướng dẫn hoặc yêu cầu.

## Acceptance Criteria
- Người dùng có phân quyền tạo thông báo (**SCR_Noti_Create**).
- Trường bắt buộc của thông báo: Tiêu đề, Nội dung, Loại thông báo.
- Trường hợp Loại thông báo = Thông báo nội bộ => Danh sách người nhận có cùng đơn vị với người gửi thông báo 
- Trường hợp Loại thông báo = Thông báo gửi Sở Tư Pháp => Hiển thị giá trị khi người dùng thuộc đơn vị Bộ Tư pháp, Đối tượng nhận thông báo là toàn bộ người dùng thuộc đơn vị Sở Tư pháp
- Trường hợp Loại thông báo = Thông báo gửi TCHNCC => Hiển thị giá trị khi người dùng thuộc đơn vị Bộ Tư pháp hoặc Sở Tư pháp, Đối tượng nhận thông báo là toàn bộ người dùng thuộc đơn vị TCHNCC được chọn
- Hỗ trợ thêm danh sách file đính kèm.
- Trạng thái thông báo:
    - Trường hợp người dùng chọn **Lưu nháp**, trạng thái của thông báo = Chưa gửi
    - Trường hợp người dùng chọn **Gửi thông báo**, trạng thái của thông báo = Đã gửi
- Khi người dùng gửi thông báo thành công, trạng thái thông báo hiển thị trên tab "Thông báo nhận" của tài khoản nhận thông báo có trạng thái "Chưa đọc".


## Tác nhân chính
- Chuyên viên STP
- Lãnh đạo STP
- Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp
- Lãnh đạo Cục BTTP
- Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền tạo thông báo.

## Luồng chính
1. Người dùng mở màn hình danh sách thông báo **UC_Noti_List** và chọn **Thêm mới thông báo**.
2. Hệ thống hiển thị form tạo mới (**SCR_Noti_Create**).
3. Người dùng nhập thông tin trên form.
4. Người dùng bấm nút **Lưu nháp** hoặc **Gửi thông báo**.
5. Hệ thống thực hiện kiểm tra tính hợp lệ của dữ liệu:
    - Nếu chọn **Lưu nháp** và dữ liệu hợp lệ: hệ thống lưu thông báo mới với trạng thái **Chưa gửi**, và hiển thị thông báo thành công. Thêm mới dữ liệu vào **ENT_Thongbao**.
    - Nếu chọn **Gửi thông báo** và dữ liệu hợp lệ: Hệ thống lưu thông báo mới với trạng thái **Đã gửi**, và hiển thị thông báo thành công. Thêm mới dữ liệu vào **ENT_Thongbao**.
6. Hệ thống chuyển về màn hình Danh sách thông báo **SCR_Noti_List**.
7. Kết thúc use case.    

## Luồng phụ / Ngoại lệ
- Nếu người dùng không có quyền tạo thông báo: hiển thị "Không có quyền truy cập".
- Nếu dữ liệu không hợp lệ: hệ thống hiển thị lỗi chi tiết và cho phép người dùng chỉnh sửa.
- Nếu người dùng chọn nút **Đóng**: Hiển thị popup xác nhận hủy thao tác. Nếu xác nhận, đóng form tạo mới (**SCR_Noti_Create**), không lưu dữ liệu, chuyển về màn hình danh sách **SCR_Noti_List**. Nếu hủy xác nhận, đóng popup xác nhận.

## Hậu điều kiện
- Nếu Tạo, gửi thông báo thành công: Cập nhật dữ liệu thông báo mới vào **ENT_Thongbao**.

## Liên kết
- Use cases: **UC_Noti_List**
- Activity Diagram: **AD_Noti_Create.puml**
- Form liên quan: **SCR_Noti_Create.md**
- Entity liên quan: **ENT_Thongbao**

