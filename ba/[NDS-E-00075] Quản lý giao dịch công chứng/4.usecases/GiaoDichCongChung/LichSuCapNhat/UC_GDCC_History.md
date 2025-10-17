# Use Case: Xem lịch sử cập nhật thông tin giao dịch

## User Story
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn xem được lịch sử cập nhật thông tin của giao dịch do các tổ chức công chứng thuộc địa bàn đang lưu trữ. 
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem được lịch sử cập nhật thông tin của giao dịch trên toàn hệ thống
- Là **Công chứng viên**, tôi muốn xem được lịch sử cập nhật thông tin của giao dịch do tổ chức công chứng của tôi đang lưu trữ.

## Acceptance Criteria
- Hệ thống hiển thị lịch sử cập nhật dưới dạng danh sách bao gồm lịch sử thêm mới, chỉnh sửa, xóa.
- Nếu không tìm thấy dữ liệu, hệ thống hiển thị thông báo "Không tìm thấy lịch sử cập nhật thông tin giao dịch".
- Nếu có lỗi hệ thống, hiển thị thông báo lỗi.  
- Áp dụng cấu hình hiển thị, cho phép người dùng chỉ nhìn thấy được cập nhật của các trường thông tin đã được cấu hình cho phép tiếp cận
## Tác nhân chính
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP, Công chứng viên

## Tiền điều kiện
- Người dùng đăng nhập hệ thống.
- Người dùng có quyền xem lịch sử cập nhật thông tin giao dịch

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách thông tin giao dịch (**SCR_GDCC_List**)
2. Người dùng click vào biểu tượng xem lịch sử cập nhật.
3. Hệ thống truy vấn lịch sử cập nhật thông tin giao dịch (**ENT_LichSuCapNhat**).
4. Hệ thống áp dụng cấu hình để hiển thị thông tin.
5. Hệ thống hiển thị popup lịch sử cập nhật thông tin giao dịch (**SCR_GDCC_History**)
6. Người dùng bấm nút hoặc biểu tượng "Đóng" => Hệ thống đóng popup
7. Kết thúc Use case

## Luồng phụ 
- Người dùng truy cập thành công màn hình chi tiết giao dịch (**SCR_GDCC_Detail**) và click vào biểu tượng/nút xem lịch sử cập nhật

## Ngoại lệ
- Không có dữ liệu: Hiển thị "Không tìm thấy lịch sử cập nhật thông tin giao dịch".
- Lỗi hệ thống: Hiển thị thông báo "Không tải được thông tin, vui lòng thử lại".
- Không có quyền: Hệ thống không hiển thị chức năng xem lịch sử cập nhật thông tin giao dịch.

## Hậu điều kiện
- Nếu thành công: Người dùng xem được lịch sử cập nhật thông tin giao dịch.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_GDCC_History.puml]
- Form/Screen: [SCR_GDCC_History.md]
- Entity liên quan: **ENT_LichSuCapNhat**, **ENT_HoSoCongChung**, **ENT_TaiSan**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_TaiLieu**
