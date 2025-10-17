# Use Case: Xem danh sách giao dịch công chứng

## User Story
- Với vai trò là **Công chứng viên**, tôi muốn xem danh sách các giao dịch công chứng do tổ chức mình quản lý để có thể theo dõi, tìm kiếm và thực hiện các thao tác nghiệp vụ khác.
- Với vai trò là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn xem danh sách các giao dịch công chứng được lưu trữ bởi các tổ chức công chứng thuộc Sở Tư pháp của mình để theo dõi, tra cứu và thực hiện các thao tác nghiệp vụ tiếp theo.
- Với vai trò là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem danh sách các giao dịch công chứng trên toàn hệ thống để theo dõi, tra cứu và thực hiện các thao tác nghiệp vụ tiếp theo.

## Acceptance Criteria
- Hệ thống kiểm tra vai trò người dùng:
  - Nếu là **Cấp Bộ**: hiển thị toàn bộ giao dịch công chứng trên toàn quốc, ngoại trừ các giao dịch đang ở trạng thái "Lưu nháp".
  - Nếu là **Cấp thuộc Bộ**: hiển thị các giao dịch của các tổ chức công chứng thuộc địa bàn/Sở Tư pháp của người dùng đang lưu trữ, ngoại trừ các giao dịch đang ở trạng thái "Lưu nháp".
  - Nếu là **Cấp thuộc Sở**: hiển thị các giao dịch do tổ chức đó lưu trữ, bao gồm cả giao dịch "Lưu nháp" và "Lưu chính thức".
- Hệ thống hiển thị danh sách giao dịch công chứng kèm các thông tin cơ bản: mã giao dịch, tên giao dịch, trạng thái, ngày tạo, tổ chức công chứng, bên liên quan.
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống cung cấp phân trang.

## Tác nhân chính
- Công chứng viên
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP
- Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Có quyền truy cập chức năng "Xem danh sách giao dịch công chứng".

## Luồng chính
1. Người dùng lựa chọn chức năng "Quản lý giao dịch công chứng" 
2. Hệ thống hiển thị 2 lựa chọn "Giao dịch công chứng giấy" và "Giao dịch công chứng điện tử"
3. Người dùng lựa chọn "Giao dịch công chứng giấy" hoặc "Giao dịch công chứng điện tử"
4. Hệ thống thực hiện truy vấn danh sách giao dịch theo loại giao dịch đã chọn
5. Hệ thống kiểm tra vai trò người dùng:
   - Nếu là **Cấp Bộ**:
     - Truy vấn toàn bộ giao dịch công chứng trên toàn quốc.
     - Loại bỏ các giao dịch đang ở trạng thái "Lưu nháp".
     - Danh sách giao dịch công chứng sắp xếp theo thứ tự:
        - Ngày công chứng, hiển thị từ giao dịch mới nhất đến giao dịch cũ nhất
        - Nếu giao dịch cùng ngày công chứng, hiển thị giao dịch theo số công chứng từ lớn nhất tới nhỏ nhất
        - Nếu cùng số công chứng, sắp xếp theo thời gian tạo mới nhất => cũ nhất
   - Nếu là **Cấp thuộc Bộ**:
     - Xác định địa bàn/Sở Tư pháp của người dùng.
     - Truy vấn các giao dịch đang được lưu trữ bởi các tổ chức công chứng thuộc địa bàn đó.
     - Loại bỏ các giao dịch đang ở trạng thái "Lưu nháp".
     - Danh sách giao dịch công chứng sắp xếp theo thứ tự:
        - Ngày công chứng, hiển thị từ giao dịch mới nhất đến giao dịch cũ nhất
        - Nếu giao dịch cùng ngày công chứng, hiển thị giao dịch theo số công chứng từ lớn nhất tới nhỏ nhất
        - Nếu cùng số công chứng, sắp xếp theo thời gian tạo mới nhất => cũ nhất
   - Nếu là **Tổ chức công chứng**:
     - Truy vấn các giao dịch do tổ chức đó lưu trữ.
     - Bao gồm cả giao dịch "Lưu nháp" và "Lưu chính thức", danh sách hiển thị tùy theo tab mà người dùng chọn
     - Sắp xếp danh sách giao dịch theo số công chứng từ lớn nhất tới nhỏ nhất
6. Hệ thống kiểm tra cấu hình hiển thị thông tin
7. Hệ thống áp dụng cấu hình để hiển thị các cột thông tin tương ứng;
8. Hệ thống hiển thị danh sách giao dịch công chứng (mặc định 10 bản ghi/trang) (**SCR_GDCC_List**) 
9. Kết thúc

## Luồng phụ
- Nếu là người dùng thuộc tổ chức công chứng, hệ thống chia danh sách giao dịch vào 2 tab "Lưu nháp" và "Lưu chính thức" (Quy tắc sắp xếp không đổi). Người dùng click vào các tab "Lưu nháp", "Lưu chính thức", hệ thống hiện thị danh sách giao dịch theo trạng thái tương ứng
- Người dùng chuyển trang khác, hệ thống hiển thị số lượng bản ghi tương ứng với trang đã chọn

## Ngoại lệ
- Không có giao dịch: hiển thị "Không có dữ liệu".
- Nếu người dùng không có quyền truy cập, hệ thống không hiển thị chức năng.
- Nếu không xác định được vai trò: hiển thị thông báo lỗi "Không xác định được vai trò người dùng" và kết thúc use case.

## Hậu điều kiện
- Thành công: Người dùng xem được danh sách giao dịch công chứng phù hợp với quyền truy cập.
- Thất bại: Hệ thống hiển thị thông báo lỗi

## Liên kết
- Activity Diagram: [AD_GDCC_List.puml]
- Form liên quan: [SCR_GDCC_List.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_TaiSan**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_YeuCauChuyenQuyenSoHuuHoSo**