# Màn hình: Chỉnh sửa thông tin danh mục Tên giao dịch công chứng
Form cho phép chỉnh sửa thông tin danh mục Tên giao dịch công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền chỉnh sửa thông tin danh mục Tên giao dịch công chứng.

## Nguyên mẫu
[]

## Thành phần

### Form chỉnh sửa (DM_TenGDCC)
- Tự động hiển thị thông tin đã lưu
<div style="overflow-x:auto">

| Trường thông tin | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả     
|:-----------------|:---------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------|
| Mã danh mục      | Text     | MaDM_TenGDCC    | -          | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách             |
| Loại Giao dịch   | Dropdown list  | TenDM_LoaiGDCC   |            | Y              | -                |                    | Chọn loại Danh mục giao dịch công chứng|
| Tên danh mục     | Text     | TenDM_TenGDCC   | 250        | Y              | -                |                    |                                                 |
| Trạng thái       | Boolean  | TT_DM_TenGDCC   | -          | Y              | Active           |                    |                                                 |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên           | Tên    | Mô tả                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------|
| Lưu thông tin | Button | Kiểm tra hợp lệ, lưu dữ liệu vào DM_TenGDCC với trạng thái = "Active" |
| Đóng          | Button | Đóng popup                                                            |
