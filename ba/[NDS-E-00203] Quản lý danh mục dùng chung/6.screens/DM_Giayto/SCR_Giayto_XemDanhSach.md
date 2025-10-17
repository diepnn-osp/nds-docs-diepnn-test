# Màn hình: Danh sách danh mục giấy tờ
- Cho phép hiển thị danh sách danh mục giấy tờ theo thứ tự mới tạo lên đầu tiên.
- Cho phép tìm kiếm thông tin danh mục giấy tờ.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem danh sách danh mục giấy tờ.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm (DM_Giayto)
- Tự động hiển thị danh sách danh mục 
- Ô tìm kiếm tự luôn xuất hiện trên top trang

<div style="overflow-x:auto">
Tiêu đề: Danh sách giấy tờ
| Trường thông tin | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                           |
|:-----------------|:---------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------|
|STT               | int      | STT             | 3          | Y              | -                |                     | Hiển thị số thứ tự tự tăng theo bản ghi      |
| Mã danh mục      | Text     | MaDM_Giayto     | -          | -              | -                | -                  | Mã danh mục tự tăng trong danh sách             |
| Tên danh mục     | Text     | TenDM_Giayto    | 250        | -              | -                | -                  |                                                 |
| Loại giấy tờ     | Text     | Loai_Giayto     | 100        | -              | -                | -                  | Loại giấy tờ cho Cá nhân/Tổ chức               |
| Trạng thái       | Boolean  | TT_DM_Giayto    | -          | -              | -                | -                  |                                                 |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                                         |
|:-------------|:-------|:--------------------------------------------------------------------------------------------------------------|
| Thêm mới     | Button | Mở form thêm mới danh mục giấy tờ (SCR_Giayto_Themoi)                                                         |
| Sửa          | Button | Mở form Sửa thông tin danh mục giấy tờ (SCR_Giayto_ChinhSua)                                                  |
| Xóa          | Button | Hiển thị alert xác nhận xóa (SRC_Giayto_Xoa)                                                                  |
