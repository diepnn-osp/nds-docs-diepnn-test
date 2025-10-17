# Màn hình: Xem thông báo
- Form cho phép xem thông tin thông báo trên hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền Xem thông báo.

## Nguyên mẫu
[]

## Thành phần

### Form nội dung thông báo

<div style="overflow-x:auto">
 
| Trường thông tin | Control          | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                 |
| :--------------- | :--------------- | :----------- | :--------- | :------------- | :--------------- | :----------------- | :------------------------------------ |
| Tiêu đề          | Text             | TieuDe       | -          | -              | -                | -                  | Hiển thị tiêu đề của thông báo        |
| Loại thông báo   | Text             | LoaiThongBao | -          | -              | -                | -                  | Hiển thị loại thông báo               |
| Người gửi        | Text             | NguoiGui     | -          | -              | -                | -                  | Hiển thị tên người tạo thông báo      |
| Nội dung         | Rich Text Editor | NoiDung      | -          | -              | -                | -                  | Hiển thị nội dung thông báo           |
| File đính kèm    | Text             | TenFile      | -          | -              | -                | -                  | Hiển thị Tên file đính kèm (**BR5.**) |


### Chức năng

<div style="overflow-x:auto">

| Tên       | Loại   | Mô tả                                |
| --------- | :----- | :----------------------------------- |
| Tải xuống | Button | Cho phép Tải xuống file đính kèm     |
| Đóng      | Button | Hiển thị popup xác nhận hủy thao tác |
