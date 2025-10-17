# Màn hình: Thêm mới tài khoản người dùng
Form cho phép thêm mới tài khoản người dùng vào hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền thêm mới tài khoản người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form nhập liệu
<div style="overflow-x:auto">
Tiêu đề: Thêm mới tài khoản người dùng

| Trường thông tin   | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                         |
|:-------------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------|
| Tên tài khoản      | Text            | Username        | 50         | Y              | -                | N                  | Nhập tên đăng nhập của tài khoản              |
| Họ và tên          | Text            | HoDem + Ten     | 50         | Y              | -                | Y                  | Nhập họ và tên của người dùng                 |
| Ngày sinh          | Date            | NgaySinh        | -          | N              | -                | Y                  | Nhập ngày sinh của người dùng                 |
| Quốc tịch          | Text            | QuocTich        | 50         | N              | Việt Nam         | Y                  | Nhập quốc tịch của người dùng                 |
| Dân tộc            | Text            | DanToc          | 50         | N              | Kinh             | Y                  | Nhập dân tộc của người dùng                   |
| Điện thoại cố định | Text            | DienThoaiCoDinh | 20         | N              | -                | Y                  | Nhập số điện thoại cố định của người dùng     |
| Điện thoại di động | Text            | DienThoaiDiDong | 20         | N              | -                | Y                  | Nhập số điện thoại di động của người dùng     |
| Giới tính          | Dropdown        | GioiTinh        | -          | Y              | -                | Y                  | Chọn giới tính của người dùng (1: Nam, 2: Nữ) |
| Email              | Text            | Email           | 100        | Y              | -                | Y                  | Nhập email của người dùng                     |
| Đơn vị             | Combobox Search | DonViId         | -          | Y              | -                | Y                  | Chọn đơn vị công tác của người dùng           |
| Chức vụ            | Combobox Search | ChucVuId        | -          | N              | -                | Y                  | Chọn chức vụ của người dùng                   |
| Địa chỉ            | Text            | DiaChi          | 255        | N              | -                | Y                  | Nhập địa chỉ của người dùng                   |
| Tỉnh/Thành phố     | Combobox Search | TinhThanhPho    | -          | N              | -                | Y                  | Chọn tỉnh/thành phố của người dùng            |
| Phường/Xã          | Combobox Search | PhuongXa        | -          | N              | -                | Y                  | Chọn phường/xã của người dùng                 |
| Địa chỉ cũ         | Text            | DiaChiCu        | 255        | N              | -                | Y                  | Nhập địa chỉ cũ của người dùng                |
| Tỉnh/Thành phố cũ  | Combobox Search | TinhThanhPhoCu  | -          | N              | -                | Y                  | Chọn tỉnh/thành phố cũ của người dùng         |
| Phường/Xã cũ       | Combobox Search | PhuongXaCu      | -          | N              | -                | Y                  | Chọn phường/xã cũ của người dùng              |
| Trạng thái         | Combobox Search | TrangThai       | -          | Y              | Active           | Y                  | Trạng thái hoạt động của tài khoản            |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                 |
|:---------------------|:--------|:---------------|:--------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -              | Hiển thị khi thêm mới thành công: **"Tạo tài khoản thành công. Mật khẩu mặc định đã được gửi về email."** |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Tên tài khoản đã tồn tại"** hoặc **"Tạo tài khoản thất bại"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                                                    |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------|
| Lưu thông tin | Button | Kiểm tra hợp lệ, ghi nhận dữ liệu vào **ENT_NguoiDung**, sinh mật khẩu mặc định theo rules chung và hiển thị thông báo thành công (**UC_User_Create**) |
| Đóng          | Button | Đóng form và quay về danh sách (**SCR_User_List.md**)                                                    |

</div>