# Màn hình: Khóa/Mở khóa tài khoản người dùng
Form cho phép người dùng quản lý khóa hoặc mở khóa một hoặc nhiều tài khoản người dùng trong danh sách thuộc đơn vị quản lý.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền khóa/mở khóa tài khoản người dùng.
- Người dùng đã chọn một hoặc nhiều tài khoản từ danh sách người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form xác nhận khóa/mở khóa
<div style="overflow-x:auto">
Tiêu đề: Khóa/Mở khóa tài khoản người dùng

| Trường thông tin    | Control  | Field         | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                 |
|:--------------------|:---------|:--------------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------|
| Danh sách tài khoản | List     | SelectedUsers | -          | Y              | -                | N                  | Hiển thị danh sách các tài khoản người dùng được chọn |
| Hành động           | Radio    | Action        | -          | Y              | -                | Y                  | Chọn hành động (Khóa hoặc Mở khóa)                    |
| Lý do               | Textarea | Reason        | 255        | Y              | -                | Y                  | Nhập lý do khóa/mở khóa tài khoản                     |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                                                                                |
|:---------------------|:--------|:---------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi khóa/mở khóa thành công: **"Khóa tài khoản thành công"** hoặc **"Mở khóa tài khoản thành công"**                                        |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Tài khoản đã bị khóa trước đó"** hoặc **"Tài khoản đang ở trạng thái hoạt động"** hoặc **"Khóa/Mở khóa tài khoản thất bại"** |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên      | Loại   | Mô tả                                                                                              |
|:---------|:-------|:---------------------------------------------------------------------------------------------------|
| Xác nhận | Button | Thực hiện khóa/mở khóa tài khoản người dùng và hiển thị thông báo kết quả (**UC_User_LockUnLock**) |
| Hủy      | Button | Đóng form và quay về danh sách người dùng (**SCR_User_List.md** hoặc **SCR_User_Search.md**)       |

</div>

## Ghi chú
- Người dùng phải chọn ít nhất một tài khoản để thực hiện khóa/mở khóa.
- Lý do khóa/mở khóa là thông tin bắt buộc.
- Khi khóa tài khoản, hệ thống sẽ cập nhật trạng thái tài khoản thành "Khóa" và ghi log lịch sử khóa tài khoản.
- Khi mở khóa tài khoản, hệ thống sẽ cập nhật trạng thái tài khoản thành "Hoạt động" và ghi log lịch sử mở khóa tài khoản.
- Sau khi thực hiện thành công, danh sách người dùng sẽ được cập nhật để hiển thị trạng thái mới.