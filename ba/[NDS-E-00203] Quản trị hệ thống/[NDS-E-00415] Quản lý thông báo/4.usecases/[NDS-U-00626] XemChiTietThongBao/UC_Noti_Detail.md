# Use Case: UC_Noti_Detail_Sent (Xem chi tiết thông báo gửi)

## User Story
- Với vai trò là **Lãnh đạo Sở Tư Pháp, Lãnh đạo Phòng HCBTTP tại Sở TP, Chuyên viên Sở Tư Pháp**, tôi muốn xem chi tiết Thông báo được tạo để gửi nội bộ Sở Tư pháp, TCHNCC để nắm bắt, điều chỉnh nội dung thông tin, hướng dẫn liên quan.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem chi tiết Thông báo được tạo để gửi nội bộ Bộ Tư pháp, Sở Tư pháp, TCHNCC để nắm bắt toàn, điều chỉnh nội dung thông tin, hướng dẫn liên quan.

## Acceptance Criteria
- Khi người dùng chọn 1 thông báo trong danh sách "Thông báo gửi" **UC_Noti_List**, hệ thống hiển thị màn hình chi tiết thông báo **SCR_Noti_Detail_Sent** được chọn từ danh sách.
- Danh sách thông báo chỉ hiển thị danh sách Thông báo có người gửi là tài khoản đang thao tác.
- Các trường thông tin bao gồm:
   - Tên cơ quan gửi thông báo
   - Người gửi (họ tên, đơn vị công tác)
   - Ngày gửi
   - Phạm vi gửi thông báo
   - Tiêu đề thông báo
   - Nội dung thông báo
   - Danh sách file đính kèm (cho phép tải về từng file)
- Người dùng có thể thực hiện Chỉnh sửa, Gửi thông báo khi thông báo có trạng thái **Chưa gửi**
- Người dùng có thể quy lại danh sách Thông báo.

## Tác nhân chính
- Chuyên viên STP
- Lãnh đạo STP
- Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp
- Lãnh đạo Cục BTTP
- Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách thông báo. Người dùng chọn tab "Thông báo gửi".
2. Người dùng truy cập trang chi tiết thông báo bằng cách chọn button "Xem chi tiết".
- Trạng thái thông báo = Đã gửi, hệ thống hiển thị màn hình **SCR_Noti_Detail.md**
3. Hệ thống hiển thị màn hình chi tiết thông báo bao gồm các thông tin:
   - Tên cơ quan gửi thông báo
   - Người gửi
   - Ngày gửi
   - Loại thông báo
   - Tiêu đề thông báo
   - Nội dung thông báo
   - Danh sách file đính kèm
4. Hệ thống hiển thị các nút chức năng
   - Nút Đóng => Bấm vào chuyển về màn hình danh sách thông báo
5. Kết thúc.

## Luồng phụ/ Ngoại lệ
- Trạng thái thông báo = Chưa gửi, hệ thống hiển thị màn hình **SCR_Noti_Update.md**, **UC_Noti_Update**
- Nếu không có file đính kèm: hiển thị "Không có file đính kèm".
- Nếu thông báo đã bị xóa: hiển thị "Thông báo đã bị xóa".
- Nếu không quyền truy cập: hiển thị "Không có quyền truy cập" và không tải dữ liệu.
- Khi tài khoản có thông báo mới hiển thị popup **SCR_Noti_Popup.md**, người dùng chọn vào popup để xem chi tiết thông báo.

## Hậu điều kiện
- Nếu thành công: Người dùng xem được chi tiết thông báo.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Related
- Activity Diagram: **AD_Noti_Detail.puml**
- Form/Screen: **SCR_Noti_Detail.md**, **SCR_Noti_Popup.md**
- Entity liên quan: **ENT_Thongbao**