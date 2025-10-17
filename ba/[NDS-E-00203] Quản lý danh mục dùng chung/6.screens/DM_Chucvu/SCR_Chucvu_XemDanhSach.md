# Màn hình: Danh sách danh mục chức vụ
- Cho phép hiển thị danh sách danh mục chức vụ theo thứ tự mới tạo lên đầu tiên.
- Cho phép tìm kiếm thông tin danh mục chức vụ.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem danh sách danh mục chức vụ.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm (DM_Chucvu)
- Tự động hiển thị danh sách danh mục 
- Ô tìm kiếm tự luôn xuất hiện trên top trang

<div style="overflow-x:auto">
Tiêu đề: Danh sách chức vụ
| Trường thông tin | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                           |
|:-----------------|:---------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------|
|STT               | int      | STT             | 3          | Y              | -                |                     | Hiển thị số thứ tự tự tăng theo bản ghi      |
| Mã danh mục      | Text     | MaDM_Chucvu     | -          | Y             | -                 | N                  | Mã danh mục tự tăng trong danh sách             |
| Tên danh mục     | Text     | TenDM_Chucvu    | 250        | Y             | -                 | Y                  |                                                 |
| Trạng thái       | Boolean  | TT_DM_Chucvu    | -          | Y             | Active            | Y                  |                                                 |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Tên    | Mô tả                                                                                                              |
|:-------------|:-------|:-------------------------------------------------------------------------------------------------------------------|
| Thêm mới     | Button | Mở form thêm mới danh mục chức vụ (SCR_Chucvu_Themoi)                                                     |
| Sửa          | Button | Mở form Sửa thông tin danh mục chức vụ (SCR_Chucvu_ChinhSua)                                              |
| Xóa          | Button | Hiển thị alert xác nhận xóa (SRC_Chucvu_Xoa)    


                                                               |
