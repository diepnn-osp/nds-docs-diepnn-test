# Màn hình: Chi tiết công chứng viên

Hiển thị đầy đủ hồ sơ cá nhân, thông tin hành nghề của công chứng viên.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem chi tiết thông tin công chứng viên.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=135-16264&t=AJ0R7XTWgx3u3lfZ-1]

## Thành phần

### Thông tin chung (ENT_CongChungVien)

<div style="overflow-x:auto">

| Trường thông tin                | Control  | Field                              | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                    |
|:--------------------------------|:---------|:-----------------------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------------------------------|
| Ảnh công chứng viên             | image    | AnhDaiDien                         | -          | -              | -                | -                  | Ảnh công chứng viên (hiển thị ảnh mặc định nếu không có) |
| Họ và tên                       | text     | HoDem + Ten                        | -          | -              | -                | -                  | Họ tên công chứng viên                                   |
| Ngày sinh                       | date | NgaySinh                           | -          | -              | -                | -                  | Ngày sinh                                                |
| Giới tính                       | text     | GioiTinh                           | -          | -              | -                | -                  | Giới tính                                                |
| Số điện thoại                   | text     | DienThoaiDiDong                    | -          | -              | -                | -                  | Số điện thoại liên hệ                                    |
| Quốc tịch                       | text     | QuocTich                           | -          | -              | -                | -                  | Quốc tịch                                                |
| Dân tộc                         | text     | DanToc                             | -          | -              | -                | -                  | Dân tộc                                                  |
| Email                           | text     | Email                              | -          | -              | -                | -                  | Email                                                    |
| Số giấy tờ (CMND/CCCD/Hộ chiếu) | text     | SoGiayTo                           | -          | -              | -                | -                  | Thông tin giấy tờ định danh                              |
| Ngày cấp                        | date | NgayCap                            | -          | -              | -                | -                  | Ngày cấp giấy tờ định danh                               |
| Nơi cấp                         | text     | NoiCap                             | -          | -              | -                | -                  | Nơi cấp giấy tờ định danh                                |
| Địa chỉ thường trú              | text     | DiaChi + PhuongXa + TinhThanhPho | -          | -              | -                | -                  | Địa chỉ thường trú                                       |

</div>

### Thông tin tổ chức hành nghề (ENT_CongChungVien, ENT_ToChucCongChung)

<div style="overflow-x:auto">

| Trường thông tin           | Control | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                             |
|:---------------------------|:--------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------|
| Tên tổ chức công chứng     | text    | TenDonVi                                         | -          | -              | -                | -                  | Tổ chức công chứng đang hành nghề |
| Địa chỉ tổ chức công chứng | text    | DiaChiChiTiet + DiaChiPhuongXa + DiaChiTinhThanh | -          | -              | -                | -                  | Địa chỉ tổ chức công chứng        |
| Số thẻ công chứng viên     | text    | SoThe                                            | -          | -              | -                | -                  | Số hiệu thẻ hành nghề             |
| Trạng thái                 | text    | TrangThai                                        | -          | -              | -                | -                  | Trạng thái hoạt động              |

</div>

### Thông tin chứng chỉ hành nghề (ENT_ChungChiHanhNghe) *(nếu có quyền)*

<div style="overflow-x:auto">

| Trường thông tin | Control  | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:---------|:------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số chứng chỉ     | text     | SoChungChi  | -          | -              | -                | -                  | Hiển thị mã số chứng chỉ hành nghề             |
| Ngày cấp         | date | NgayCap     | -          | -              | -                | -                  | Hiển thị ngày cấp chứng chỉ                    |
| Nơi cấp          | text     | NoiCap      | -          | -              | -                | -                  | Hiển thị nơi cấp chứng chỉ                     |
| Ngày hiệu lực    | date | NgayHieuLuc | -          | -              | -                | -                  | Hiển thị ngày hiệu lực                         |
| Ngày hết hạn     | date | NgayHetHan  | -          | -              | -                | -                  | Hiển thị ngày hết hạn                          |
| Đơn vị cấp       | text     | DonViCap    | -          | -              | -                | -                  | Hiển thị cơ quan cấp chứng chỉ                 |
| Trạng thái       | text     | TrangThai   | -          | -              | -                | -                  | Hiển thị trạng thái chứng chỉ                  |
| File đính kèm    | file     | FileDinhKem | -          | -              | -                | -                  | Link file chứng chỉ, click vào mở preview file |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên                        | Loại   | Mô tả                                                                                  |
|:---------------------------|:-------|:---------------------------------------------------------------------------------------|
| Quay lại / Đóng            | Button | Trở về màn hình danh sách công chứng viên (**SCR_CCV_List**)                           |
| Chỉnh sửa                  | Button | Mở màn hình chỉnh sửa thông tin công chứng viên (**UC_CCV_Update**)                    |
| Lịch sử cập nhật chứng chỉ | Button | Hiển thị lịch sử cập nhật chứng chỉ (**UC_ChungChi_History**) (Hiển thị nếu có quyền)  |
| Lịch sử cập nhật           | Button | Hiển thị lịch sử cập nhật công chứng viên (**UC_CCV_History**) (Hiển thị nếu có quyền) |

</div>
