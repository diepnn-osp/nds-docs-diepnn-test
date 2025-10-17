# Màn hình: Danh sách tài sản
Danh sách tài sản hiển thị trên form tạo lập/chỉnh sửa hoặc trang chi tiết giao dịch công chứng

## Điều kiện tiên quyết
- Nếu ở màn hình tạo lập/chỉnh sửa, người dùng cần đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Nếu ở màn hình chi tiết, người dùng cần đã đăng nhập và có quyền xem chi tiết giao dịch công chứng.
- Đã có dữ liệu tài sản

## Nguyên mẫu
[]

## Thành phần

### Danh sách tài sản

- Hiển thị dữ liệu đã ghi nhận/lưu

<div style="overflow-x:auto">

| Trường thông tin   | Control | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-------------------|:--------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| STT                | number  | -               | -          | -              | -                | -                  |       |
| Loại tài sản       | text    | LoaiTaiSan      | -          | -              | -                | -                  |       |
| Số giấy chứng nhận | text    | SoGiayChungNhan | -          | -              | -                | -                  |       |
| Ngày cấp           | date    | NgayCap         | -          | -              | -                | -                  |       |
| Nơi cấp            | text    | NoiCap          | -          | -              | -                | -                  |       |
| Chủ sở hữu         | text    | ChuSoHuu        | -          | -              | -                | -                  |       |
| Ghi chú            | text    | GhiChu          | -          | -              | -                | -                  |       |

</div>

### Nút chức năng

| Tên          | Loại   | Mô tả                                                                     |
|:-------------|:-------|:--------------------------------------------------------------------------|
| Xem chi tiết | Button | Click vào hiển thị popup chi tiết thông tin tài sản (**SCR_TSGD_Detail**) |

