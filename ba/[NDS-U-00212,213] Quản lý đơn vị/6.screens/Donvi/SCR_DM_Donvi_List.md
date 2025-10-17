# Màn hình: Danh sách danh mục đơn vị
Màn hình hiển thị danh sách danh mục đơn vị với các chức năng quản lý tương ứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem danh sách danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Bảng kết quả
<div style="overflow-x:auto">
Tiêu đề: Danh sách danh mục đơn vị

| Trường thông tin    | Control | Field | Mô tả                             |
| :------------------ | :------ | :---- | :-------------------------------- |
| STT                 | Label   | -     | Số thứ tự của bản ghi             |
| Mã danh mục         | Label   | -     | Mã danh mục đơn vị                |
| Tên đơn vị          | Label   | -     | Tên đơn vị                        |
| Loại đơn vị         | Label   | -     | Loại đơn vị (Bộ Tư Pháp, Sở Tư pháp, Tổ chức hành nghề công chứng, Đơn vị gửi thông tin ngăn chặn) |
| Số điện thoại       | Label   | -     | Số điện thoại                     |
| Email               | Label   | -     | Thông tin email                   |
| Địa chỉ             | Label   | -     | Địa chỉ (Tỉnh/Thành phố, Phường/Xã, Số nhà) |
| Trạng thái          | Label   | -     | Trạng thái (Hoạt động, Ngừng hoạt động) |

</div>

### Phân trang
<div style="overflow-x-auto">

| Thành phần | Control    | Bắt buộc (Y/N) | Mô tả                                                |
| :--------- | :--------- | :------------- | :--------------------------------------------------- |
| Phân trang | Pagination | -              | Hiển thị 10 bản ghi mỗi trang, cho phép chuyển trang |

</div>

### Tìm kiếm
<div style="overflow-x:auto">

| Thành phần | Control    | Field | Bắt buộc (Y/N) | Mô tả                                                      |
| :--------- | :--------- | :---- | :------------- | :--------------------------------------------------------- |
| Ô tìm kiếm | Text input | -     | N              | Cho phép người dùng nhập tiêu chí tìm kiếm danh mục đơn vị |

</div>

### Thông báo
<div style="overflow-x-auto">

| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                      |
| :------------------- | :------ | :------------- | :----------------------------------------- |
| Thông báo thành công | Label   | -              | Hiển thị khi thực hiện thao tác thành công |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi xảy ra:                |
- "Không có dữ liệu danh mục đơn vị"
- "Không tải được danh sách, vui lòng thử lại"
- "Không có quyền truy cập" |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên                    | Loại   | Mô tả                                                                    |
| :--------------------- | :----- | :----------------------------------------------------------------------- |
| Thêm mới               | Button | Mở form thêm mới danh mục đơn vị (**SCR_DM_Donvi_Create**)            |
| Xem chi tiết           | Button | Xem chi tiết thông tin danh mục đơn vị                                   |
| Sửa                    | Button | Mở form chỉnh sửa thông tin danh mục đơn vị (**SCR_DM_Donvi_Update**) |
| Xóa                    | Button | Mở popup xác nhận xóa danh mục đơn vị (**SCR_DM_Donvi_Delete**)       |
| Xem lịch sử            | Button | Xem lịch sử thay đổi của danh mục đơn vị                                 |
| Tải về file mẫu import | Button | Tải về file mẫu import (**SCR_DM_Donvi_Download_Temp**)               |
| Import dữ liệu đơn vị  | Button | Mở form import dữ liệu (**SCR_DM_Donvi_Import**)                      |
| Xuất danh sách đơn vị  | Button | Xuất danh sách đơn vị (**SCR_DM_Donvi_Export**)                       |

</div>
