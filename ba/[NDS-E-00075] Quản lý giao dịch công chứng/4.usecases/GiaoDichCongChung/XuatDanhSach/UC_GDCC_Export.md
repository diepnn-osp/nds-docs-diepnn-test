# Use Case: Xuất danh sách giao dịch công chứng

## User Story
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP** tôi muốn xuất được danh sách giao dịch công chứng thuộc Sở Tư pháp của mình để có thể lấy được dữ liệu dưới dạng file excel
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xuất được danh sách giao dịch công chứng trên toàn quốc để có thể lấy được dữ liệu dưới dạng file excel
- Là **Công chứng viên**, tôi muốn xuất được danh sách giao dịch công chứng do tổ chức mình lưu trữ có thể lấy được dữ liệu dưới dạng file excel

## Acceptance Criteria
- Xuất thành công danh sách giao dịch công chứng dưới dạng file excel

## Tác nhân chính
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP, Công chứng viên

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xuất danh sách giao dịch công chứng

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách giao dịch công chứng (**SCR_GDCC_List**).
2. Người dùng tìm kiếm danh sách giao dịch công chứng cần xuất (**UC_GDCC_Search**).
3. Người dùng bấm xuất danh sách.
4. Nếu người dùng có quyền, hệ thống xuất danh sách giao dịch công chứng theo kết quả đã tìm kiếm. File excel tuân theo quy tắc bên dưới, nếu trường thông tin được cấu hình không cho phép người dùng tiếp cận, hệ thống bỏ qua:
    - SỐ CÔNG CHỨNG: SoCongChung	
    - NGÀY, THÁNG, NĂM CÔNG CHỨNG: NgayCongChung	
    - THÔNG TIN VỀ NGƯỜI YÊU CẦU CÔNG CHỨNG: Thông tin tất cả các người tham gia giao dịch theo template dưới, thông tin cách nhau bởi dấu ";"
        - Cá nhân: Hodem + Ten, SoGiayTo
        - Tổ chức: TenToChuc, SoGiayToPhapNhan
    - LOẠI GIAO DỊCH: TenGiaoDichId	
    - HỌ TÊN CÔNG CHỨNG VIÊN KÝ VĂN BẢN CÔNG CHỨNG: CongChungVienId	
    - PHÍ CÔNG CHỨNG: PhiCongChung	
    - GIÁ DỊCH VỤ THEO YÊU CẦU LIÊN QUAN ĐẾN VIỆC CÔNG CHỨNG;CHI PHÍ KHÁC: ThuLaoCongChung	
    - TÀI SẢN LÀ ĐỐI TƯỢNG HOẶC LIÊN QUAN ĐẾN GIAO DỊCH: Xuất theo template "Loại tài sản: LoaiTaiSan, chủ sở hữu: ChuSoHuu, Số giấy chứng nhận: SoGiayChungNhan, Ngày cấp: NgayCap, NoiCap.", mỗi tài sản cách nhau bởi dấu ";"
    - GHI CHÚ: GhiChu
5. Kết thúc.

## Luồng phụ / ngoại lệ
- Nếu có lỗi tải danh sách: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không quyền truy cập: Không hiển thị chức năng xuất danh sách.
- Nếu xuất thất bại: hiển thị "Xuất danh sách thất bại, vui lòng thử lại".

## Hậu điều kiện
- Nếu thành công: Người dùng xuất được danh sách giao dịch công chứng.
- Nếu thất bại: Thông báo lỗi "Xuất danh sách thất bại, vui lòng thử lại".

## Liên kết
- Activity Diagram: [AD_GDCC_Export.puml]
- Form/Screen: [SCR_GDCC_List.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_TaiSan**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_YeuCauChuyenQuyenSoHuuHoSo**
