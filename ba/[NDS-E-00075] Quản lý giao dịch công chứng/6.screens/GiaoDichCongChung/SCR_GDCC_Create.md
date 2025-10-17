# Màn hình: Thêm mới giao dịch công chứng

Form cho phép nhập và lưu thông tin giao dịch công chứng mới vào hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền thêm mới giao dịch công chứng.

## Nguyên mẫu
[]

## Thành phần

### Thông tin chung

| Trường thông tin       | Control         | Field               | Max length | Bắt buộc (Y/N) | Giá trị mặc định                   | Cho phép sửa (Y/N) | Mô tả                                                                                                                                                     |
|------------------------|-----------------|---------------------|------------|----------------|------------------------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ngày công chứng        | date            | NgayCongChung       | -          | Y              | -                                  | -                  |                                                                                                                                                           |
| Số công chứng          | text            | SoCongChung         | 50         | Y              | -                                  | -                  | **BR9.13**                                                                                                                                                          |
| Phương thức công chứng | dropdown        | PhuongThucCongChung | -          | Y              | Công chứng giấy/Công chứng điện tử | N                  | Disabled, không cho phép thay đổi                                                                                                                         |
| Loại giao dịch         | combobox search | LoaiGiaoDichId      | -          | Y              | -                                  | -                  | Chọn từ danh mục loại giao dịch                                                                                                                           |
| Tên giao dịch          | combobox search | TenGiaoDichId       | -          | Y              | -                                  | -                  | Chọn từ danh mục tên giao dịch liên kết với loại giao dịch đã chọn                                                                                        |
| Nội dung giao dịch     | textarea        | NoiDungGiaoDich     | 2000       | N              | -                                  | -                  |                                                                                                                                                           |
| Giá trị giao dịch      | number          | GiaTri              | -          | N              | -                                  | -                  |                                                                                                                                                           |
| Địa điểm công chứng    | text            | DiaDiemCongChung    | 500        | Y              | -                                  | -                  |                                                                                                                                                           |
| Tổ chức công chứng     | combobox search | ToChucCongChungId   | -          | Y              | THNCC của người đang tạo lập       | N                  | Chọn 1 từ danh sách tổ chức công chứng thực hiện yêu cầu chuyển quyền sở hữu hồ sơ (**ENT_YeuCauChuyenQuyenSoHuuHoSo**) + Tổ chức công chứng đang tạo lập |
| Công chứng viên        | combobox search | CongChungVienId     | -          | Y              | -                                  | -                  | Chọn 1 từ danh sách công chứng viên thuộc tổ chức công chứng đã chọn                                                                                      |
| Thời hạn ủy quyền      | text            | ThoiHan             | 100        | Y              | -                                  | -                  | Hiển thị đối với tên giao dịch loại ủy quyền                                                                                                              |

### Thông tin giao dịch thế chấp

- Chỉ hiển thị với tên giao dịch loại thế chấp

| Trường thông tin     | Control         | Field             | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
|----------------------|-----------------|-------------------|------------|----------------|------------------|--------------------|----------------------------------|
| Trạng thái giải chấp | combobox search | TrangThaiGiaiChap | -          | Y              | Chưa giải chấp   | Y                  | Chọn 1 từ danh sách trong entity |
| Thời hạn giải chấp   | text            | ThoiHanGiaiChap   | 50         | N              | -                | -                  |                                  |
| Ngày giải chấp       | date            | NgayGiaiChap      | -          | Y              | -                | -                  |                                  |
| Ghi chú giải chấp    | textarea        | GhiChuGiaiChap    | 500        | N              | -                | -                  |                                  |


### Thông tin khác
| Trường thông tin   | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|--------------------|----------|-----------------|------------|----------------|------------------|--------------------|-------|
| Phí công chứng     | number   | PhiCongChung    | 20         | N              | -                | -                  |       |
| Thù lao công chứng | number   | ThuLaoCongChung | 20         | N              | -                | -                  |       |
| Ghi chú            | textarea | GhiChu          | 1000       | N              | -                | -                  |       |

### Thông tin bên liên quan

#### Danh sách bên liên quan

- Mặc định luôn hiển thị 1 bên liên quan, không cho phép xóa nếu còn duy nhất 1 bên liên quan

| Trường thông tin | Control         | Field               | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                                |
|------------------|-----------------|---------------------|------------|----------------|------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Bên liên quan    | combobox search | ThongTinBenLienQuan | -          | Y              | -                | -                  | Hiển thị trường này với mỗi bên liên quan được thêm vào form giao dịch. Chọn giá trị từ danh mục bên liên quan gắn với tên giao dịch |

##### Danh sách người tham gia giao dịch

- Với mỗi bên liên quan, hiển thị bảng danh sách cá nhân và tổ chức tham gia giao dịch đã được thêm. Mô tả trong (**SCR_NTGGD_List**)

##### Các nút chức năng

| Tên chức năng                      | Loại   | Mô tả                                                                                                                                   |
|------------------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Thêm mới người tham gia giao dịch  | Button | Click vào mở popup thêm mới người tham gia giao dịch (**SCR_NTGGD_Create**)                                                             |
| Xóa người tham gia giao dịch       | Button | Hiển thị trên mỗi dòng danh sách người tham gia giao dịch, Click vào mở popup xác nhận xóa (**SCR_NTGGD_Delete**)                       |
| Chỉnh sửa người tham gia giao dịch | Button | Hiển thị trên mỗi dòng danh sách người tham gia giao dịch, Click vào mở popup chỉnh sửa người tham gia giao dịch (**SCR_NTGGD_Update**) |

#### Các nút chức năng

| Tên chức năng          | Loại   | Mô tả                                                                                                                                                             |
|------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Thêm mới bên liên quan | Button | Click vào thêm mới 1 bên liên quan vào danh sách (**UC_BLQ_Create**)                                                                                              |
| Xóa bên liên quan      | Button | Hiển thị ở mỗi bên liên quan đã tạo, click vào thực hiện luồng xóa bên liên quan (**UC_BLQ_Delete**). Nút này không hiển thị nếu chỉ có duy nhất 1 bên liên quan |

### Thông tin tài sản giao dịch

#### Danh sách tài sản giao dịch

- Với mỗi loại tài sản, hiển thị danh sách tài sản giao dịch. Mô tả trong (**SCR_TSGD_List**)

#### Các nút chức năng

| Tên chức năng     | Loại   | Mô tả                                                                                                     |
|-------------------|--------|-----------------------------------------------------------------------------------------------------------|
| Thêm mới tài sản  | Button | Click vào mở popup thêm mới tài sản giao dịch (**SCR_TSGD_Create**)                                       |
| Xóa tài sản       | Button | Hiển thị ở mỗi tài sản đã tạo, click vào mở popup xác nhận xóa (**SCR_TSGD_Delete**)                      |
| Chỉnh sửa tài sản | Button | Hiển thị ở mỗi bên tài sản đã tạo, click vào mở popup chỉnh sửa tài sản giao dịch (**SCR_TSGD_Update**) |


### Tài liệu đính kèm

#### Danh sách tài liệu

- Công chứng giấy

| Trường thông tin           | Control | Field   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                     |
|----------------------------|---------|---------|------------|----------------|------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Văn bản công chứng điện tử | text    | TenFile | -          | N              | -                | -                  | Hiển thị tên file văn bản công chứng điện tử đã tải lên (Lấy theo FileVanBanCongChungDienTuId). Click vào mở preview file |
| Hồ sơ lưu trữ điện tử      | text    | TenFile | -          | N              | -                | -                  | Hiển thị tên file hồ sơ lưu trữ điện tử (Lấy theo FileHoSoLuuTruDienTuId). Click vào mở preview file                      |
| Thành phần hồ sơ khác      | text    | TenFile | -          | N              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file trong danh sách. Click mở preview file                                       |

- Công chứng điện tử

| Trường thông tin           | Control | Field   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                     |
|----------------------------|---------|---------|------------|----------------|------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| Văn bản công chứng điện tử | text    | TenFile | -          | Y              | -                | -                  | Hiển thị tên file văn bản công chứng điện tử đã tải lên (Lấy theo FileVanBanCongChungDienTuId). Click vào mở preview file |
| Văn bản sửa lỗi kỹ thuật   | text    | TenFile | -          | N              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file trong danh sách. Click mở preview file                                |
| Thành phần hồ sơ khác      | text    | TenFile | -          | Y              | -                | -                  | Mỗi file đã tải lên hiển thị 1 dòng tên file trong danh sách. Click mở preview file                                       |

#### Các nút chức năng

| Tên chức năng                           | Loại   | Mô tả                                                                            |
|-----------------------------------------|--------|----------------------------------------------------------------------------------|
| Tải lên file văn bản công chứng điện tử | Button | Cho phép tải lên 1 file *.pdf dưới 50Mb. Ẩn đi sau khi tải lên thành công        |
| Tải lên file hồ sơ lưu trữ điện tử      | Button | Cho phép tải lên 1 file *.pdf dưới 50Mb. Ẩn đi sau khi tải lên thành công        |
| Tải lên văn bản sửa lỗi kỹ thuật        | Button | Cho phép tải lên nhiều file *.pdf, *.docs, *docx, *.jpeg, *.png, *.jpg dưới 50Mb |
| Tải lên thành phần hồ sơ khác           | Button | Cho phép tải lên nhiều file *.pdf, *.docs, *docx, *.jpeg, *.png, *.jpg dưới 50Mb |
| Xóa file                                | Button | Hiển thị cạnh tên tài liệu vừa tải lên, click vào xóa tài liệu vừa tải lên       |

### Các nút chức năng

| Tên chức năng  | Loại   | Mô tả                                               |
|----------------|--------|-----------------------------------------------------|
| Lưu nháp       | Button | Thực hiện luồng lưu nháp (**UC_GDCC_Create**)       |
| Lưu chính thức | Button | Thực hiện luồng lưu chính thức (**UC_GDCC_Create**) |
| Hủy            | Button | Hiển thị popup xác nhận hủy thao tác                |
