# Use Case: UC_Noti_Update (Chỉnh sửa thông báo)

## User Story
- Với vai trò là **Lãnh đạo Sở Tư Pháp, Lãnh đạo Phòng HCBTTP tại Sở TP, Chuyên viên Sở Tư Pháp**, tôi muốn chỉnh sửa Thông báo đã tạo để cập nhật tiêu đề, nội dung, file đính kèm, phạm vi gửi.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn chỉnh sửa Thông báo đã tạo để cập nhật tiêu đề, nội dung, file đính kèm, phạm vi gửi.

## Acceptance Criteria
- Hệ thống hiển thị form chỉnh sửa thông báo và điền sẵn thông tin đã lưu.
- Cho phép chỉnh sửa khi Thông báo có trạng thái **Chưa gửi**. Không cho phép chỉnh sửa khi Thông báo có trạng thái **Đã gửi**.
- Hệ thống cho phép chỉnh sửa các trường: Tiêu đề, Nội dung, Phạm vi gửi, File đính kèm (thêm/xóa).

## Tác nhân chính
- Chuyên viên STP
- Lãnh đạo STP
- Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp
- Lãnh đạo Cục BTTP
- Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đăng nhập và có quyền chỉnh sửa thông báo.
- Thông báo có trạng thái **Chưa gửi**.

## Luồng chính
1. Người dùng mở danh sách "Thông báo gửi" (**UC_Noti_List**) chọn chức năng **Chỉnh sửa** trên thông báo mong muốn.
2. Hệ thống kiểm tra quyền chỉnh sửa của người dùng.
3. Hệ thống mở màn hình chỉnh sửa (**SCR_Noti_Update**) với dữ liệu hiện tại của thông báo.
4. Người dùng chỉnh sửa dữ liệu của thông báo.
5. Hệ thống hiển thị các nút chức năgn 
- Nút **Cập nhật** để cập nhật dữ liệu mới của thông báo.
- Nút **Gửi thông báo** để cập nhật dữ liệu mới và gửi thông báo
6. Hệ thống thực hiện kiểm tra tính hợp lệ của dữ liệu:
- Nếu dữ liệu hợp lệ: Cập nhật dữ liệu mới vào **ENT_Thongbao**
- Thông báo cập nhật/ gửi thông báo thành công.
- Chuyển màn hình danh sách thông báo.
7. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Nếu dữ liệu không hợp lệ: hệ thống hiển thị lỗi chi tiết và cho phép người dùng chỉnh sửa.
- Nếu người dùng không có quyền: hiển thị "Không có quyền chỉnh sửa".
- Nếu người dùng chọn nút **Đóng**: Hiển thị popup xác nhận hủy thao tác. Nếu xác nhận, đóng form tạo mới (**SCR_Noti_Update**), không lưu dữ liệu, chuyển về màn hình danh sách **SCR_Noti_List**. Nếu hủy xác nhận, đóng popup xác nhận.

## Hậu điều kiện
- Nếu chỉnh sửa thành công: thông báo được cập nhật và log ghi lại hành động.

## Related
- Activity Diagram: **AD_Noti_Update.puml**
- Form liên quan: **SCR_Noti_Update.md**
- Entity liên quan: **ENT_Thongbao**
