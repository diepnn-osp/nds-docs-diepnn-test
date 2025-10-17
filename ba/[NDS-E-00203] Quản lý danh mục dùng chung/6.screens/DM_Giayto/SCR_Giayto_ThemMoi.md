# Màn hình: Thêm mới thông tin danh mục giấy tờ
Form cho phép Thêm mới thông tin danh mục giấy tờ.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền Thêm mới thông tin danh mục giấy tờ.

## Nguyên mẫu
[]

## Thành phần

### Form Thêm mới (DM_Giayto)
- Hiển thị form thêm mới
<div style="overflow-x:auto">

| Trường thông tin | Control  | Field        -   | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:---------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Mã danh mục      | Text     | MaDM_Giayto      | -          | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách            |
| Tên danh mục     | Text     | TenDM_Giayto     | 250        | Y              | -                | Y                  |                                                |
| Loại giấy tờ     | Text     | Loai_Giayto      | 100        | Y              | -                | Y                  | Loại giấy tờ cho Cá nhân/Tổ chức               |
| Trạng thái       | Boolean  | TT_DM_Giayto     | -          | Y              | Active           |                    |                                                |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                           |
|:-------------|:-------|:------------------------------------------------------------------------------------------------|
| Lưu thông tin| Button | Kiểm tra hợp lệ, lưu dữ liệu vào DM_Giayto với trạng thái = "Active"                            |
| Đóng         | Button | Đóng popup                                                                                      |
