# Use Case: Tìm kiếm giao dịch công chứng

## User Story
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn tìm kiếm giao dịch công chứng trên địa bàn Sở Tư pháp của mình theo nhiều tiêu chí để có thể nhanh chóng tìm thấy thông tin cần thiết.  
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn tìm kiếm giao dịch công chứng trên toàn quốc theo nhiều tiêu chí để có thể nhanh chóng tìm thấy thông tin cần thiết. 
- Là **Công chứng viên**, tôi muốn tìm kiếm giao dịch công chứng trong danh sách mà tổ chức mình lưu trữ, để có thể nhanh chóng tìm thấy thông tin cần thiết

## Acceptance criteria
- Đối với người dùng là tổ chức công chứng, hệ thống hỗ trợ tìm kiếm toàn văn theo từ khóa chung trên toàn bộ nội dung giao dịch để trả về kết quả phù hợp nhất.
- Đối với người dùng là các tác nhân khác, hệ thống hỗ trợ tìm kiếm toàn văn theo từ khóa chung trên các trường thông tin được cấu hình cho phép tìm kiếm.
- Hệ thống cho phép người dùng tìm kiếm nâng cao theo "loại tài sản", "tên giao dịch", "tổ chức công chứng", "trạng thái"
- Hiển thị danh sách giao dịch công chứng theo tiêu chí đã tìm kiếm.
- Nếu có lỗi tải dữ liệu, hiển thị thông báo lỗi.
- Nếu không tìm thấy dữ liệu theo tiêu chí, thông báo "Không tìm thấy dữ liệu giao dịch"
 
## Tác nhân chính
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP, Công chứng viên

## Tiền điều kiện
- Người dùng đăng nhập hệ thống.
- Người dùng có quyền xem danh sách giao dịch công chứng

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách giao dịch công chứng (**SCR_GDCC_List**).
4. Người dùng điền thông tin tìm kiếm
5. Người dùng chọn tiêu chí tìm kiếm
6. Người dùng bấm nút "Tìm kiếm"
7. Đối với người dùng thuộc tổ chức công chứng: Hệ thống sẽ thực hiện tìm kiếm từ khóa trên toàn bộ nội dung của giao dịch công chứng, bao gồm tất cả các trường dữ liệu, văn bản và thông tin liên quan. Việc tìm kiếm vẫn tuân theo phạm vi dữ liệu mà người dùng được phép truy cập.
8. Đối với người dùng là tác nhân khác (không thuộc tổ chức công chứng): Hệ thống chỉ tìm kiếm từ khóa trong các trường thông tin đã được cấu hình cho phép tìm kiếm, tức là những trường dữ liệu được xác định rõ trong hệ thống. Việc tìm kiếm cũng giới hạn trong phạm vi dữ liệu mà người dùng được quyền tiếp cận. 
9. Hệ thống lọc danh sách kết quả tìm kiếm
    - Chính xác theo trạng thái giao dịch đã chọn
    - Chính xác theo loại tài sản giao dịch đã chọn
    - Chính xác theo tên giao dịch công chứng đã chọn
    - Chính xác theo tổ chức công chứng đã chọn
    - Chính xác theo Sở Tư pháp đã chọn
10. Hệ thống hiển thị danh sách giao dịch theo kết quả đã truy vấn được, sắp xếp theo quy tắc đã mô tả trong (**UC_GDCC_List**)
11. Kết thúc.

## Luồng phụ / ngoại lệ
- Nếu có lỗi tìm kiếm: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không tìm thấy dữ liệu: hiển thị "Không tìm thấy dữ liệu giao dịch".

## Hậu điều kiện
- Nếu thành công: Người dùng tìm kiếm thành công thông tin giao dịch.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_GDCC_Search.puml]
- Form/Screen: [SCR_GDCC_List.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_TaiSan**, **ENT_CaNhan**, **ENT_ToChuc**
