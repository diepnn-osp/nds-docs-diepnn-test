# Màn hình: Danh sách tài khoản người dùng
Màn hình hiển thị danh sách tài khoản người dùng với các chức năng quản lý tương ứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem danh sách tài khoản người dùng.

## Nguyên mẫu
[]

## Thành phần

### Bảng kết quả
<div style="overflow-x:auto">
Tiêu đề: Danh sách tài khoản người dùng

| Trường thông tin | Control | Field | Mô tả                                 |
|:-----------------|:--------|:------|:--------------------------------------|
| STT              | Label   | -     | Số thứ tự của bản ghi                 |
| Tên tài khoản    | Label   | -     | Tên đăng nhập của tài khoản           |
| Họ và tên        | Label   | -     | Họ và tên đầy đủ của người dùng       |
| Email            | Label   | -     | Email của người dùng                  |
| Vai trò          | Label   | -     | Vai trò của người dùng trong hệ thống |
| Đơn vị           | Label   | -     | Đơn vị công tác của người dùng        |
| Trạng thái       | Label   | -     | Trạng thái hoạt động của tài khoản    |

</div>

### Phân trang
<div style="overflow-x:auto">

| Thành phần | Control | Bắt buộc (Y/N) | Mô tả |
|:----------|:--------|:---------------|:------|
| Phân trang | Pagination | - | Hiển thị 10 bản ghi mỗi trang, cho phép chuyển trang |

</div>

### Tìm kiếm
<div style="overflow-x:auto">

| Thành phần | Control | Field | Bắt buộc (Y/N) | Mô tả |
|:----------|:--------|:------|:---------------|:------|
| Ô tìm kiếm | Text input | - | N | Cho phép người dùng nhập tiêu chí tìm kiếm tài khoản người dùng |

</div>

### Thông báo
<div style="overflow-x:auto">

| Thành phần | Control | Bắt buộc (Y/N) | Mô tả |
|:----------|:--------|:---------------|:------|
| Thông báo thành công | Label | - | Hiển thị khi thực hiện thao tác thành công |
| Thông báo lỗi | Label | - | Hiển thị khi có lỗi xảy ra:
- "Không có dữ liệu tài khoản người dùng"
- "Không tải được danh sách, vui lòng thử lại"
- "Không có quyền truy cập" |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                 |
|:-------------|:-------|:--------------------------------------------------------------------------------------|
| Thêm mới     | Button | Mở form thêm mới tài khoản người dùng (**SCR_User_Create.md**) (**UC_User_Create**)   |
| Xem chi tiết | Button | Xem chi tiết thông tin tài khoản người dùng (**SCR_User_View.md**) (**UC_User_View**) |
| Sửa | Button | Mở form chỉnh sửa thông tin tài khoản người dùng (**SCR_User_Update.md**) (**UC_User_Update**) |
| Xóa | Button | Mở popup xác nhận xóa tài khoản người dùng (**SCR_User_Delete.md**) (**UC_User_Delete**) |
| Đổi mật khẩu | Button | Mở form đổi mật khẩu tài khoản người dùng (**SCR_User_ChangePass.md**) (**UC_User_ChangePass**) |
| Gán vai trò | Button | Mở form gán vai trò cho tài khoản người dùng (**SCR_User_Assign.md**) (**UC_User_Assign**) |
| Xóa vai trò | Button | Mở form xóa vai trò khỏi tài khoản người dùng (**SCR_User_Remove.md**) (**UC_User_Remove**) |
| Xem vai trò | Button | Xem vai trò của tài khoản người dùng (**SCR_User_View.md**) (**UC_User_View**) |

</div>