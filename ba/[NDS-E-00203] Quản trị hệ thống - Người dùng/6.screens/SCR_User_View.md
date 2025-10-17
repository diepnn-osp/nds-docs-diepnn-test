# Màn hình: Xem chi tiết thông tin tài khoản người dùng
Form cho phép xem thông tin chi tiết tài khoản người dùng trong hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem thông tin tài khoản người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form hiển thị thông tin
<div style="overflow-x:auto">

Tiêu đề: Thông tin chi tiết tài khoản người dùng

| Trường thông tin   | Control | Field           | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                               |
|:-------------------|:--------|:----------------|:-----------------|:-------------------|:----------------------------------------------------|
| Tên tài khoản      | Text    | Username        | -                | N                  | Hiển thị tên đăng nhập của tài khoản                |
| Họ và tên đệm      | Text    | HoDem + Ten     | -                | N                  | Hiển thị họ và tên của người dùng                   |
| Ngày sinh          | Text    | NgaySinh        | -                | N                  | Hiển thị ngày sinh của người dùng                   |
| Quốc tịch          | Text    | QuocTich        | -                | N                  | Hiển thị quốc tịch của người dùng                   |
| Dân tộc            | Text    | DanToc          | -                | N                  | Hiển thị dân tộc của người dùng                     |
| Điện thoại cố định | Text    | DienThoaiCoDinh | -                | N                  | Hiển thị số điện thoại cố định của người dùng       |
| Điện thoại di động | Text    | DienThoaiDiDong | -                | N                  | Hiển thị số điện thoại di động của người dùng       |
| Giới tính          | Text    | GioiTinh        | -                | N                  | Hiển thị giới tính của người dùng ("Nam" hoặc "Nữ") |
| Email              | Text    | Email           | -                | N                  | Hiển thị email của người dùng                       |
| Đơn vị             | Text    | DonViId         | -                | N                  | Hiển thị đơn vị công tác của người dùng             |
| Chức vụ            | Text    | ChucVuId        | -                | N                  | Hiển thị chức vụ của người dùng                     |
| Địa chỉ            | Text    | DiaChi          | -                | N                  | Hiển thị địa chỉ của người dùng                     |
| Tỉnh/Thành phố     | Text    | TinhThanhPho    | -                | N                  | Hiển thị tỉnh/thành phố của người dùng              |
| Phường/Xã          | Text    | PhuongXa        | -                | N                  | Hiển thị phường/xã của người dùng                   |
| Địa chỉ cũ         | Text    | DiaChiCu        | -                | N                  | Hiển thị địa chỉ cũ của người dùng                  |
| Tỉnh/Thành phố cũ  | Text    | TinhThanhPhoCu  | -                | N                  | Hiển thị tỉnh/thành phố cũ của người dùng           |
| Phường/Xã cũ       | Text    | PhuongXaCu      | -                | N                  | Hiển thị phường/xã cũ của người dùng                |
| Trạng thái         | Text    | TrangThai       | -                | N                  | Hiển thị trạng thái hoạt động của tài khoản         |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên      | Loại   | Mô tả                                                                    |
|:---------|:-------|:-------------------------------------------------------------------------|
| Cập nhật | Button | Mở form cập nhật thông tin tài khoản người dùng (**SCR_User_Update.md**) |
| Đóng     | Button | Đóng form và quay về danh sách (**SCR_User_List.md**)                    |

</div>