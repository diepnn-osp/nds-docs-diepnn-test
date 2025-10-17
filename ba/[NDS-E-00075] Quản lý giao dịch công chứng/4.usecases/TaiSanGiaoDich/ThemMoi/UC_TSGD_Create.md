# Use Case: Thêm mới tài sản

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn thêm mới thông tin tài sản vào giao dịch công chứng đang lập hoặc chỉnh sửa, để đảm bảo dữ liệu tài sản được khai báo đầy đủ và hiển thị trên form trước khi lưu hồ sơ.

## Acceptance Criteria
- Hệ thống hiển thị popup thêm mới thông tin tài sản.  
- Khi người dùng lưu thành công, hệ thống hiển thị thông tin tài sản giao dịch trên màn hình thêm mới/chỉnh sửa giao dịch công chứng.  
- Nếu dữ liệu không hợp lệ, hiển thị thông báo lỗi cụ thể.  
- Người dùng có thể hủy thao tác thêm mới thông tin.

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Có quyền "Thêm mới/Chỉnh sửa giao dịch công chứng".
- Đang thao tác trong form giao dịch công chứng (**SCR_GDCC_Create** hoặc **SCR_GDCC_Update**).

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới tài sản** từ form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**).
2. Hệ thống hiển thị popup thêm mới tài sản (**SCR_TSGD_Create**).
3. Hệ thống tự động hiển thị danh sách loại tài sản phù hợp với **tên giao dịch công chứng** đã chọn trong hồ sơ.
4. Người dùng chọn loại tài sản.
5. Hệ thống hiển thị các trường thông tin tương ứng với loại tài sản đã chọn.
6. Người dùng nhập thông tin chi tiết tài sản.
7. Người dùng chọn thao tác **Lưu**:
8. Hệ thống kiểm tra tính hợp lệ của dữ liệu:
9. Nếu hợp lệ:
  - Ghi nhận dữ liệu vào danh sách tài sản của giao dịch.
  - Hiển thị thông báo "Thêm mới tài sản thành công".
  - Hiển thị lại danh sách tài sản trên form giao dịch công chứng.
10. Kết thúc use case.
   

## Luồng phụ 
- Người dùng chọn thao tác **Hủy**:
     - Hiển thị popup xác nhận hủy thao tác.
     - Nếu người dùng xác nhận: Đóng popup, quay lại form giao dịch công chứng (**SCR_GDCC_Create / SCR_GDCC_Update**) mà không ghi nhận dữ liệu.
     - Nếu người dùng không xác nhận: Đóng popup xác nhận, giữ nguyên popup thêm mới tài sản.
     - Kết thúc use case.

## Ngoại lệ
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".
- Nếu chưa điền đầy đủ thông tin bắt buộc: Hiển thị thông báo yêu cầu nhập thông tin bắt buộc. 

## Hậu điều kiện
- Nếu thành công: tài sản mới được thêm vào danh sách tài sản giao dịch trong giao dịch công chứng.
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu tài sản nào được thêm mới.

## Liên kết
- Activity Diagram: [AD_TSGD_Create.puml]
- Form liên quan: [SCR_TSGD_Create.md]
- Entity liên quan: **ENT_TaiSan**, **ENT_HoSoCongChung**