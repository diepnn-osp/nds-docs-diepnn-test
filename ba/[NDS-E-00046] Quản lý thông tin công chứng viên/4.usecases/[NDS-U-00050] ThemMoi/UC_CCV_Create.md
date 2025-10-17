# Use Case: UC_CCV_Create (Thêm mới công chứng viên)

## User Story
- Với vai trò là **Chuyên viên STP**, tôi muốn có thể thêm mới công chứng viên vào hệ thống, để đảm bảo dữ liệu công chứng viên luôn đầy đủ.

## Acceptance Criteria
- Hệ thống hiển thị form thêm mới công chứng viên.
- Hệ thống kiểm tra dữ liệu hợp lệ trước khi lưu thông tin công chứng viên.
- Nếu dữ liệu hợp lệ, hệ thống lưu công chứng viên mới vào danh sách và hiển thị thông báo thành công.
- Nếu dữ liệu không hợp lệ, hiển thị thông báo lỗi.
- Người dùng có thể hủy thao tác thêm mới.

## Tác nhân chính
- Chuyên viên STP

## Tiền điều kiện
- Người dùng đã đăng nhập.
- Người dùng có quyền "Thêm mới công chứng viên".

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới công chứng viên** từ danh sách (**UC_CCV_List**).
2. Hệ thống hiển thị form thêm mới (**SCR_CCV_Create**).
3. Người dùng nhập các thông tin cần thiết.
4. Người dùng bấm nút **Lưu**.
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu:
   - Nếu hợp lệ: Lưu dữ liệu vào  **ENT_CongChungVien**.
   - Thông báo "Thêm mới công chứng viên thành công".
   - Mở màn hình chi tiết công chứng viên vừa tạo (**UC_CCV_Detail**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- Người dùng chọn **Hủy**: Hiển thị popup xác nhận hủy thao tác. Nếu xác nhận, form đóng, không lưu dữ liệu, chuyển về màn danh sách. Nếu hủy xác nhận, đóng popup xác nhận
- Lỗi hệ thống: Hiển thị thông báo lỗi "Hệ thống phát sinh lỗi, vui lòng thử lại", không lưu dữ liệu.
- Nếu Ngày Sinh/Ngày cấp giấy tờ > Ngày hôm nay: thông báo lỗi "Thông tin không hợp lệ"
- Nếu chưa điền thông tin bắt buộc, hiển thị thông báo yêu cầu điền thông tin bắt buộc
- Nếu sai định dạng thông tin, hiển thị thông báo lỗi "Thông tin không hợp lệ"
- Nếu số thẻ bị trùng với công chứng viên khác trong hệ thống, hệ thống thông báo lỗi "Số thẻ đã tồn tại". 
- Nếu số giấy tờ cá nhân bị trùng với công chứng viên khác trong hệ thống, hệ thống thông báo lỗi "Số CCCD/CMND/Hộ chiếu đã tồn tại". 

## Hậu điều kiện
- Nếu thành công: Công chứng viên được thêm vào hệ thống.
- Nếu thất bại: Không có dữ liệu mới nào được thêm, hiển thị "Thêm mới công chứng viên thất bại, vui lòng thử lại.

## Liên kết
- Activity Diagram: [AD_CCV_Create.puml]
- Form liên quan: [SCR_CCV_Create.md]
- Entity liên quan: **ENT_CongChungVien**, **ENT_ToChucCongChung**
