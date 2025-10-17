# Use Case: Xem chi tiết thông tin tài sản

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn có thể xem chi tiết thông tin tài sản đã thêm vào giao dịch công chứng, để đảm bảo dữ liệu đã nhập chính xác và đầy đù.

## Acceptance Criteria
- Hệ thống hiển thị popup chi tiết thông tin tài sản và đổ ra dữ liệu.  
- Hệ thống hiển thị chính xác thông tin theo từng loại tài sản

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập.  
- Người dùng có quyền "Thêm mới/Chỉnh sửa/Xem chi tiết giao dịch công chứng".  
- Người dùng đang thao tác trong form giao dịch công chứng (**SCR_GDCC_Create** / **SCR_GDCC_Update**) hoặc màn hình chi tiết giao dịch (**SCR_GDCC_Detail**).  

## Luồng chính
1. Người dùng chọn chức năng **Xem chi tiết** thông tin 1 tài sản trong danh sách tài sản của giao dịch.  
2. Hệ thống hiển thị popup chi tiết thông tin tài sản (**SCR_TSGD_Detail**).  
3. Người dùng xem thông tin chi tiết tài sản.  
4. Người dùng bấm **Đóng**.  
5. Hệ thống đóng popup chi tiết thông tin tài sản:
6. Kết thúc use case.  

## Luồng phụ / Ngoại lệ
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".  

## Hậu điều kiện
- Nếu thành công: Người dùng xem được chi tiết thông tin tài sản.  
- Nếu thất bại: Hiển thị thông báo lỗi.  

## Liên kết
- Activity Diagram: [AD_TSGD_Detail.puml]  
- Form liên quan: [SCR_GDCC_Detail.md], [SCR_GDCC_Update.md], [SCR_GDCC_Create.md], [SCR_TSGD_Detail.md]
- Entity liên quan: **ENT_TaiSan**, **ENT_HoSoCongChung**
