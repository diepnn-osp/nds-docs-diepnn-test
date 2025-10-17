# Màn hình: Tra cứu công chứng viên
Form cho phép người dùng nhập tiêu chí tra cứu và hiển thị danh sách công chứng viên phù hợp.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền tra cứu thông tin công chứng viên và chứng chỉ hành nghề.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=270-26074&t=VeTqJhXDfKkDczGX-1]

## Thành phần

### Form tra cứu

<div style="overflow-x:auto">

| Trường thông tin             | Control         | Field             | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                         |
|:-----------------------------|:----------------|:------------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------------------------------------------------------------------------------|
| Ô điền thông tin tra cứu     | text            | HoVaTen           | 250        | -              | -                | -                  | Hiển thị khi có quyền tra cứu công chứng viên, placeholder: "Điền tên công chứng viên, số thẻ CCV hoặc số chứng chỉ hành nghề" |
| Trạng thái                   | combobox search | TrangThai         | -          | -              | -                | -                  | Hiển thị khi có quyền tra cứu công chứng viên,Chọn 1 theo trạng thái hành nghề trong entity                                   |
| Sở Tư Pháp                   | combobox search | SoTuPhap          | -          | -              | -                | -                  | Hiển thị khi có quyền tra cứu công chứng viên, Chọn 1 từ danh sách Sở Tư pháp                                                 |
| Tổ chức hành nghề công chứng | combobox search | ToChucCongChungID | -          | -              | -                | -                  | Hiển thị khi có quyền tra cứu công chứng viên, Danh sách hiển thị theo Sở Tư pháp đã chọn, chọn 1 từ danh sách tổ chức        |

</div>

### Bảng kết quả

<div style="overflow-x:auto">

| Trường thông tin             | Control | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                         |
|:-----------------------------|:--------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------------------------------------|
| STT                          | text    | -                                                | -          | -              | -                | -                  | Số thứ tự bản ghi                                             |
| Sở Tư pháp                   | text    | TenDonVi                                         | -          | -              | -                | -                  | Hiển thị tên Sở Tư pháp                                       |
| Họ và tên                    | text    | HoDem + Ten                                      | 250        | -              | -                | -                  | Họ và tên công chứng viên                                     |
| Số thẻ CCV                   | text    | SoThe                                            | 50         | -              | -                | -                  | Số hiệu thẻ hành nghề công chứng viên                         |
| Số chứng chỉ hành nghề       | text    | SoChungChi                                       | 50         | -              | -                | -                  | Bấm vào hiển thị popup chi tiết chứng chỉ                     |
| Tổ chức công chứng hành nghề | text    | TenDonVi                                         | 500        | -              | -                | -                  | Tổ chức công chứng đang hành nghề                             |
| Địa chỉ trụ sở               | text    | DiaChiChiTiet + DiaChiPhuongXa + DiaChiTinhThanh | 500        | -              | -                | -                  | Hiển thị địa chỉ chi tiết của tổ chức + Phường xã, Tỉnh/Thành |
| Trạng thái hoạt động         | text    | TrangThai                                        | 50         | -              | -                | -                  | Trạng thái công chứng viên                                    |

</div>

### Popup chi tiết chứng chỉ hành nghề

<div style="overflow-x:auto">

| Trường thông tin | Control | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                       |
|:-----------------|:--------|:------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------|
| Số chứng chỉ     | text    | SoChungChi  | 50         | -              | -                | -                  | Mã số chứng chỉ hành nghề   |
| Ngày cấp         | date    | NgayCap     | -          | -              | -                | -                  | Ngày cấp chứng chỉ          |
| Ngày hiệu lực    | date    | NgayHieuLuc | -          | -              | -                | -                  | Ngày bắt đầu có hiệu lực    |
| Ngày hết hạn     | date    | NgayHetHan  | -          | -              | -                | -                  | Ngày chứng chỉ hết hiệu lực |
| Đơn vị cấp       | text    | TenDonVi    | 500        | -              | -                | -                  | Cơ quan cấp chứng chỉ       |
| Trạng thái       | text    | TrangThai   | 50         | -              | -                | -                  | Trạng thái chứng chỉ        |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên                         | Loại   | Mô tả                                                              |
|:----------------------------|:-------|:-------------------------------------------------------------------|
| Tra cứu                     | Button | Thực hiện tra cứu theo tiêu chí đã nhập                            |
| Phân trang                  | Button | Click vào hiển thị danh sách theo trang (10 bản ghi/trang)         |
| Đóng popup                  | Button | Đóng popup chi tiết chứng chỉ hành nghề, quay lại màn hình tra cứu |
| Reset                       | Button | Reset màn hình tra cứu                                             |
| Tab tra cứu công chứng viên | Tab    | Click vào hiển thị màn hình tra cứu công chứng viên                |

</div>
