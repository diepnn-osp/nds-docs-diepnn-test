# Use Case: Xóa bên liên quan trong form giao dịch công chứng

## User Story
- Là **Nhân viên/Công chứng TCHNCC**, trong khi tạo lập/chỉnh sửa giao dịch công chứng, tôi muốn xóa được bên liên quan, để có thể loại bỏ những thông tin đã bị tạo nhầm.

## Acceptance Criteria
- Khi người dùng chọn Xóa bên liên quan, hệ thống phải hiển thị hộp thoại xác nhận với nội dung: “Bạn có chắc chắn muốn xóa bên liên quan không?”.
- Hệ thống phải cung cấp hai lựa chọn: Xác nhận và Hủy.
- Nếu người dùng chọn Hủy, hệ thống đóng hộp thoại và bên liên quan không bị xóa.
- Nếu người dùng chọn Xác nhận, hệ thống xóa thành công bên liên quan và toàn bộ danh sách người tham gia giao dịch trong đó, hiển thị thông báo "Xóa thành công bên liên quan"
- Hệ thống phải cập nhật danh sách bên liên quan hiển thị trên form giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**) sau khi xóa thành công

## Tác nhân chính
- Nhân viên/Công chứng TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền thêm mới/Chỉnh sửa giao dịch công chứng

## Luồng chính
1. Người dùng đang thực hiện thêm mới/chỉnh sửa giao dịch công chứng (**SCR_GDCC_Update** / **SCR_GDCC_Create**).  
2. Người dùng bấm nút xóa 1 bên liên quan;
3. Hệ thống hiển thị popup xác nhận xóa.  
4. Người dùng nhấn nút "Xác nhận".  
5. Hệ thống đóng popup, xóa bên liên quan và toàn bộ người tham gia giao dịch trong đó trên form thêm mới/chỉnh sửa giao dịch công chứng (**SCR_GDCC_Update** / **SCR_GDCC_Create**).  
6. Hệ thống hiển thị thông báo kết quả "Xóa thành công bên liên quan".  
7. Use case kết thúc. 

## Luồng phụ
- Người dùng nhấn **Hủy** hoặc biểu tượng đóng popup xác nhận xóa → Hệ thống đóng popup, use case kết thúc, không có thay đổi.  

## Ngoại lệ
- Nếu có lỗi hệ thống → Hiển thị thông báo lỗi: "Hệ thống phát sinh lỗi, vui lòng thử lại", không xóa dữ liệu.  

## Hậu điều kiện
- Nếu thành công: bên liên quan bị xóa và không còn trong form giao dịch công chứng.  
- Nếu thất bại hoặc hủy: Không có thay đổi nào trong hệ thống.

## Liên kết
- Activity Diagram: [AD_BLQ_Delete.puml]
- Form/Screen: [SCR_GDCC_Create.md], [SCR_GDCC_Update.md]
- Entity liên quan: **ENT_HoSoCongChung**
