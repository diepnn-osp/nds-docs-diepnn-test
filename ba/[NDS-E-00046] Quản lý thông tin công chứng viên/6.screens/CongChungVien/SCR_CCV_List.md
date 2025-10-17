# Màn hình: Danh sách công chứng viên
Nơi tập trung để xem và quản lý công chứng viên trên hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xem danh sách công chứng viên.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=135-15983&t=AJ0R7XTWgx3u3lfZ-1]

## Thành phần

### Bảng chính
- Các cột trong bảng danh sách công chứng viên hiển thị theo thứ tự bên dưới

<div style="overflow-x:auto">

| Trường thông tin     | Control | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                     |
|:---------------------|:--------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------------------------------------------------------------------|
| STT                  | text    | -                                                | -          | -              | -                | -                  | Số thứ tự bản ghi                                                                                         |
| Sở Tư pháp           | text    | TenDonVi                                         | 500        | -              | -                | -                  | Hiển thị tên Sở Tư pháp (Không hiển thị cột này với người dùng cấp Sở)                                    |
| Họ và tên            | text    | HoDem + Ten                                      | 250        | -              | -                | -                  | Họ và tên công chứng viên                                                                                 |
| Số thẻ               | text    | SoThe                                            | 50         | -              | -                | -                  | Số hiệu thẻ hành nghề công chứng                                                                          |
| Tổ chức công chứng   | text    | TenDonVi                                         | 500        | -              | -                | -                  | Tên tổ chức công chứng đang hành nghề                                                                     |
| Địa chỉ tổ chức      | text    | DiaChiChiTiet + DiaChiTinhThanh + DiaChiPhuongXa | 500        | -              | -                | -                  | Địa chỉ tổ chức công chứng                                                                                |
| Trạng thái hoạt động | text    | TrangThai                                        | 50         | -              | -                | -                  | "Đang hành nghề" hiển thị trạng thái màu xanh lá. "Đã miễn nhiệm"/"Tạm đình chỉ" màu đỏ. Còn lại màu vàng |
| Chức năng            | icon    | -                                                | -          | -              | -                | -                  | Xem chi tiết, Sửa, Xóa, Xem lịch sử (tùy quyền)                                                           |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên                         | Loại            | Mô tả                                                                                                                              |
|:----------------------------|:----------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| Ô tìm kiếm                  | Input           | Nhập tên công chứng viên hoặc số thẻ để tìm kiếm                                                                                   |
| Ô chọn trạng thái           | combobox search | Chọn 1 trạng thái từ danh sách trạng thái hoạt động của công chứng viên (Giống với SCR_CCV_Create) để tìm kiếm (**UC_CCV_Search**) |
| Ô chọn Sở Tư pháp           | combobox search | Không hiển thị với người dùng cấp Sở. Chọn 1 Sở Tư pháp từ danh sách Sở Tư pháp để tìm kiếm (**UC_CCV_Search**)                    |
| Ô chọn Tổ chức công chứng   | combobox search | Chọn 1 tổ chức công chứng theo Sở Tư Pháp đã chọn/hiện tại (**UC_CCV_Search**)                                                     |
| Biểu tượng tìm kiếm         | Button          | Bấm vào thực hiện tìm kiếm theo thông tin đã nhập/chọn (UC_CCV_Search)                                                             |
| Biểu tượng reset            | Button          | Bấm vào thực hiện reset kết quả tìm kiếm, hiển thị lại danh sách mặc định                                                          |
| Nút xuất danh sách          | Button          | Hiển thị nếu có quyền, click sẽ xuất danh sách theo điều kiện đã tìm (UC_CCV_Export)                                               |
| Nút thêm mới                | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình thêm công chứng viên (UC_CCV_Create)                                                   |
| Biểu tượng xem chi tiết     | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình xem chi tiết công chứng viên (UC_CCV_Detail)                                           |
| Biểu tượng sửa              | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình chỉnh sửa công chứng viên (UC_CCV_Update)                                              |
| Biểu tượng xóa              | Button          | Hiển thị nếu có quyền, click sẽ mở popup xác nhận xóa công chứng viên (UC_CCV_Delete)                                              |
| Biểu tượng lịch sử cập nhật | Button          | Hiển thị nếu có quyền, click sẽ mở popup xem lịch sử cập nhật thông tin công chứng viên (UC_CCV_History)                           |

</div>
