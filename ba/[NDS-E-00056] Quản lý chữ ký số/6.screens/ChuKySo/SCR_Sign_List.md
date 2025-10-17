# Màn hình: Danh sách chữ ký số
Nơi tập trung để xem và quản lý các chữ ký số.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền truy cập chức năng quản lý chữ ký số.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=329-21485&t=qwdm1CHMm4I6o7Ud-1]
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=343-38802&t=qwdm1CHMm4I6o7Ud-1]
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=343-33956&t=qwdm1CHMm4I6o7Ud-1]

## Thành phần

### Bảng chính

<div style="overflow-x:auto">

| Trường thông tin           | Control | Field                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                 |
|:---------------------------|:--------|:---------------------------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------------------------------|
| STT                        | text    | -                                | -          | -              | -                | -                  | Số thứ tự bản ghi                                                     |
| Sở Tư pháp                 | text    | tenDonVi                         | 500        | -              | -                | -                  | Chỉ hiển thị trong trường hợp người dùng cấp Bộ                       |
| Tên tổ chức công chứng     | text    | tenDonVi                         | 500        | -              | -                | -                  | Chỉ hiển thị trong trường hợp người dùng cấp Sở và cấp Bộ             |
| Địa chỉ tổ chức công chứng | text    | diaChi + phuongXa + tinhThanhPho | 500        | -              | -                | -                  | Chỉ hiển thị trong trường hợp người dùng cấp Sở và cấp Bộ             |
| Số serial                  | text    | soSerial                         | 100        | -              | -                | -                  | Số Serial                                                             |
| Nhà cung cấp dịch vụ       | text    | nhaCungCap                       | 200        | -              | -                | -                  | Nhà cung cấp chữ ký số                                                |
| Loại chữ ký số             | text    | loaiChuKySo                      | 50         | -              | -                | -                  | Cá nhân / Tổ chức                                                     |
| Tên công chứng viên        | text    | hodem + ten                      | 250        | -              | -                | -                  | Hiển thị tên công chứng viên đã chọn nếu là chữ ký số cá nhân         |
| Trạng thái                 | text    | trangThai                        | 50         | -              | -                | -                  | Mới tạo (Xanh) / Chờ duyệt (Vàng) / Đã duyệt (Xanh lá) / Từ chối (Đỏ) |
| Chức năng                  | icon    | -                                | -          | -              | -                | -                  | Xem chi tiết, Chỉnh sửa, Xóa , xem lịch sử (tuỳ quyền).               |

</div> 

### Chức năng

<div style="overflow-x:auto">

| Tên                       | Loại            | Mô tả                                                                                                                                                                      |
|:--------------------------|:----------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ô Tìm kiếm                | Input           | Hiển thị nếu có quyền tìm kiếm, placeholder: "Điền tên công chứng viên, hoặc số serial" (**UC_Sign_Search**)                                                               |
| Ô chọn Sở Tư pháp         | combobox search | Hiển thị nếu có quyền tìm kiếm, không hiển thị cho người dùng thuộc tổ chức công chứng. Chọn 1 từ danh sách Sở Tư pháp (**UC_Sign_Search**)                                |
| Ô chọn tổ chức công chứng | combobox search | Hiển thị nếu có quyền tìm kiếm, không hiển thị cho người dùng thuộc tổ chức công chứng, hiển thị theo Sở Tư pháp đã chọn (**UC_Sign_Search**). Chọn 1 từ danh sách tổ chức |
| Ô chọn nhà cung cấp       | combobox search | Hiển thị nếu có quyền tìm kiếm, Chọn 1 nhà cung cấp từ danh sách để tìm kiếm (**UC_Sign_Search**)                                                                          |
| Ô chọn loại chữ ký số     | combobox search | Hiển thị nếu có quyền tìm kiếm, Chọn 1 loại chữ ký số (cá nhân/tổ chức) để tìm kiếm (**UC_Sign_Search**)                                                                   |
| Ô chọn trạng thái         | combobox search | Hiển thị nếu có quyền tìm kiếm, Chọn 1 trạng thái (Chờ duyệt, tạo mới, đã duyệt, từ chối) để tìm kiếm (**UC_Sign_Search**)                                                 |
| Biểu tượng reset          | Button          | Bấm vào thực hiện reset kết quả tìm kiếm, hiển thị lại danh sách mặc định                                                                                                  |
| Tìm kiếm                  | Button          | Hiển thị nếu có quyền tìm kiếm, Click vào hệ thống sẽ thực hiện tìm kiếm theo tiêu chí đã nhập và chọn                                                                     |
| Xuất danh sách                    | Button          | Hiển thị nếu có quyền Xuất danh sách (**UC_Sign_Export**)                                                                                              |
| Nút đăng ký               | Button          | Hiển thị nếu có quyền thêm mới, click mở màn hình thêm mới đăng ký chữ ký số (**UC_Sign_Create**)                                                                          |
| Biểu tượng xem chi tiết   | Button          | Hiển thị nếu có quyền xem chi tiết, click mở màn hình chi tiết thông tin đăng ký chữ ký số (**UC_Sign_Detail**)                                                            |
| Biểu tượng sửa            | Button          | Hiển thị nếu có quyền chỉnh sửa, click mở màn hình chỉnh sửa đăng ký chữ ký số. Không hiển thị nếu trạng thái khác "Chờ duyệt" hoặc "Mới tạo" (**UC_Sign_Update**)         |
| Biểu tượng xóa            | Button          | Hiển thị nếu có quyền xóa, click mở popup xác nhận xoá. Không hiển thị nếu trạng thái khác "Chờ duyệt" hoặc "Mới tạo" (**UC_Sign_Delete**)                                 |
| Biểu tượng xem lịch sử    | Button          | Hiển thị nếu có quyền, click mở popup lịch sử thay đổi (**UC_Sign_History**)                                                                                               |

</div>