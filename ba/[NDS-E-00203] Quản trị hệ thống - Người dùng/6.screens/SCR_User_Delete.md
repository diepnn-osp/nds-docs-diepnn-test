# Màn hình: Xóa tài khoản người dùng
Form cho phép xóa mềm tài khoản người dùng trong hệ thống. Chỉ áp dụng cho tài khoản quản trị, chuyên viên thuộc BTP/STP được tạo tài khoản.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xóa tài khoản người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form xác nhận xóa
<div style="overflow-x:auto">
Tiêu đề: Xóa tài khoản người dùng

| Trường thông tin | Control  | Field       | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                            |
|:-----------------|:---------|:------------|:-----------------|:-------------------|:-------------------------------------------------|
| Tên tài khoản    | Text     | Username    | -                | N                  | Hiển thị tên đăng nhập của tài khoản cần xóa     |
| Họ và tên        | Text     | Hodem + Ten | -                | N                  | Hiển thị họ và tên đầy đủ của người dùng cần xóa |
| Đơn vị           | Text     | DonVi       | -                | N                  | Hiển thị đơn vị công tác của người dùng cần xóa  |
| Vai trò          | Text     | VaiTro      | -                | N                  | Hiển thị vai trò của người dùng cần xóa          |
| Lý do xóa        | Textarea | LyDoXoa     | -                | Y                  | Nhập lý do xóa tài khoản người dùng              |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                               |
|:---------------------|:--------|:---------------|:----------------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi xóa thành công: **"Xóa tài khoản người dùng thành công"**                              |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Xóa tài khoản người dùng thất bại"** hoặc **"Không thể xóa tài khoản này"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                                                                             |
|:--------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------|
| Xóa tài khoản | Button | Thực hiện xóa mềm tài khoản người dùng (cập nhật trạng thái thành "Không sử dụng") và hiển thị thông báo thành công (**UC_User_Delete**) |
| Hủy           | Button | Đóng form và quay về danh sách (**SCR_User_List).md**)                                                                             |

</div>

## Ghi chú
- Chỉ áp dụng cho tài khoản quản trị, chuyên viên thuộc BTP/STP được tạo tài khoản.
- Thực hiện xóa mềm tài khoản, không xóa hẳn khỏi hệ thống.
- Lý do xóa là thông tin bắt buộc phải nhập.