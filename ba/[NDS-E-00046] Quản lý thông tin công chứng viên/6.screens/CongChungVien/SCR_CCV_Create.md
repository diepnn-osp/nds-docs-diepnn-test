# Màn hình: Thêm mới công chứng viên
Form cho phép nhập và lưu thông tin công chứng viên mới vào hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền thêm mới công chứng viên.
 
## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=135-16133&t=AJ0R7XTWgx3u3lfZ-1]

## Thành phần

### Thông tin cá nhân

<div style="overflow-x:auto">

| Trường thông tin                | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                           |
|:--------------------------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------------------------------------------------------|
| Ảnh                             | image           | AnhDaiDien      | -          | N              | -                | -                  | Sau khi Upload thành công sẽ hiển thị ảnh vừa tải lên, click vào có thể preview |
| Họ và tên                       | text            | HoDem + Ten     | 250        | Y              | -                | -                  | Điền họ và tên công chứng viên                                                  |
| Ngày sinh                       | date            | NgaySinh        | -          | Y              | -                | -                  | **BR9.3**                                                                       |
| Giới tính                       | dropdown        | GioiTinh        | -          | Y              | -                | -                  | Chọn 1 Nam/Nữ                                                                   |
| Quốc tịch                       | combobox search | QuocTich        | -          | Y              | Việt Nam         | Y                  | Chọn 1 từ danh mục quốc tịch                                                    |
| Dân tộc                         | combobox search | DanToc          | -          | N              | -                | -                  | Chọn 1 từ danh mục dân tộc                                                      |
| Số điện thoại                   | text            | DienThoaiDiDong | 20         | N              | -                | -                  | **BR9.4**                                                                       |
| Email                           | text            | Email           | 250        | N              | -                | -                  |                                                                                 |
| Số giấy tờ (CMND/CCCD/Hộ chiếu) | text            | SoGiayTo        | 20         | Y              | -                | -                  | **BR9.10**                                                                      |
| Ngày cấp                        | date            | NgayCap         | -          | Y              | -                | -                  | **BR9.3**                                                                       |
| Nơi cấp                         | text            | NoiCap          | 500        | Y              | -                | -                  |                                                                                 |
| Địa chỉ thường trú              | text            | DiaChi          | 500        | Y              | -                | -                  | Placeholder: Nhập địa chỉ số nhà, tổ, thôn, xóm                                 |
| Tỉnh/Thành phố thường trú       | combobox search | TinhThanhPho    | -          | Y              | -                | -                  | Chọn 1 từ danh mục tỉnh thành phố mới. **BR9.7**                                |
| Phường/Xã thường trú            | combobox search | PhuongXa        | -          | Y              | -                | -                  | Chọn 1 từ danh mục phường xã mới. **BR9.8**                                     |
| Trạng thái                      | combobox search | TrangThai       | -          | Y              | Đang hành nghề   | Y                  | Chọn 1 từ danh sách lấy trong entity                                            |

</div>

### Thông tin tổ chức hành nghề

<div style="overflow-x:auto">

| Trường thông tin           | Control         | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                |
|:---------------------------|:----------------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------------------------------------------|
| Tên tổ chức công chứng     | combobox search | DonViId                                          | -          | Y              | -                | -                  | Chọn từ danh sách tổ chức công chứng thuộc Sở Tư pháp của người dùng |
| Địa chỉ tổ chức công chứng | text            | DiaChiChiTiet + DiaChiTinhThanh + DiaChiPhuongXa | 500        | N              | -                | N                  | Tự động điền từ tổ chức chọn, disable                                |
| Số thẻ công chứng viên     | text            | SoThe                                            | 50         | Y              | -                | -                  | Số hiệu thẻ hành nghề                                                |
| Trưởng văn phòng           | checkbox        | LaTruongVanPhong                                 | -          | N              | False            | Y                  |                                                                      |

</div>

### Thông tin chứng chỉ hành nghề

<div style="overflow-x:auto">

| Trường thông tin | Control         | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                    |
|:-----------------|:----------------|:------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------|
| Số chứng chỉ     | text            | SoChungChi  | 50         | N              | -                | -                  |                                          |
| Ngày cấp         | date            | NgayCap     | -          | N              | -                | -                  |                                          |
| Ngày hiệu lực    | date            | NgayHieuLuc | -          | N              | -                | -                  |                                          |
| Ngày hết hạn     | date            | NgayHetHan  | -          | N              | -                | -                  | Ngày hết hạn lớn hoặc bằng ngày hiệu lực |
| Đơn vị cấp       | text            | DonViCap    | 100        | N              | -                | -                  |                                          |
| Trạng thái       | Combobox search | TrangThai   | -          | N              | -                | -                  | Chọn 1 trong các trạng thái trong entity |
| File đính kèm    | file            | FileDinhKem | -          | N              | -                | -                  | Link file vừa tải lên, bấm để mở file    |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                  |
|:-------------|:-------|:-----------------------------------------------------------------------|
| Lưu          | Button | Kiểm tra hợp lệ, lưu dữ liệu vào ENT_CongChungVien (**UC_CCV_Create**) |
| Hủy          | Button | Hiển thị popup xác nhận hủy thao tác                                   |
| Tải lên      | Button | Upload ảnh công chứng viên, chỉ chấp nhận định dạng ảnh dưới 10MB.     |
| Tải lên file | Button | Tải lên file pdf, docs, docx, tối đa 10MB                              |
| Xóa ảnh      | Button | Xóa ảnh công chứng viên vừa tải lên                                    |
| Xóa file     | Button | Xóa file chứng chỉ vừa tải lên                                         |

</div>
