# Màn hình: Cập nhật thông tin tài khoản người dùng
Form cho phép người dùng cập nhật thông tin tài khoản của mình sau khi đã đăng nhập hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng truy cập vào màn hình thông tin tài khoản (**SCR_User_Info.md**) và chọn chức năng "Cập nhật thông tin".

## Nguyên mẫu
[]

## Thành phần

### Form cập nhật thông tin
<div style="overflow-x:auto">
Tiêu đề: Cập nhật thông tin tài khoản

| Trường thông tin | Control | Field       | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:--------|:------------|:-----------------|:-------------------|:-----------------------------------------------|
| Tên tài khoản    | Text    | Username    | -                | N                  | Hiển thị tên đăng nhập của người dùng hiện tại |
| Họ và tên        | Text    | Hodem + Ten | -                | Y                  | Nhập họ và tên của người dùng                  |
| Đơn vị           | Text    | DonVi       | -                | N                  | Hiển thị đơn vị công tác của người dùng        |
| Chức vụ          | Text    | ChucVu      | -                | Y                  | Hiển thị chức vụ của người dùng                |
| Số điện thoại    | Text    | SoDienThoai | -                | Y                  | Nhập số điện thoại của người dùng              |
| Email            | Text    | Email       | -                | Y                  | Nhập email của người dùng                      |
| Địa chỉ          | Text    | DiaChi      | -                | Y                  | Nhập địa chỉ của người dùng                    |
| Vai trò          | Text    | VaiTro      | -                | N                  | Hiển thị vai trò của người dùng                |
| Trạng thái       | Text    | TrangThai   | -                | N                  | Hiển thị trạng thái người dùng                 |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                        |
|:---------------------|:--------|:---------------|:---------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi cập nhật thành công: **"Cập nhật thông tin tài khoản thành công"**              |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Cập nhật thông tin tài khoản thất bại"** hoặc **"Email đã tồn tại"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                                                       |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------|
| Lưu thông tin | Button | Thực hiện cập nhật thông tin tài khoản người dùng và hiển thị thông báo thành công (**UC_User_UpdateInfo**) |
| Hủy           | Button | Đóng form và quay về màn hình thông tin tài khoản (**SCR_User_Info.md**)                                    |

</div>

## Ghi chú
- Người dùng không thể thay đổi tên tài khoản, đơn vị.
- Email phải là duy nhất trong hệ thống.
- Số điện thoại phải đúng định dạng.
- Các trường thông tin được cập nhật sẽ được lưu vào **ENT_NguoiDung** trong hệ thống.