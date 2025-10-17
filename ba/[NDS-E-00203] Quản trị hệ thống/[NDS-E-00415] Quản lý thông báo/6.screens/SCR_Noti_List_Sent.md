# Màn hình: Danh sách thông báo GỬI
- Cho phép hiển thị danh sách Thông báo theo thứ tự mới tạo lên đầu tiên
- Cho phép tìm kiếm Thông báo, thao tác (Xem chi tiết, Chỉnh sửa, Xóa, Tạo mới)

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem danh sách thông báo.

## Nguyên mẫu
[]

## Thành phần

### Form tìm kiếm 
<div style="overflow-x:auto">
- Ô tìm kiếm luôn hiển thị trên top trang
Tiêu đề: Tìm kiếm
| Trường thông tin | Control | Field    | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                    |
| :--------------- | :------ | :------- | :--------- | :------------- | :--------------- | :----------------- | :--------------------------------------- |
| Tiêu đề          | Text    | TieuDe   | 250        | -              | -                | Y                  | Nhập từ khoá tìm kiếm theo Tiêu đề       |
| Người gửi        | Text    | NguoiGui | -          | -              | -                | Y                  | Nhập từ khoá tìm kiếm theo Tên người gửi |

### Form tìm kiếm nâng cao
<div style="overflow-x:auto">
| Trường thông tin | Control  | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                               |
| :--------------- | :------- | :----------- | :--------- | :------------- | :--------------- | :----------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| Loại Thông báo   | Combobox | LoaiThongBao | -          | -              | -                | Y                  | Chọn loại thông báo                                                                                                                 |
| Thời gian gửi    | date     | NgayGui      | -          | -              | -                | Y                  | Cho phép chọn Khoảng thời gian Từ ngày - Đến ngày, kết quả hiển thị Danh sách thông báo có ngày gửi trong khoảng Từ ngày - Đến ngày |
| Trạng thái       | Combobox | TrangThai    | -          | -              | -                | Y                  | Chọn trạng thái thông báo (Chưa gửi/ Đã gửi)                                                                                        |

### Danh sách thông báo
<div style="overflow-x:auto">
Tiêu đề: Danh sách thông báo
| Trường thông tin | Control  | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
| :--------------- | :------- | :----------- | :--------- | :------------- | :--------------- | :----------------- | :------------------------------- |
| Tiêu đề          | Text     | TieuDe       | -          | -              | -                | -                  | Hiển thị tiêu đề thông báo       |
| Người gửi        | Text     | NguoiGui     | -          | -              | -                | -                  | Hiển thị Tên người gửi           |
| Loại Thông báo   | Combobox | LoaiThongBao | -          | -              | -                | -                  | Hiển thị thông báo              |
| Thời gian gửi    | date     | NgayGui      | -          | -              | -                | -                  | Hiển thị thời gian gửi thông báo |
| Trạng thái       | Text     | TrangThai    | -          | -              | -                | -                  | Hiển thị trạng thái thông báo    |

### Chức năng

<div style="overflow-x:auto">

| Tên                    | Loại   | Mô tả                                                                                 |
| :--------------------- | :----- | :------------------------------------------------------------------------------------ |
| Tìm kiếm               | Button | Kiểm tra hợp lệ và hiển thị danh sách thông báo bên liên quan theo điều kiện tìm kiếm |
| Xoá điều kiện tìm kiếm | Button | Reset màn hình danh sách                                                              |
| Thêm mới               | Button | Mở form thêm mới thông báo (SCR_Noti_Create)                                          |
| Xem chi tiết           | Button | Mở form thêm xem chi tiết (SCR_Noti_Detail)                                           |
| Sửa                    | Button | Mở form Sửa thông báo (SCR_Noti_Update)                                               |
| Xóa                    | Button | Hiển thị popup xác nhận xóa (SRC_Noti_Delete)                                         |


