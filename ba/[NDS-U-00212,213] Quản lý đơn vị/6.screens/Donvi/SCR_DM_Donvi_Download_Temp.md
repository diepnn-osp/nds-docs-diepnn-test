# Màn hình: Tải về file mẫu import danh mục đơn vị
Màn hình cho phép người dùng tải về file mẫu import danh mục đơn vị từ danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền truy cập danh sách danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Nút tải về file mẫu
- Hiển thị trên màn hình danh sách danh mục đơn vị
<div style="overflow-x:auto">

| Thành phần | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                 |
|:----------|:--------|:------|:---------------|:----------------------------------------------------------------------|
| Nút tải về | Button  | -     | -              | Nút "Tải về file mẫu import" để tải file mẫu về thiết bị người dùng |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                 |
|:----------|:--------|:------|:---------------|:----------------------------------------------------------------------|
| Thông báo thành công | Label | - | - | Hiển thị khi tải về thành công: **"Tải về file mẫu thành công"** |
| Thông báo lỗi | Label | - | - | Hiển thị khi có lỗi: **"Tải về file mẫu thất bại"** hoặc **"Không tìm thấy file mẫu"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên | Loại | Mô tả |
|:----|:-----|:------|
| Tải về file mẫu import | Button | Lấy file mẫu từ danh mục file (**DM_Donvi_Download_Temp.xlsx**) và tải về thiết bị người dùng, sau đó hiển thị thông báo kết quả và quay về danh sách (**SCR_DM_Donvi_List**) |

</div>
