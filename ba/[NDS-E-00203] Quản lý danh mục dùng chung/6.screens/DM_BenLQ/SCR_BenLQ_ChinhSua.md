# Màn hình: Chỉnh sửa thông tin danh mục bên liên quan
Form cho phép chỉnh sửa thông tin danh mục bên liên quan.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền chỉnh sửa thông tin danh mục bên liên quan.

## Nguyên mẫu
[]

## Thành phần

### Form chỉnh sửa (DM_BenLQ)
- Tự động hiển thị thông tin đã lưu
<div style="overflow-x:auto">

| Trường thông tin         | Control       | Field         | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                               |
|:-------------------------|:--------------|:--------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------|
| Mã danh mục              | Text          | MaDM_BenLQ    | -          | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách |
| Tên giao dịch công chứng | Dropdown list | TenDM_TenGDCC | 250        | Y              | -                |                    | Chọn tên giao dịch công chứng       |
| Tên danh mục             | Text          | TenDM_BenLQ   | 250        | Y              | -                | Y                  | Điền vào tên danh mục bên liên quan |
| Trạng thái               | Boolean       | TT_DM_BenLQ   | -          | Y              | Active           | Y                  |                                     |
</div>

### Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                               |
|:--------------|:-------|:--------------------------------------------------------------------|
| Lưu thông tin | Button | Kiểm tra hợp lệ, lưu dữ liệu vào DM_BenLQ với trạng thái = "Active" |
| Đóng          | Button | Đóng popup                                                          |
