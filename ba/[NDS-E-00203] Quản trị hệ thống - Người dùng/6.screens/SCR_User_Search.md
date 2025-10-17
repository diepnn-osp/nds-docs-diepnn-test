# Màn hình: Tìm kiếm tài khoản người dùng
Màn hình cho phép người dùng quản lý tìm kiếm tài khoản người dùng trong danh sách người dùng thuộc đơn vị quản lý.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền quản lý người dùng.
- Tại danh sách tài khoản người dùng điền từ khóa, lọc điều kiện để tìm kiếm.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm
<div style="overflow-x:auto">
Tiêu đề: Tìm kiếm tài khoản người dùng

| Trường thông tin | Control         | Field       | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                            |
|:-----------------|:----------------|:------------|:-----------------|:-------------------|:-------------------------------------------------|
| Tên tài khoản    | Text            | Username    | -                | Y                  | Nhập tên đăng nhập để tìm kiếm                   |
| Họ và tên        | Text            | Hodem + Ten | -                | Y                  | Nhập họ và tên đệm để tìm kiếm                   |
| Đơn vị           | Combobox Search | DonVi       | -                | Y                  | Chọn đơn vị để lọc người dùng                    |
| Chức vụ          | Combobox Search | ChucVu      | -                | Y                  | Chọn chức vụ để lọc người dùng                   |
| Trạng thái       | Combobox Search | TrangThai   | -                | Y                  | Chọn trạng thái để lọc (Tất cả, Hoạt động, Khóa) |

</div>

### Kết quả tìm kiếm
<div style="overflow-x:auto">
Tiêu đề: Danh sách tài khoản người dùng

| STT | Tên tài khoản | Họ và tên đệm | Tên | Đơn vị | Chức vụ | Trạng thái | Thao tác                             |
|:----|:--------------|:--------------|:----|:-------|:--------|:-----------|:-------------------------------------|
| 1   | -             | -             | -   | -      | -       | -          | Xem, Sửa, Xóa, Đổi mật khẩu mặc định |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                          |
|:---------------------|:--------|:---------------|:-------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi tìm kiếm thành công: **"Tìm kiếm thành công"**                    |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Tìm kiếm thất bại"** hoặc **"Không tìm thấy kết quả"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên                   | Loại   | Mô tả                                                                                                           |
|:----------------------|:-------|:----------------------------------------------------------------------------------------------------------------|
| Tìm kiếm              | Button | Thực hiện tìm kiếm tài khoản người dùng dựa trên các điều kiện đã nhập và hiển thị kết quả (**UC_User_Search**) |
| Xóa điều kiện         | Button | Xóa tất cả các điều kiện tìm kiếm đã nhập                                                                       |
| Xem                   | Button | Chuyển đến màn hình xem chi tiết thông tin tài khoản người dùng (**SCR_User_View.md**)                          |
| Sửa                   | Button | Chuyển đến màn hình cập nhật thông tin tài khoản người dùng (**SCR_User_Update.md**)                            |
| Xóa                   | Button | Chuyển đến màn hình xóa tài khoản người dùng (**SCR_User_Delete.md**)                                           |
| Đổi mật khẩu mặc định | Button | Đổi mật khẩu của tài khoản người dùng về mật khẩu mặc định của hệ thống (**UC_User_ResetPass**)                 |
| Xuất danh sách        | Button | Xuất danh sách kết quả tìm kiếm ra file Excel                                                                   |

</div>

## Ghi chú
- Người dùng có thể tìm kiếm theo một hoặc nhiều điều kiện.
- Kết quả tìm kiếm chỉ hiển thị các tài khoản người dùng thuộc đơn vị quản lý của người dùng đang đăng nhập.
- Mật khẩu mặc định của hệ thống được quy định trong cấu hình hệ thống.
- Chỉ người dùng có quyền quản lý người dùng mới có thể thực hiện các thao tác Sửa, Xóa và Đổi mật khẩu mặc định.