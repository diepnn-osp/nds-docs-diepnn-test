# Màn hình: Đặt lại mật khẩu người dùng
Form cho phép người dùng có vai trò quản lý người dùng đặt lại mật khẩu của người dùng được chọn về mật khẩu mặc định.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền đặt lại mật khẩu người dùng.
- Người dùng đã chọn một hoặc nhiều tài khoản từ danh sách người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form xác nhận đặt lại mật khẩu
<div style="overflow-x:auto">
Tiêu đề: Đặt lại mật khẩu người dùng

| Trường thông tin       | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định                      | Cho phép sửa (Y/N) | Mô tả                                                 |
|:-----------------------|:---------|:----------------|:-----------|:---------------|:--------------------------------------|:-------------------|:------------------------------------------------------|
| Danh sách tài khoản    | List     | SelectedUsers   | -          | Y              | -                                     | N                  | Hiển thị danh sách các tài khoản người dùng được chọn |
| Lý do đặt lại mật khẩu | Textarea | Reason          | 255        | Y              | -                                     | Y                  | Nhập lý do đặt lại mật khẩu tài khoản                 |
| Mật khẩu mặc định      | Text     | DefaultPassword | -          | N              | [Mật khẩu mặc định theo quy tắc BR13] | N                  | Hiển thị mật khẩu mặc định sẽ được đặt cho tài khoản  |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                                                           |
|:---------------------|:--------|:---------------|:--------------------------------------------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi đặt lại mật khẩu thành công: **"Đặt lại mật khẩu thành công. Mật khẩu mặc định đã được gửi về email người dùng."** |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Đặt lại mật khẩu thất bại"** hoặc **"Không thể đặt lại mật khẩu cho tài khoản đang bị khóa"**           |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên      | Loại   | Mô tả                                                                                                                      |
|:---------|:-------|:---------------------------------------------------------------------------------------------------------------------------|
| Xác nhận | Button | Thực hiện đặt lại mật khẩu tài khoản người dùng về mật khẩu mặc định và hiển thị thông báo kết quả (**UC_User_ResetPass**) |
| Hủy      | Button | Đóng form và quay về danh sách người dùng (**SCR_User_List.md** hoặc **SCR_User_Search.md**)                               |

</div>

## Ghi chú
- Người dùng phải chọn ít nhất một tài khoản để thực hiện đặt lại mật khẩu.
- Lý do đặt lại mật khẩu là thông tin bắt buộc.
- Mật khẩu mặc định được tạo theo quy tắc BR13 trong file business_rules.md.
- Khi đặt lại mật khẩu, hệ thống sẽ cập nhật mật khẩu mới cho tài khoản và ghi log lịch sử thay đổi mật khẩu.
- Sau khi thực hiện thành công, hệ thống sẽ gửi thông báo về email của người dùng được đặt lại mật khẩu.
- Không thể đặt lại mật khẩu cho tài khoản đang ở trạng thái khóa.