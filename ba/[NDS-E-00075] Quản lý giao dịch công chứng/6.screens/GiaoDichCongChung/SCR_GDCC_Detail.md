# Màn hình: Chi tiết giao dịch công chứng

Màn hình hiển thị chi tiết giao dịch công chứng

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xem chi tiết giao dịch công chứng.

## Nguyên mẫu
[]

## Thành phần

### Thông tin chung

- Các trường thông tin được hiển thị theo cấu hình

| Trường thông tin       | Control | Field                 | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|------------------------|---------|-----------------------|------------|----------------|------------------|--------------------|-------|
| Ngày công chứng        | date    | NgayCongChung         | -          | -              | -                | -                  |       |
| Số công chứng          | text    | SoCongChung           | -          | -              | -                | -                  |       |
| Loại giao dịch         | text    | LoaiGiaoDichId        | -          | -              | -                | -                  |       |
| Tên giao dịch          | text    | TenGiaoDichId         | -          | -              | -                | -                  |       |
| Phương thức công chứng | text    | PhuongThucCongChungId | -          | -              | -                | -                  |       |
| Nội dung giao dịch     | text    | NoiDungGiaoDich       | -          | -              | -                | -                  |       |
| Giá trị giao dịch      | number  | GiaTri                | -          | -              | -                | -                  |       |
| Địa điểm công chứng    | text    | DiaDiemCongChung      | -          | -              | -                | -                  |       |
| Công chứng viên        | text    | CongChungVienId       | -          | -              | -                | -                  |       |
| Tổ chức công chứng     | text    | ToChucCongChungId     | -          | -              | -                | -                  |       |
| Thời hạn ủy quyền      | text    | ThoiHan               | -          | -              | -                | -                  |       |

### Thông tin giao dịch thế chấp

- Chỉ hiển thị với tên giao dịch loại thế chấp
- Các trường thông tin được hiển thị theo cấu hình

| Trường thông tin     | Control | Field             | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
|----------------------|---------|-------------------|------------|----------------|------------------|--------------------|----------------------------------|
| Trạng thái giải chấp | text    | TrangThaiGiaiChap | -          | -              | -                | -                  | Chọn 1 từ danh sách trong entity |
| Thời hạn giải chấp   | text    | ThoiHanGiaiChap       | -          | -              | -                | -                  |                                  |
| Ngày giải chấp       | date    | NgayGiaiChap      | -          | -              | -                | -                  |                                  |
| Ghi chú giải chấp    | text    | GhiChuGiaiChap    | -          | -              | -                | -                  |                                  |


### Thông tin khác

- Các trường thông tin được hiển thị theo cấu hình

| Trường thông tin   | Control | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|--------------------|---------|-----------------|------------|----------------|------------------|--------------------|-------|
| Phí công chứng     | number  | PhiCongChung    | -          | -              | -                | -                  |       |
| Thù lao công chứng | number  | ThuLaoCongChung | -          | -              | -                | -                  |       |
| Ghi chú            | text    | GhiChu          | -          | -              | -                | -                  |       |

### Thông tin bên liên quan

#### Danh sách bên liên quan

| Trường thông tin | Control | Field               | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|------------------|---------|---------------------|------------|----------------|------------------|--------------------|-------|
| Bên liên quan    | text    | ThongTinBenLienQuan | -          | -              | -                | -                  |       |

##### Danh sách người tham gia giao dịch

- Với mỗi bên liên quan, hiển thị bảng danh sách cá nhân và tổ chức tham gia giao dịch đã được thêm. Mô tả trong (**SCR_NTGGD_List**)
- Danh sách người tham gia giao dịch được hiển thị theo cấu hình

### Thông tin tài sản giao dịch

- Với mỗi loại tài sản, hiển thị danh sách tài sản giao dịch. Mô tả trong (**SCR_TSGD_List**)
- Danh sách tài sản được hiển thị theo cấu hình

### Tài liệu đính kèm

#### Danh sách tài liệu

- Danh sách file được hiển thị theo cấu hình

- Công chứng giấy

| Trường thông tin           | Control | Field   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                     |
|----------------------------|---------|---------|------------|----------------|------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Văn bản công chứng điện tử | text    | TenFile | -          | -              | -                | -                  | Hiển thị tên file văn bản công chứng điện tử đã tải lên (Lấy theo FileVanBanCongChungDienTuId). Click vào mở preview file |
| Hồ sơ lưu trữ điện tử      | text    | TenFile | -          | -              | -                | -                  | Hiển thị tên file hồ sơ lưu trữ điện tử (Lấy theo FileHoSoLuuTruDienTuId). Click vào mở preview file                      |
| Thành phần hồ sơ khác      | text    | TenFile | -          | -              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file trong danh sách. Click mở preview file                                       |

- Công chứng điện tử

| Trường thông tin           | Control | Field   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                     |
|----------------------------|---------|---------|------------|----------------|------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Văn bản công chứng điện tử | text    | TenFile | -          | -              | -                | -                  | Hiển thị tên file văn bản công chứng điện tử đã tải lên (Lấy theo FileVanBanCongChungDienTuId). Click vào mở preview file |
| Văn bản sửa lỗi kỹ thuật   | text    | TenFile | -          | -              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file. Click mở preview file                              |
| Thành phần hồ sơ khác      | text    | TenFile | -          | -              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file trong danh sách. Click mở preview file                                       |

### Các nút chức năng

| Tên chức năng        | Loại   | Mô tả                                                                                           |
|----------------------|--------|-------------------------------------------------------------------------------------------------|
| Đóng                 | Button | Quay trở lại màn hình danh sách (**SCR_GDCC_List**)                                             |
| Quay lại             | Button | Quay trở lại màn hình danh sách (**SCR_GDCC_List**)                                             |
| Xem lịch sử cập nhật | Button | Hiển thị nếu có quyền, click vào mở popup xem lịch sử cập nhật giao dịch (**SCR_GDCC_History**) |
