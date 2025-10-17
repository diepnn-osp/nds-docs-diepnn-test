# Màn hình: Tìm kiếm danh mục đơn vị
Màn hình cho phép tìm kiếm thông tin danh mục đơn vị.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền truy cập chức năng.
- Người dùng đang ở màn hình danh sách danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm
- Hiển thị trên màn hình danh sách danh mục đơn vị
<div style="overflow-x:auto">

| Trường thông tin | Control    | Field | Bắt buộc (Y/N) | Mô tả                                  |
| :--------------- | :--------- | :---- | :------------- | :------------------------------------- |
| Từ khóa tìm kiếm | Text input | -     | N              | Nhập tiêu chí tìm kiếm danh mục đơn vị |
| Loại đơn vị      | Select     | -     | N              | Chọn loại đơn vị để tìm kiếm           |
| Trạng thái       | Select     | -     | N              | Chọn trạng thái để tìm kiếm            |

</div>

### Bảng kết quả tìm kiếm
<div style="overflow-x-auto">

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

### Thông báo
<div style="overflow-x:auto">

| Thành phần               | Control | Bắt buộc (Y/N) | Mô tả                                                                        |
| :----------------------- | :------ | :------------- | :--------------------------------------------------------------------------- |
| Thông báo không tìm thấy | Label   | -              | Hiển thị khi không có kết quả tìm kiếm: **"Không tìm thấy kết quả phù hợp"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                                                                          |
| :----------- | :----- | :------------------------------------------------------------------------------------------------------------- |
| Tìm kiếm     | Button | Kiểm tra dữ liệu tìm kiếm và hiển thị kết quả phù hợp                                                          |
| Xem chi tiết | Button | Xem chi tiết thông tin danh mục đơn vị (trên kết quả tìm kiếm)                                                 |
| Sửa          | Button | Mở form chỉnh sửa thông tin danh mục đơn vị (**SCR_DM_Donvi_Update**) (trên kết quả tìm kiếm, nếu có quyền) |
| Xóa          | Button | Mở popup xác nhận xóa danh mục đơn vị (**SCR_DM_Donvi_Delete**) (trên kết quả tìm kiếm, nếu có quyền)       |

</div>
