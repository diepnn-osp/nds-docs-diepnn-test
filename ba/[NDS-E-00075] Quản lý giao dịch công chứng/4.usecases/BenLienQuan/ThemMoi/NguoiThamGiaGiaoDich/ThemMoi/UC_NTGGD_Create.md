# Use Case: Thêm mới người tham gia giao dịch

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn có thể thêm mới thông tin người tham gia giao dịch thuộc bên liên quan vào giao dịch công chứng đang lập hoặc chỉnh sửa, để đảm bảo dữ liệu người tham gia giao dịch được khai báo đầy đủ và hiển thị trên form trước khi lưu hồ sơ.

## Acceptance Criteria
- Hệ thống hiển thị popup thêm mới người tham gia giao dịch.  
- Người dùng có thể chọn thêm mới cá nhân/Tổ chức.  
- Khi người dùng lưu thành công, hệ thống hiển thị thông tin người tham gia giao dịch trên màn hình thêm mới/chỉnh sửa giao dịch công chứng ở đúng bên liên quan.  
- Nếu dữ liệu không hợp lệ, hiển thị thông báo lỗi cụ thể.  
- Người dùng có thể hủy thao tác thêm mới.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập.  
- Người dùng có quyền "Thêm mới/Chỉnh sửa giao dịch công chứng".  
- Người dùng đang thao tác trong form thêm mới hoặc chỉnh sửa giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).
- Đã thêm bên liên quan  

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới người tham gia giao dịch** trong form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).  
2. Hệ thống hiển thị popup thêm mới người tham gia giao dịch (**SCR_NTGGD_Create**).  
3. Hệ thống hiển thị ô lựa chọn cá nhân/tổ chức.  
4. Người dùng chọn cá nhân/tổ chức.  
5. Hệ thống hiển thị các trường thông tin tương ứng với cá nhân/tổ chức.  
6. Người dùng nhập thông tin chi tiết người tham gia giao dịch.  
7. Người dùng bấm **Lưu**.  
8. Hệ thống kiểm tra tính hợp lệ của dữ liệu và các trường thông tin bắt buộc:
9. Nếu hợp lệ và đầy đủ:  
     - Ghi nhận dữ liệu người tham gia giao dịch vào form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).  
     - Thông báo "Thêm mới người tham gia giao dịch thành công".  
     - Hiển thị lại danh sách người tham gia giao dịch trên form giao dịch.   
10. Kết thúc use case.  

## Luồng phụ 
- Người dùng chọn **Hủy**  
  - Hiển thị popup xác nhận hủy thao tác.  
  - Nếu xác nhận, đóng popup và quay lại form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**) mà không ghi nhận dữ liệu.  
  - Nếu hủy xác nhận, đóng popup xác nhận, người dùng ở lại popup thêm mới người tham gia giao dịch.  

## Ngoại lệ
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo lỗi "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".  
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".  
- Nếu chưa điền đầy đủ thông tin bắt buộc: Hiển thị thông báo yêu cầu nhập thông tin bắt buộc. 

## Hậu điều kiện
- Nếu thành công: người tham gia giao dịch mới được thêm vào danh sách của bên liên quan trong form giao dịch công chứng.  
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu người tham gia giao dịch nào được thêm mới.  

## Liên kết
- Activity Diagram: [AD_NTGGD_Create.puml]  
- Form liên quan: [SCR_NTGGD_Create.md], [SCR_GDCC_Update.md], [SCR_GDCC_Create.md]  
- Entity liên quan:  **ENT_CaNhan**, **ENT_ToChuc**, **ENT_HoSoCongChung**
