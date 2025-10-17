# Use Case: Thêm mới bên liên quan

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn có thể thêm mới thông tin bên liên quan vào giao dịch công chứng đang lập hoặc chỉnh sửa, để đảm bảo các bên tham gia giao dịch được khai báo đầy đủ và hiển thị trên form trước khi lưu giao dịch.

## Acceptance Criteria
- Hệ thống thêm mới thành công 1 khối bên liên quan mới .
- Hệ thống hiển thị các nút thao tác:
  - "Thêm người tham gia giao dịch"
  - "Xóa bên liên quan"
  - Ô lựa chọn thông tin bên liên quan (ví dụ: người đại diện).
- Danh sách thông tin bên liên quan được lọc theo **tên giao dịch công chứng** đã chọn trong giao dịch.
- Người dùng có thể chọn thông tin bên liên quan từ danh sách.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập.
- Người dùng có quyền "Thêm mới/Chỉnh sửa giao dịch công chứng".
- Người dùng đang thao tác trong form thêm mới hoặc chỉnh sửa giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới** bên liên quan trong form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).
2. Hệ thống thêm một khối bên liên quan mới bên dưới.
3. Hệ thống hiển thị:
   - Nút "Thêm người tham gia giao dịch" (**UC_NTGGD_Create**)
   - Nút "Xóa bên liên quan" (**UC_BLQ_Delete**)
   - Ô lựa chọn thông tin bên liên quan.
4. Hệ thống lọc danh sách thông tin bên liên quan theo **tên giao dịch công chứng** đã chọn.
5. Người dùng chọn bên liên quan từ danh sách, hệ thống hiển thị kết quả trong form giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).
6. Người dùng có thể lựa chọn:
   - Thêm mới 1 bên liên quan nữa
   - Thêm mới người tham gia giao dịch (**UC_NTGGD_Create**) 
7. Kết thúc use case.

## Luồng phụ
- Nếu người dùng đã chọn 1 bên liên quan từ danh sách (Ví dụ: bên ủy quyền), thông tin này sẽ bị ẩn đi ở các bên liên quan khác.

## Ngoại lệ
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".

## Hậu điều kiện
- Nếu thành công: bên liên quan mới được hiển thị trong form giao dịch công chứng.
- Nếu thất bại: không có dữ liệu bên liên quan nào được thêm mới.

## Liên kết
- Activity Diagram: [AD_BLQ_Create.puml]  
- Form liên quan: [SCR_GDCC_Create.md], [SCR_GDCC_Update.md]  
- Entity liên quan: **ENT_HoSoCongChung**