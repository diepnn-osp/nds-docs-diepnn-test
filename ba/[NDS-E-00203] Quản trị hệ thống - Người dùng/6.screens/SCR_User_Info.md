# Màn hình: Thông tin tài khoản người dùng
Màn hình cho phép người dùng xem thông tin tài khoản của mình sau khi đã đăng nhập hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng truy cập vào mục thông tin tài khoản.

## Nguyên mẫu
[]

## Thành phần

### Thông tin tài khoản
<div style="overflow-x:auto">
Tiêu đề: Thông tin tài khoản

| Trường thông tin | Control | Field       | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:--------|:------------|:-----------------|:-------------------|:-----------------------------------------------|
| Tên tài khoản    | Text    | Username    | -                | N                  | Hiển thị tên đăng nhập của người dùng hiện tại |
| Họ và tên        | Text    | Hodem + Ten | -                | N                  | Hiển thị họ và tên của người dùng              |
| Đơn vị           | Text    | DonVi       | -                | N                  | Hiển thị đơn vị công tác của người dùng        |
| Chức vụ          | Text    | ChucVu      | -                | N                  | Hiển thị chức vụ của người dùng                |
| Số điện thoại    | Text    | SoDienThoai | -                | N                  | Hiển thị số điện thoại của người dùng          |
| Email            | Text    | Email       | -                | N                  | Hiển thị email của người dùng                  |
| Địa chỉ          | Text    | DiaChi      | -                | N                  | Hiển thị địa chỉ của người dùng                |
| Trạng thái       | Text    | TrangThai   | -                | N                  | Hiển thị trạng thái tài khoản (Hoạt động/Khóa) |

</div>

### Chức năng
<div style="overflow-x:auto">

| Tên                | Loại   | Mô tả                                                                         |
|:-------------------|:-------|:------------------------------------------------------------------------------|
| Cập nhật thông tin | Button | Chuyển đến màn hình cập nhật thông tin tài khoản (**SCR_User_UpdateInfo.md**) |
| Đổi mật khẩu       | Button | Chuyển đến màn hình đổi mật khẩu (**SCR_User_ChangePass.md**)                 |
| Đóng               | Button | Đóng màn hình thông tin tài khoản và quay về màn hình chính                   |

</div>

## Ghi chú
- Màn hình này chỉ hiển thị thông tin tài khoản của người dùng đang đăng nhập.
- Người dùng không thể chỉnh sửa thông tin trực tiếp trên màn hình này mà phải chuyển đến màn hình cập nhật thông tin.
- Các thông tin được hiển thị dựa trên dữ liệu từ entity NguoiDung trong hệ thống.