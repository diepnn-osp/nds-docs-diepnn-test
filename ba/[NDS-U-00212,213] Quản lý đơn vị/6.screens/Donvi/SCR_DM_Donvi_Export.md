# Màn hình: Xuất danh sách danh mục đơn vị
Màn hình cho phép người dùng xuất danh sách danh mục đơn vị từ danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền truy cập danh sách danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Nút xuất danh sách
- Hiển thị trên màn hình danh sách danh mục đơn vị
<div style="overflow-x:auto">

| Thành phần | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                 |
|:----------|:--------|:------|:---------------|:----------------------------------------------------------------------|
| Checkbox lựa chọn | Checkbox | - | - | Cho phép người dùng chọn các bản ghi cần xuất |
| Nút xuất danh sách | Button | - | - | Nút "Xuất danh sách" để xuất các bản ghi đã chọn |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                 |
|:----------|:--------|:------|:---------------|:----------------------------------------------------------------------|
| Thông báo thành công | Label | - | - | Hiển thị khi xuất thành công: **"Xuất danh sách thành công"** |
| Thông báo lỗi | Label | - | - | Hiển thị khi có lỗi: **"Không có dữ liệu để xuất"**, **"Lỗi hệ thống không thể tạo file xuất"**, hoặc **"Tải về file thất bại"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên | Loại | Mô tả |
|:----|:-----|:------|
| Xuất danh sách | Button | Lấy dữ liệu danh sách theo phạm vi truy cập của người dùng, tạo file xuất (Excel/CSV) với các trường (Mã danh mục, Tên đơn vị, Loại đơn vị, Đơn vị cha, Số điện thoại, Email, Fax, Website, Tỉnh/Thành phố, Phường/Xã, Địa chỉ, Thông tin khác, Trạng thái) và tải về thiết bị người dùng, sau đó hiển thị thông báo kết quả và quay về danh sách (**SCR_DM_Donvi_List**) |

</div>
