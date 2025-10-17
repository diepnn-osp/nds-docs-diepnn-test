# Use Case: UC_Noti_Delete (Xóa thông báo)

## User Story
- Với vai trò là **Công chứng viên / Nhân viên TCHNCC**, tôi muốn xóa Thông báo đã tạo để bỏ những bản ghi đã bị tạo nhầm.
- Với vai trò là **Lãnh đạo Sở Tư Pháp, Lãnh đạo Phòng HCBTTP tại Sở TP, Chuyên viên Sở Tư Pháp**, tôi muốn xóa Thông báo đã tạo để bỏ những bản ghi đã bị tạo nhầm.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xóa Thông báo đã tạo để bỏ những bản ghi đã bị tạo nhầm.

## Acceptance Criteria
- Khi người dùng chọn xóa, hệ thống hiển thị popup xác nhận với nội dung "Xác nhận xóa thông báo này?" (thao tác: Xác nhận / Hủy).
- Chỉ cho phép xóa nếu thông báo có trạng thái "Chưa gửi".
- Nếu không đáp ứng điều kiện xóa: hệ thống hiển thị thông báo "Không thể xóa thông báo".
- Sau xóa thành công: bản ghi thông báo bị xóa , danh sách **SCR_Noti_List** được cập nhật và hệ thống ghi nhật ký (audit).

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
- Người dùng đã đăng nhập và có quyền thực hiện xóa thông báo.

## Luồng chính
1. Người dùng truy cập danh sách thông báo **UC_Noti_List** và chọn nút **Xóa** trên dòng thông báo cần xóa.
2. Hệ thống hiển thị hộp xác nhận (popup): "Xác nhận xóa thông báo này?" với hai lựa chọn Xác nhận và Hủy.
3. Người dùng chọn Xác nhận.
4. Hệ thống kiểm tra:
   - Người dùng có quyền xóa không?
   - Thông báo đang ở trạng thái cho phép xóa không? 
5. Nếu tất cả điều kiện đều hợp lệ, hệ thống xóa bản ghi thông báo, xoá bản ghi trong  **ENT_Thongbao**.
6. Hệ thống ghi lại hành động vào audit log.
7. Hệ thống cập nhật và trả về danh sách thông báo mới trên **SCR_Noti_List** và hiển thị thông báo thành công: "Xóa thông báo thành công".
8. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Người dùng chọn **Hủy** trên popup: đóng popup, không thực hiện xóa, két thúc use case.
- Nếu người dùng không có quyền xóa: hiển thị "Không có quyền xóa thông báo" và không thực hiện xóa.
- Nếu trạng thái thông báo là "Đã gửi": hiển thị "Không thể xóa thông báo".

## Hậu điều kiện
- Nếu xóa thành công: thông báo bị xóa (hoặc đánh dấu deleted), audit log được ghi, **SCR_Noti_List** cập nhật danh sách mới.
- Nếu xóa không thành công: không có thay đổi dữ liệu, người dùng nhận thông báo lỗi phù hợp.

## Liên kết (Related)
- Activity Diagram: **AD_Noti_Delete.puml**
- Form liên quan: **SCR_Noti_Delete.md**
- Entity liên quan: **ENT_Thongbao**


