# Màn hình: Xác thực người dùng qua email
Popup yêu cầu người dùng xác thực tài khoản qua email khi quản trị hệ thống bật cấu hình xác thực.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Quản trị hệ thống đã bật cấu hình yêu cầu xác thực người dùng.
- Người dùng chưa thực hiện xác thực email.

## Nguyên mẫu
[]

## Thành phần

### Popup xác thực email
<div style="overflow-x:auto">
Tiêu đề: Xác thực tài khoản qua email

| Trường thông tin | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định              | Mô tả                                                                                       |
|:-----------------|:--------|:------|:-----------|:---------------|:------------------------------|:--------------------------------------------------------------------------------------------|
| Email            | Text    | Email | 100        | Y              | Email của người dùng (nếu có) | Nhập email để nhận mã xác thực. Nếu người dùng đã có email trong hệ thống, sẽ tự động điền. |

</div>

### Popup nhập mã OTP
<div style="overflow-x:auto">
Tiêu đề: Nhập mã xác thực

| Trường thông tin | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Mô tả                                                    |
|:-----------------|:--------|:------|:-----------|:---------------|:-----------------|:---------------------------------------------------------|
| OTP 1            | Text    | OTP1  | 1          | Y              | -                | Ô nhập chữ số đầu tiên của mã OTP. Chỉ cho phép nhập số. |
| OTP 2            | Text    | OTP2  | 1          | Y              | -                | Ô nhập chữ số thứ hai của mã OTP. Chỉ cho phép nhập số.  |
| OTP 3            | Text    | OTP3  | 1          | Y              | -                | Ô nhập chữ số thứ ba của mã OTP. Chỉ cho phép nhập số.   |
| OTP 4            | Text    | OTP4  | 1          | Y              | -                | Ô nhập chữ số thứ tư của mã OTP. Chỉ cho phép nhập số.   |
| OTP 5            | Text    | OTP5  | 1          | Y              | -                | Ô nhập chữ số thứ năm của mã OTP. Chỉ cho phép nhập số.  |
| OTP 6            | Text    | OTP6  | 1          | Y              | -                | Ô nhập chữ số thứ sáu của mã OTP. Chỉ cho phép nhập số.  |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần                       | Control | Bắt buộc (Y/N) | Mô tả                                                                                                                                                                               |
|:---------------------------------|:--------|:---------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Thông báo thành công             | Label   | -              | Hiển thị khi xác thực thành công: **"Xác thực thành công"**                                                                                                                         |
| Thông báo lỗi                    | Label   | -              | Hiển thị khi có lỗi: **"Mã OTP không đúng hoặc đã hết hạn"**, **"Vui lòng nhập email"**, **"Email không hợp lệ"** hoặc **"Bạn đã xác thực sai quá 5 lần. Vui lòng đăng nhập lại."** |
| Thông báo yêu cầu cập nhật email | Label   | -              | Hiển thị khi người dùng chưa có email: **"Bạn chưa có email trong hệ thống. Vui lòng cập nhật email để xác thực tài khoản."**                                                       |
| Thông báo đã gửi mã              | Label   | -              | Hiển thị sau khi gửi mã OTP: **"Mã xác thực đã được gửi đến email [email]"**                                                                                                        |
| Thông báo đếm ngược              | Label   | -              | Hiển thị đếm ngược thời gian còn lại để gửi lại OTP: **"Gửi lại mã sau [XX:XX]"**                                                                                                   |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên              | Loại   | Trạng thái                                         | Mô tả                                                                                                      |
|:-----------------|:-------|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| Xác thực (Email) | Button | Disable cho đến khi nhập đúng định dạng email      | Gửi mã OTP đến email người dùng và chuyển sang màn hình nhập mã OTP                                        |
| Xác thực (OTP)   | Button | Disable cho đến khi nhập đủ 6 số                   | Xác nhận mã OTP và hoàn tất quá trình xác thực tài khoản                                                   |
| Gửi lại mã       | Button | Disable cho đến khi hết thời gian đếm ngược 5 phút | Gửi lại mã OTP mới về email người dùng. Nút này sẽ ở trạng thái không khả dụng trong 5 phút sau khi gửi mã |
| Hủy              | Button | Luôn enable                                        | Hiển thị thông báo "Bạn phải xác thực tài khoản để tiếp tục sử dụng hệ thống" (không cho phép đóng popup)  |

</div>

## Ghi chú
- Popup xác thực không thể đóng cho đến khi người dùng xác thực thành công.
- Nếu người dùng chưa có email, phải cập nhật email trước khi có thể xác thực.
- Mã OTP gồm 6 chữ số và chỉ có hiệu lực trong 5 phút kể từ khi gửi.
- Form nhập mã OTP có 6 ô riêng biệt, mỗi ô chỉ cho phép nhập 1 số. Tự động chuyển focus sang ô tiếp theo sau khi nhập.
- Nút "Xác thực (Email)" chỉ được kích hoạt khi người dùng nhập đúng định dạng email (kiểm tra regex email).
- Nút "Xác thực (OTP)" chỉ được kích hoạt khi người dùng nhập đủ 6 số vào các ô OTP.
- Nút "Gửi lại mã" sẽ ở trạng thái không khả dụng trong 5 phút sau khi gửi mã, sau đó sẽ kích hoạt lại.
- Giới hạn số lần gửi lại mã OTP (tối đa 3 lần trong 15 phút).
- Nếu người dùng xác thực OTP sai quá 5 lần, hệ thống sẽ tự động đăng xuất tài khoản và yêu cầu đăng nhập lại.
- Hệ thống sẽ hiển thị thông báo "Bạn đã xác thực sai quá 5 lần. Vui lòng đăng nhập lại." trước khi đăng xuất.
- Sau khi xác thực thành công, popup sẽ tự động đóng và người dùng có thể truy cập các tính năng của hệ thống.