# Use Case: Tìm kiếm chữ ký số

## User Story
- Là **Công chứng viên / Nhân viên TCHNCC**, tôi muốn tìm kiếm theo nhiều tiêu chí, để có thể nhanh chóng tìm thấy chữ ký số trong danh sách đã đăng ký của tổ chức mình
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn tìm kiếm theo nhiều tiêu chí, để có thể nhanh chóng tìm thấy thông tin chữ ký số trong danh sách đã đăng ký của các tổ chức công chứng thuộc Sở Tư pháp
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn tìm kiếm theo nhiều tiêu chí, để có thể tìm thấy thông tin chữ ký số trong danh sách đăng ký trên cả hệ thống

## Acceptance criteria
- Hệ thống hiển thị form tìm kiếm với các tiêu chí
    - Ô điền thông tin tìm kiếm theo "Họ và tên công chứng viên", "Số serial"
    - Chọn trạng thái
    - Chọn nhà cung cấp dịch vụ
    - Chọn loại chữ ký số
    - Chọn Sở Tư pháp
    - Chọn tổ chức công chứng
- Hiển thị bảng danh sách Thông tin đăng ký chữ ký số với các cột tông tin cơ bản (Tên tổ chức công chứng, Số serial, Nhà cung cấp dịch vụ, Trạng thái, Loại chữ ký số, tên công chứng viên) theo tiêu chí đã tìm kiếm.
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống phải cung cấp phân trang (10 bản ghi 1 trang).
- Nếu có lỗi tải dữ liệu, hiển thị thông báo lỗi.
- Nếu không tìm thấy dữ liệu theo tiêu chí tìm kiếm, thông báo "Không tìm thấy dữ liệu Thông tin chữ ký số"
- Danh sách Thông tin chữ ký số hiển thị theo thứ tự thời gian cập nhật từ mới tới cũ nhất.

## Tác nhân chính
- Công chứng viên / Nhân viên TCHNCC, Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đăng nhập hệ thống.
- Người dùng có quyền tìm kiếm thông tin Thông tin chữ ký số

## Luồng chính
1. Người dùng truy cập màn hình danh sách Thông tin đăng ký chữ ký số (**UC_Sign_List**).
2. Người dùng điền thông tin tìm kiếm (theo "Họ và tên công chứng viên", "Số serial")
3. Người dùng chọn tiêu chí tìm kiếm khác
4. Người dùng bấm nút "Tìm kiếm"
5. Hệ thống truy vấn thông tin Thông tin đăng ký chữ ký số
    - Truy vấn họ và tên công chứng viên gần giống với kết quả đã điền
    - Truy vấn chính xác số serial đã điền
    - Truy vấn chính xác theo trạng thái đăng ký đã chọn
    - Truy vấn chính xác theo nhà cung cấp dịch vụ đã chọn
    - Truy vấn chính xác theo tổ chức công chứng đã chọn
    - Truy vấn chính xác theo Sở Tư pháp đã chọn
    - Truy vấn chính xác loại chữ ký số đã chọn
6. Hệ thống hiển thị danh sách thông tin đăng ký chữ ký số theo kết quả đã truy vấn được
7. Hệ thống hiển thị danh sách Thông tin đăng ký chữ ký số theo thứ tự thời gian cập nhật từ mới tới cũ nhất
8. Nếu số lượng bản ghi lớn hơn 10, hệ thống thực hiện phân trang, 10 bản ghi mỗi trang
9. Kết thúc.

## Luồng phụ / ngoại lệ
- Nếu có lỗi tìm kiếm: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không tìm thấy dữ liệu: hiển thị "Không có dữ liệu chữ ký số".

## Hậu điều kiện
- Nếu thành công: Người dùng tìm kiếm thành công thông tin chữ ký số.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_Sign_Search.puml]
- Form/Screen: [SCR_Sign_Search.md]
- Entity liên quan: ENT_CongChungVien, ENT_ToChucCongChung, ENT_ChuKySo
