# Màn hình: Xác nhận xóa Thông tin đăng ký chữ ký số
Popup xác nhận khi người dùng thực hiện thao tác xóa Thông tin chữ ký số từ danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xóa Thông tin chữ ký số.
- Người dùng chỉ có thể xóa Thông tin chữ ký số thuộc tổ chức của mình.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=329-21860&t=qwdm1CHMm4I6o7Ud-1]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần      | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                     |
|:----------------|:--------|:------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------------------------------------------|
| Thông báo chính | label   | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Bạn có chắc chắn muốn xóa Thông tin chữ ký số này không?"** |
| Nút Xác nhận    | button  | -     | -          | -              | -                | -                  | Khi bấm, hệ thống kiểm tra ràng buộc trước khi xóa                                        |
| Nút Hủy         | button  | -     | -          | -              | -                | -                  | Khi bấm, đóng popup, không thực hiện xóa                                                  |

</div>
