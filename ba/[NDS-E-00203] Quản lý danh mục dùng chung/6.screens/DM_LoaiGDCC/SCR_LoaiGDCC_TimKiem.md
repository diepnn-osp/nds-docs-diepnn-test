# Màn hình: Danh sách danh mục Loại giao dịch công chứng
Form cho phép tìm kiếm thông tin danh mục Loại giao dịch công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm (DM_LoaiGDCC)
- Tự động hiển thị danh sách danh mục 
- Ô tìm kiếm tự luôn xuất hiện trên top trang

<div style="overflow-x:auto">

| Trường thông tin | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                           |
|:-----------------|:---------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------|
| Mã danh mục      | Text     | MaDM_LoaiGDCC   | -         | Y              | -                | N                  | Mã danh mục tự tăng trong danh sách             |
| Tên danh mục     | Text     | TenDM_LoaiGDCC  | 250       | Y              | -                | Y                  |                                                 |
| Trạng thái       | Boolean  | TT_DM_LoaiGDCC  | -         | Y              | Active           | Y                  |                                                 |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                           |
|:-------------|:-------|:------------------------------------------------------------------------------------------------|
| Tìm kiếm     | Button | Kiểm tra hợp lệ và hiển thị danh sách thông tin danh mục Loại giao dịch công chứng theo từ khóa tìm kiếm          |
| Làm mới      | Button | Làm mới lại thông tin tìm kiếm                                                                  |
