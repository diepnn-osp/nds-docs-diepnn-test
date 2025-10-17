# Use Case: Xuất danh sách chữ ký số

## User Story
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn xuất được danh sách chữ ký số của các tổ chức công chứng thuộc Sở Tư pháp của mình trên hệ thống theo kết quả tìm kiếm để có thể lấy được dữ liệu dưới dạng file excel
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xuất được danh sách chữ ký số của toàn bộ hệ thống theo kết quả tìm kiếm để có thể lấy được dữ liệu dưới dạng file excel
- Là **Công chứng viên/Nhân viên TCHNCC**, tôi muốn xuất được danh sách chữ ký số mà tổ chức đã đăng ký theo kết quả tìm kiếm để có thể lấy được dữ liệu dưới dạng file excel

## Acceptance criteria
- Xuất thành công danh sách gồm các trường thông tin

## Tác nhân chính
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xuất danh sách chữ ký số

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách chữ ký số.
2. Người dùng tìm kiếm danh sách chữ ký số cần xuất (UC_CCV_Export).
3. Người dùng bấm xuất danh sách.
4. Nếu người dùng có quyền, hệ thống xuất danh sách chữ ký số theo kết quả đã tìm kiếm. File excel danh sách bao gồm các cột bên dưới
    - Sở Tư pháp (Chỉ người dùng cấp Bộ)
    - Tên tổ chức công chứng (Chỉ người dùng cấp Bộ và Sở)
    - Địa chỉ tổ chức công chứng (Chỉ người dùng cấp Bộ và Sở)
    - Số Serial
    - Nhà cung cấp dịch vụ
    - Trạng thái
    - Loại chữ ký số: Cá nhân/Tổ chức
    - Tên công chứng viên
    - Ngày hiệu lực
    - Ngày hết hạn
5. Kết thúc.

## Luồng phụ / ngoại lệ
- Nếu có lỗi tải danh sách: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không quyền truy cập: hiển thị "Không có quyền truy cập" và ẩn đi nút "xuất danh sách".

## Hậu điều kiện
- Nếu thành công: Người dùng xuất được danh sách chữ ký số.
- Nếu thất bại: Thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_Sign_Export.puml]
- Form/Screen: [SCR_CCV_List.md]
- Entity liên quan: **ENT_CongChungVien**, **ENT_ToChucCongChung**
