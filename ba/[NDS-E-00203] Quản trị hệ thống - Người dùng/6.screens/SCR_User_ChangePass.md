# Màn hình: Đổi mật khẩu người dùng
Form cho phép người dùng đổi mật khẩu tài khoản của mình sau khi đăng nhập vào hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng truy cập vào màn hình thông tin tài khoản và chọn chức năng "Đổi mật khẩu".

## Nguyên mẫu
[]

## Thành phần

### Form đổi mật khẩu
<div style="overflow-x:auto">
Tiêu đề: Đổi mật khẩu

| Trường thông tin      | Control  | Field             | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:----------------------|:---------|:------------------|:-----------------|:-------------------|:-----------------------------------------------|
| Tên tài khoản         | Text     | Username          | -                | N                  | Hiển thị tên đăng nhập của người dùng hiện tại |
| Mật khẩu hiện tại     | Password | MatKhauHienTai    | -                | Y                  | Nhập mật khẩu hiện tại của người dùng          |
| Mật khẩu mới          | Password | MatKhauMoi        | -                | Y                  | Nhập mật khẩu mới của người dùng               |
| Xác nhận mật khẩu mới | Password | XacNhanMatKhauMoi | -                | Y                  | Nhập lại mật khẩu mới để xác nhận              |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                                                                        |
|:---------------------|:--------|:---------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi đổi mật khẩu thành công: **"Đổi mật khẩu thành công"**                                                                          |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Đổi mật khẩu thất bại"**, **"Mật khẩu hiện tại không đúng"** hoặc **"Mật khẩu mới và xác nhận mật khẩu không khớp"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                       |
|:-------------|:-------|:--------------------------------------------------------------------------------------------|
| Đổi mật khẩu | Button | Thực hiện đổi mật khẩu người dùng và hiển thị thông báo thành công (**UC_User_ChangePass**) |
| Hủy          | Button | Đóng form và quay về màn hình thông tin tài khoản (**SCR_User_Info**)                    |

</div>

## Ghi chú
- Mật khẩu mới phải tuân thủ quy định về độ phức tạp của hệ thống.
- Mật khẩu mới không được trùng với mật khẩu hiện tại.
- Mật khẩu mới và xác nhận mật khẩu mới phải khớp nhau.
- Sau khi đổi mật khẩu thành công, hệ thống sẽ yêu cầu người dùng đăng nhập lại với mật khẩu mới.