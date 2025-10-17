# Use Case: Chỉnh sửa người tham gia giao dịch

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn có thể chỉnh sửa thông tin người tham gia giao dịch trong giao dịch công chứng đang tạo lập hoặc chỉnh sửa, để đảm bảo dữ liệu người tham gia giao dịch được khai báo chính xác.

## Acceptance Criteria
- Hệ thống hiển thị popup chỉnh sửa người tham gia giao dịch, hiển thị dữ liệu đã lưu.  
- Khi người dùng lưu thành công, hệ thống hiển thị thông tin đã cập nhật trên danh sách người tham gia giao dịch.  
- Nếu dữ liệu không hợp lệ, hiển thị thông báo lỗi cụ thể.  
- Người dùng có thể hủy thao tác chỉnh sửa.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập.  
- Người dùng có quyền "Thêm mới/Chỉnh sửa giao dịch công chứng".  
- Người dùng đang thao tác trong form thêm mới hoặc chỉnh sửa giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).
- Đã thêm bên liên quan  

## Luồng chính
1. Người dùng chọn chức năng **chỉnh sửa** 1 người tham gia giao dịch trong form giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).  
2. Hệ thống hiển thị popup chỉnh sửa người tham gia giao dịch (**SCR_NTGGD_Update**).  
3. Hệ thống hiển thị dữ liệu đã lưu.  
4. Người dùng cập nhật thông tin chi tiết người tham gia giao dịch.  
5. Người dùng bấm **Lưu**.  
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu và các trường thông tin bắt buộc:
7. Nếu dữ liệu hợp lệ và thông tin đã điền đầy đủ:  
     - Cập nhật dữ liệu người tham gia giao dịch vào form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).  
     - Thông báo "Chỉnh sửa người tham gia giao dịch thành công".  
     - Hiển thị lại danh sách người tham gia giao dịch trên form giao dịch.  
8. Kết thúc use case.  

## Luồng phụ 
- Người dùng chọn **Hủy**  
  - Hiển thị popup xác nhận hủy thao tác.  
  - Nếu xác nhận, đóng popup và quay lại form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**) mà không ghi nhận dữ liệu.  
  - Nếu hủy xác nhận, đóng popup xác nhận, người dùng ở lại popup chỉnh sửa người tham gia giao dịch.   

## Ngoại lệ
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo lỗi "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".  
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".  
- Nếu chưa điền đầy đủ thông tin bắt buộc: Hiển thị thông báo yêu cầu nhập thông tin bắt buộc.

## Hậu điều kiện
- Nếu thành công: cập nhật thành công thông tin người tham gia giao dịch.  
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu người tham gia giao dịch nào được chỉnh sửa.  

## Liên kết
- Activity Diagram: [AD_NTGGD_Update.puml]  
- Form liên quan: [SCR_NTGGD_Update.md], [SCR_GDCC_Update.md], [SCR_GDCC_Create.md]
- Entity liên quan:  **ENT_CaNhan**, **ENT_ToChuc**, **ENT_HoSoCongChung**