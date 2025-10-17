# Use Case: Chỉnh sửa thông tin tài sản

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn có thể chỉnh sửa thông tin tài sản đã thêm vào giao dịch công chứng đang lập hoặc chỉnh sửa, để đảm bảo dữ liệu tài sản được khai báo đầy đủ và chính xác trước khi lưu hồ sơ.

## Acceptance Criteria
- Hệ thống hiển thị popup chỉnh sửa thông tin tài sản và đổ ra dữ liệu.  
- Khi người dùng lưu thành công, hệ thống hiển thị thông tin tài sản giao dịch trên màn hình thêm mới/chỉnh sửa giao dịch công chứng.  
- Nếu dữ liệu không hợp lệ, hiển thị thông báo lỗi cụ thể.  
- Người dùng có thể hủy thao tác chỉnh sửa thông tin.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập.  
- Người dùng có quyền "Thêm mới/Chỉnh sửa giao dịch công chứng".  
- Người dùng đang thao tác trong form chỉnh sửa thông tin hoặc tạo lập giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**).  

## Luồng chính
1. Người dùng chọn chức năng **Chỉnh sửa thông tin tài sản** trong form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).  
2. Hệ thống hiển thị popup chỉnh sửa thông tin tài sản (**SCR_TSGD_Update**).  
3. Người dùng cập nhật thông tin chi tiết tài sản.  
4. Người dùng bấm **Lưu**.  
5. Hệ thống kiểm tra tính hợp lệ và các trường thông tin bắt buộc:
6. Nếu hợp lệ và đầy đủ:  
     - Cập nhật dữ liệu tài sản trong form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).  
     - Thông báo "Cập nhật thông tin tài sản thành công".  
     - Hiển thị lại danh sách tài sản trên form hồ sơ.  
7. Kết thúc use case.  

## Luồng phụ
- Người dùng chọn **Hủy**  
  - Hiển thị popup xác nhận hủy thao tác.  
  - Nếu xác nhận, đóng popup và quay lại form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**) mà không ghi nhận dữ liệu tạm.  
  - Nếu hủy xác nhận, đóng popup xác nhận, người dùng ở lại popup chỉnh sửa thông tin tài sản.  

## Ngoại lệ
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo lỗi "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".  
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".  
- Nếu chưa điền đầy đủ thông tin bắt buộc: Hiển thị thông báo yêu cầu nhập thông tin bắt buộc. 

## Hậu điều kiện
- Nếu thành công: tài sản được cập nhật thông tin.  
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu tài sản nào được cập nhật.  

## Liên kết
- Activity Diagram: [AD_TSGD_Update.puml]  
- Form liên quan: [SCR_TSGD_Update.md], [SCR_GDCC_Update.md], [SCR_GDCC_Create.md] 
- Entity liên quan: **ENT_TaiSan**, **ENT_HoSoCongChung**
