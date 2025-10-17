# Use Case: Xem chi tiết giao dịch công chứng

## User Story
- Là **Công chứng viên**, tôi muốn xem được chi tiết giao dịch công chứng do tổ chức mình lưu trữ, để có thể rà soát thông tin giao dịch.
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn xem được chi tiết thông tin giao dịch được lưu trữ bởi các tổ chức công chứng trên địa bàn của mình, để có thể nắm rõ thông tin hồ sơ và thực hiện các nghiệp vụ cần thiết.
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem được chi tiết thông tin các giao dịch trên toàn quốc, để có thể nắm rõ thông tin hồ sơ và thực hiện các nghiệp vụ cần thiết.

## Acceptance criteria
- Với công chứng viên, hệ thống hiển thị đầy đủ thông tin chi tiết của giao dịch công chứng được chọn từ danh sách.
- Với những tác nhân khác, hệ thống hiển thị thông tin giao dịch công chứng theo cấu hình.
- Người dùng có thể quay lại danh sách giao dịch công chứng.
- Nếu không tìm thấy dữ liệu, hệ thống hiển thị thông báo "Không tìm thấy thông tin giao dịch công chứng".
- Nếu có lỗi hệ thống, hiển thị thông báo lỗi.  

## Tác nhân chính
- Công chứng viên
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đăng nhập hệ thống.
- Người dùng có quyền xem chi tiết giao dịch công chứng

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách giao dịch công chứng điện tử/giấy (**SCR_GDCC_List**)
2. Hệ thống kiểm tra quyền truy cập của người dùng
3. Nếu có quyền, người dùng chọn xem chi tiết 1 giao dịch công chứng
4. Hệ thống truy vấn dữ liệu giao dịch công chứng từ cơ sở dữ liệu (**ENT_HoSoCongChung**)
5. Hệ thống kiểm tra cấu hình hiển thị chi tiết giao dịch công chứng
6. Hệ thống hiển thị màn hình chi tiết giao dịch công chứng (**SCR_GDCC_Detail**)
7. Hệ thống hiển thị các trường thông tin chi tiết giao dịch công chứng theo cấu hình
8. Kết thúc use case

## Luồng phụ 
- Người dùng chọn "Đóng" màn hình chi tiết hoặc chọn quay lại, hệ thống quay trở lại màn hình danh sách giao dịch công chứng (**SCR_GDCC_List**)

## Ngoại lệ
- Không có dữ liệu: Hiển thị "Không tìm thấy thông tin giao dịch công chứng".
- Lỗi hệ thống: Hiển thị thông báo "Không tải được thông tin, vui lòng thử lại".
- Không có quyền truy cập: Hệ thống không hiển thị chức năng xem chi tiết giao dịch công chứng

## Hậu điều kiện
- Nếu thành công: Người dùng xem được thông tin chi tiết giao dịch công chứng.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_GDCC_Detail.puml]
- Form/Screen: [SCR_GDCC_Detail.md], [SCR_NTGGD_List.md], [SCR_TSGD_List.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_TaiSan**, **ENT_CaNhan**, **ENT_ToChuc**.
