# Use Case: UC_Noti_List (Xem danh sách thông báo)

## User Story
- Với vai trò là **Công chứng viên / Nhân viên TCHNCC**, tôi muốn xem danh sách Thông báo được gửi bởi Bộ Tư pháp, Sở Tư pháp để nắm bắt thông tin, hướng dẫn liên quan.
- Với vai trò là **Lãnh đạo Sở Tư Pháp, Lãnh đạo Phòng HCBTTP tại Sở TP, Chuyên viên Sở Tư Pháp**, tôi muốn xem danh sách Thông báo được gửi bởi Bộ Tư pháp, nội bộ Sở Tư pháp để nắm bắt thông tin, hướng dẫn liên quan.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem danh sách Thông báo được gửi bởi Bộ Tư pháp để nắm bắt thông tin, hướng dẫn liên quan.

## Acceptance Criteria
- Hệ thống hiển thị danh sách thông báo với 2 tab: "Thông báo gửi" và "Thông báo nhận", mặc định hiển thị danh sách thông báo tab "Thông báo nhận".
- Tab "Thông báo gửi" hiển thị danh sách Thông báo có người gửi là tài khoản đang thao tác.
- Tab "Thông báo gửi" hiển thị các trường: Tiêu đề, Nội dung thông báo, Người gửi, Loại thông báo, Ngày gửi, Trạng thái (Chưa gửi/ Đã gửi), Chức năng (Xem, sửa, xóa).
- Tab "Thông báo gửi" ẩn hiển thị đối với tài khoản thuộc đơn vị **TCHNCC**.
- Tab "Thông báo nhận" hiển thị danh sách Thông báo có người gửi là tài khoản khác tài khoản đang thao tác.
- Tab "Thông báo nhận" hiển thị các trường: Tiêu đề, Nội dung thông báo, Người gửi, Loại thông báo, Ngày gửi, Trạng thái (Đã đọc/ Chưa đọc), Chức năng (Xem)
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống thực hiện phân trang dữ liệu (10 bản ghi 1 trang).
- Danh sách thông báo số hiển thị theo thứ tự thời gian cập nhật từ mới tới cũ nhất.
- Hệ thống cho phép tìm kiếm thông báo (chi tiết trong **UC_Noti_Search**).    

## Tác nhân chính
- Công chứng viên
- Nhân viên TCHNCC
- Chuyên viên STP
- Lãnh đạo STP
- Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp
- Lãnh đạo Cục BTTP
- Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập và tài khoản có quyền truy cập chức năng Xem thông báo.

## Luồng chính
1. Người dùng mở menu chọn "Quản lý thông báo".
2. Hệ thống kiểm tra phân quyền tài khoản người dùng (lấy dữ liệu từ **ENT_Nguoidung**).
3. Hệ thống mặc định hiển thị danh sách "Thông báo nhận":
- Nếu người dùng thuộc Bộ, Hệ thống tải toàn bộ danh sách danh sách Thông báo được gửi bởi Bộ Tư pháp.
- Nếu người dùng thuộc Sở, Đơn vị thuộc quản lý cấp Bộ Hệ thống tải danh sách danh sách Thông báo được gửi bởi Bộ Tư pháp, nội bộ Sở Tư pháp.
- Nếu người dùng thuộc tổ chức công chứng, Hệ thống tải danh sách danh sách Thông báo được gửi bởi Bộ Tư pháp, Sở Tư pháp, nội bộ TCHNCC.
4. Người dùng chọn xem tab thông báo
- "Thông báo nhận", hệ thống hiển thị danh sách Thông báo gửi (**SCR_Noti_List_Received**)
- "Thông báo gửi", hệ thống hiển thị danh sách Thông báo gửi (**SCR_Noti_List_Sent**)
5. Hệ thống hiển thị màn hình danh sách đăng theo thứ tự thời gian cập nhật từ mới tới cũ nhất **BR2. Hiển thị** (lấy dữ liệu từ **ENT_Thongbao**).
6. Nếu số lượng bản ghi lớn hơn 10, hệ thống thực hiện phân trang **BR1. Phân trang dữ liệu**
7. Người dùng có thể:
   - Chuyển đổi giữa 2 tab "Thông báo nhận" và "Thông báo gửi"
   - Chọn xem trang tiếp theo/ trước, hệ thống sẽ hiển thị bản ghi của trang tương ứng
   - Tìm kiếm (**UC_Noti_Search**)
   - Xem chi tiết (**UC_Noti_Detail**)
   - Đối với tab "Thông báo gửi": người dùng có thể Chỉnh sửa (**UC_Noti_Update**), Xóa (**UC_Noti_Delete**)
8. Kết thúc.

## Luồng phụ/ Ngoại lệ
- Nếu có lỗi tải danh sách: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không có dữ liệu: hiển thị "Không có dữ liệu thông báo".
- Nếu không quyền truy cập: hiển thị "Không có quyền truy cập" và ẩn đi menu "Quản lý thông báo".

## Hậu điều kiện
- Nếu thành công: Người dùng xem được danh sách thông báo.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Related
- Activity Diagram: **AD_Noti_List.puml**
- Form/Screen: **SCR_Noti_List.md**
- Entity liên quan: **ENT_Thongbao**