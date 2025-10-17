# Màn hình: Popup Thông báo mới
- Hiển thị thông báo dạng pop-up ở góc dưới bên phải màn hình khi có thông báo mới phát sinh.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền nhận thông báo.
- Hệ thống có thông báo mới gửi đến người dùng.

## Nguyên mẫu
[]

## Thành phần

### Form nội dung popup thông báo mới

<div style="overflow-x:auto">
 
| Trường thông tin | Control | Field    | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                           |
| :--------------- | :------ | :------- | :--------- | :------------- | :--------------- | :----------------- | :---------------------------------------------- |
| Tiêu đề          | Text    | TieuDe   | -          | -              | Thông báo mới    | -                  | Hiển thị tiêu đề của thông báo                  |
| Nội dung         | Text    | NoiDung  | -          | -              | -                | -                  | Hiển thị tiêu đề và Tên người gửi của thông báo |
| Thời gian        | date    | ThoiGian | -          | -              | -                | -                  | Hiển thị thời gian nhận được thông báo          |

### Chức năng

<div style="overflow-x:auto">

| Tên          | Loại   | Mô tả                                                |
| ------------ | :----- | :--------------------------------------------------- |
| Xem chi tiết | Button | Mở form xem chi tiết thông báo (**SCR_Noti_Detail**) |
| Đóng         | Button | Đóng popup thông báo, đánh dấu thông báo là đã đọc   |