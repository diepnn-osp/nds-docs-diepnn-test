# Màn hình: Chỉnh sửa thông tin danh mục chức vụ
Form cho phép chỉnh sửa thông tin danh mục chức vụ.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền chỉnh sửa thông tin danh mục chức vụ.

## Nguyên mẫu
[]

## Thành phần

### Form chỉnh sửa (DM_Chucvu)
- Tự động hiển thị thông tin đã lưu
<div style="overflow-x:auto">

| Trường thông tin | Control  | Field             | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                         |
|:-----------------|:---------|:----------------  |:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------|
| Mã danh mục      | Text     | MaDM_Chucvu       | -          | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách           |
| Tên danh mục     | Text     | TenDM_Chucvu      | 250        | Y              | -                |                    |                                               |
| Trạng thái       | Boolean  | TT_DM_Chucvu      | -          | Y              | Active           |                    |                                               |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Tên   | Mô tả                                                                                            |
|:-------------|:-------|:------------------------------------------------------------------------------------------------|
| Lưu thông tin| Button | Kiểm tra hợp lệ, lưu dữ liệu vào DM_Chucvu với trạng thái = "Active"                        |
| Đóng         | Button | Đóng popup                                                                                      |
