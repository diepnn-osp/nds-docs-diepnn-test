# Màn hình: Cập nhật thông báo
- Form cho phép nhập và lưu thông tin thông báo mới vào hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền Cập nhật thông báo.

## Nguyên mẫu
[]

## Thành phần

### Form nội dung thông báo

<div style="overflow-x:auto">
 
| Trường thông tin | Control          | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                            |
| :--------------- | :--------------- | :----------- | :--------- | :------------- | :--------------- | :----------------- | :------------------------------------------------------------------------------- |
| Tiêu đề          | Text             | TieuDe       | 250        | Y              | -                | Y                  | Nhập tiêu đề thông báo, hiển thị trong danh sách và chi tiết                     |
| Loại thông báo   | Combobox         | LoaiThongBao | -          | Y              | -                | Y                  | Chọn Loại thông báo Thông báo nội bộ, Thông báo gửi STP, Thông báo gửi TCHNCCbáo |
| Người gửi        | Text             | NguoiGui     | -          | -              | -                | N                  | Hiển thị tên người tạo thông báo                                                 |
| Nội dung         | Rich Text Editor | NoiDung      | 2000       | Y              | -                | Y                  | Nhập nội dung thông báo                                                          |
| File đính kèm    | Text             | TenFile      | -          | N              | -                | -                  | Hiển thị Tên file đính kèm (**BR5.**)                                            |

### Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                    |
| ------------- | :----- | :----------------------------------------------------------------------- |
| Tải file      | Button | Cho phép Tải lên file đính kèm                                           |
| Tải xuống     | Button | Cho phép Tải xuống file đính kèm                                         |
| Xoá file      | Button | Cho phép Xoá file đính kèm                                               |
| Lưu nháp      | Button | Kiểm tra hợp lệ, lưu dữ liệu vào **ENT_Thongbao**, trạng thái = Chưa gửi |
| Gửi thông báo | Button | Kiểm tra hợp lệ, lưu dữ liệu vào **ENT_Thongbao**, trạng thái = Đã gửi   |
| Đóng          | Button | Hiển thị popup xác nhận hủy thao tác                                     |
