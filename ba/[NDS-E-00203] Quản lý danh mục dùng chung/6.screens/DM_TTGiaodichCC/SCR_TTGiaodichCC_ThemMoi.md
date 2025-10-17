# Màn hình: Thêm mới thông tin danh mục trạng thái giao dịch công chứng
Form cho phép Thêm mới thông tin danh mục trạng thái giao dịch công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền Thêm mới thông tin danh mục trạng thái giao dịch công chứng.

## Nguyên mẫu
[]

## Thành phần

### Form Thêm mới (DM_TTGiaodichCC)
- Hiển thị form thêm mới
<div style="overflow-x:auto">

| Trường thông tin | Control  | Field        -   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:---------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
|STT               | int      | STT             | 3          | Y              | -                |                     | Hiển thị số thứ tự tự tăng theo bản ghi      |
| Mã danh mục      | Text     | MaDM_TTGiaodich  | -          | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách            |
| Tên danh mục     | Text     | TenDM_TTGiaodich | 250        | Y              | -                |                    |                                                |
| Trạng thái       | Boolean  | TT_DM_TTGiaodich | -          | Y              | Active           |                    |                                                |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Tên   | Mô tả                                                                                            |
|:-------------|:-------|:------------------------------------------------------------------------------------------------|
| Lưu thông tin| Button | Kiểm tra hợp lệ, lưu dữ liệu vào DM_TTGiaodich với trạng thái = "Active"                           |
| Đóng         | Button | Đóng popup                                                                                      |
