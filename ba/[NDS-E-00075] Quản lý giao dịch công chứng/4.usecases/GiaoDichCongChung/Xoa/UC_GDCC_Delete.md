# Use Case: Xóa giao dịch công chứng

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn xóa 1 hoặc nhiều giao dịch công chứng đang ở trạng thái lưu nháp để loại bỏ những hồ sơ chưa hoàn chỉnh hoặc tạo nhầm, đảm bảo hệ thống không lưu trữ dữ liệu dư thừa.

## Acceptance Criteria
- Hệ thống kiểm tra trạng thái giao dịch, nếu giao dịch đang "Lưu nháp" thì cho phép xóa, nếu không thì không hiển thị chức năng
- Nếu không có quyền, hệ thống không hiển thị chức năng
- Khi người dùng xác nhận xóa:
  - Hệ thống xóa hồ sơ khỏi **ENT_HoSoCongChung** và cập nhật danh sách hiển thị **SCR_GDCC_List**.
  - Xóa các bên liên quan khỏi **ENT_CaNhan**, **ENT_ToChuc**.
  - Xóa tài sản giao dịch khỏi **ENT_TaiSan**.
  - Xóa tài liệu đính kèm nếu có **ENT_TaiLieu**.
  - Không xóa các giao dịch khác liên quan.
- Hiển thị thông báo "Xóa giao dịch công chứng thành công".
- Nếu người dùng không xác nhận xóa, giữ nguyên màn hình danh sách giao dịch.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Có quyền "Xóa giao dịch công chứng".
- Giao dịch đang ở trạng thái "Lưu nháp".

## Luồng chính
1. Người dùng chọn nhiều giao dịch đang ở trạng thái "Lưu nháp" để xóa
2. Hệ thống hiển thị popup xác nhận xóa giao dịch.
3. Người dùng đồng ý xóa:
4. Hệ thống thực hiện:
     - Xóa giao dịch khỏi **ENT_HoSoCongChung**.
     - Xóa các bên liên quan khỏi **ENT_CaNhan**, **ENT_ToChuc**.
     - Xóa tài sản giao dịch khỏi **ENT_TaiSan**.
     - Xóa tài liệu đính kèm nếu có **ENT_TaiLieu**.
     - Không xóa các giao dịch khác liên quan.
     - Hiển thị thông báo "Xóa giao dịch công chứng thành công".
     - Chuyển hướng về danh sách giao dịch (**SCR_GDCC_List**).
   
## Luồng phụ 
- Người dùng không đồng ý xóa, hệ thống thực hiện:
     - Đóng popup xác nhận.
     - Giữ nguyên màn hình danh sách giao dịch (**SCR_GDCC_List**).

## Ngoại lệ
- Hồ sơ không ở trạng thái "Lưu nháp": không hiển thị chức năng xóa.
- Nếu không có quyền: không hiển thị chức năng xóa.
- Lỗi hệ thống: Hiển thị thông báo "Phát sinh lỗi hệ thống, vui lòng thử lại".

## Hậu điều kiện
- Nếu thành công: giao dịch công chứng và các dữ liệu liên quan được xóa khỏi hệ thống.
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu nào bị xóa.

## Liên kết
- Activity Diagram: [AD_GDCC_Delete.puml]
- Form liên quan: [SCR_GDCC_List.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_TaiSan**, **ENT_TaiLieu**