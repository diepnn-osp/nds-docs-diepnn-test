# Màn hình: Chỉnh sửa công chứng viên
Form cho phép chỉnh sửa thông tin công chứng viên, hiển thị dữ liệu đã có và cho phép cập nhật.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền chỉnh sửa công chứng viên.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=135-16198&t=AJ0R7XTWgx3u3lfZ-1]

## Thành phần

### Thông tin cá nhân
- Thông tin được tự động điền từ dữ liệu đã lưu
<div style="overflow-x:auto">

| Trường thông tin                | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                           |
|:--------------------------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------------------------------------------------------|
| Ảnh                             | image           | AnhDaiDien      | -          | N              | -                | Y                  | Sau khi Upload thành công sẽ hiển thị ảnh vừa tải lên, click vào có thể preview |
| Họ và tên                       | text            | HoDem + Ten     | 250        | Y              | -                | Y                  | Điền họ và tên công chứng viên                                                  |
| Ngày sinh                       | date            | NgaySinh        | -          | Y              | -                | Y                  | **BR9.3**                                                                       |
| Giới tính                       | dropdown        | GioiTinh        | -          | Y              | -                | Y                  | Chọn 1 Nam/Nữ                                                                   |
| Quốc tịch                       | combobox search | QuocTich        | -          | Y              | Việt Nam         | Y                  | Chọn 1 từ danh mục quốc tịch                                                    |
| Dân tộc                         | combobox search | DanToc          | -          | N              | -                | Y                  | Chọn 1 từ danh mục dân tộc                                                      |
| Số điện thoại                   | text            | DienThoaiDiDong | 20         | N              | -                | Y                  | **BR9.4**                                                                       |
| Email                           | text            | Email           | 250        | N              | -                | Y                  |                                                                                 |
| Số giấy tờ (CMND/CCCD/Hộ chiếu) | text            | SoGiayTo        | 20         | Y              | -                | N                  | **BR9.10**                                                                      |
| Ngày cấp                        | date            | NgayCap         | -          | Y              | -                | N                  | **BR9.3**                                                                       |
| Nơi cấp                         | text            | NoiCap          | 500        | Y              | -                | Y                  |                                                                                 |
| Địa chỉ thường trú (mới)        | text            | DiaChi          | 500        | Y              | -                | Y                  | Placeholder: Nhập địa chỉ số nhà, tổ, thôn, xóm                                 |
| Tỉnh/Thành phố thường trú (mới) | combobox search | TinhThanhPho    | -          | Y              | -                | Y                  | Chọn 1 từ danh mục tỉnh thành phố mới. **BR9.7**                                |
| Phường/Xã thường trú (mới)      | combobox search | PhuongXa        | -          | Y              | -                | Y                  | Chọn 1 từ danh mục phường xã mới. **BR9.8**                                     |
| Trạng thái                      | combobox search | TrangThai       | -          | Y              | Đang hành nghề   | Y                  | Chọn 1 từ danh sách lấy trong entity                                            |

</div>

### Thông tin tổ chức hành nghề
- Thông tin được tự động điền từ dữ liệu đã lưu
<div style="overflow-x:auto">

| Trường thông tin           | Control         | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                |
|:---------------------------|:----------------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------------------------------------------|
| Tên tổ chức công chứng     | combobox search | DonViId                                          | 250        | Y              | -                | Y                  | Chọn từ danh sách tổ chức công chứng thuộc Sở Tư pháp của người dùng |
| Địa chỉ tổ chức công chứng | text            | DiaChiChiTiet + DiaChiTinhThanh + DiaChiPhuongXa | 500        | N              | -                | N                  | Tự động điền từ tổ chức chọn, disable                                |
| Số thẻ công chứng viên     | text            | SoThe                                            | 50         | Y              | -                | N                  | Số hiệu thẻ hành nghề                                                |

</div>

### Thông tin chứng chỉ hành nghề
- Thông tin được tự động điền từ dữ liệu đã lưu

<div style="overflow-x:auto">

| Trường thông tin | Control         | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                    |
|:-----------------|:----------------|:------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------|
| Số chứng chỉ     | text            | SoChungChi  | 50         | N              | -                | Y                  |                                          |
| Ngày cấp         | date            | NgayCap     | -          | N              | -                | Y                  |                                          |
| Ngày hiệu lực    | date            | NgayHieuLuc | -          | N              | -                | Y                  |                                          |
| Ngày hết hạn     | date            | NgayHetHan  | -          | N              | -                | Y                  | Ngày hết hạn lớn hoặc bằng ngày hiệu lực |
| Đơn vị cấp       | text            | DonViCap    | 100        | N              | -                | Y                  |                                          |
| Trạng thái       | Combobox search | TrangThai   | -          | N              | -                | Y                  | Chọn 1 trong các trạng thái trong entity |
| File đính kèm    | file            | FileDinhKem | -          | N              | -                | Y                  | Link file vừa tải lên, bấm để mở file    |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                  |
|:-------------|:-------|:-----------------------------------------------------------------------|
| Lưu          | Button | Kiểm tra hợp lệ, lưu dữ liệu vào ENT_CongChungVien (**UC_CCV_Update**) |
| Hủy          | Button | Hiển thị popup xác nhận hủy thao tác                                   |
| Tải lên      | Button | Upload ảnh công chứng viên, chỉ chấp nhận định dạng ảnh dưới 10MB.     |
| Tải lên file | Button | Tải lên file .pdf, .docs, .docx, tối đa 10MB                              |
| Xóa ảnh      | Button | Xóa ảnh công chứng viên vừa tải lên                                    |
| Xóa file     | Button | Xóa file chứng chỉ vừa tải lên                                         |

</div>
