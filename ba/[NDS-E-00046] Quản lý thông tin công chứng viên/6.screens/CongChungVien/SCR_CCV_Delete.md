# Màn hình: Xác nhận xóa công chứng viên
Popup xác nhận khi người dùng thực hiện thao tác xóa công chứng viên từ màn hình danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xóa công chứng viên.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=156-17661&t=AJ0R7XTWgx3u3lfZ-1]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần      | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                         |
|:----------------|:--------|:------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------------------------------|
| Thông báo chính | text    | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Bạn có chắc chắn muốn xóa công chứng viên này không?"** |
| Thông báo phụ   | text    | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Hành động này không thể khôi phục"**                    |
| Nút Xác nhận    | button  | -     | -          | -              | -                | -                  | Khi bấm, hệ thống thực hiện kiểm tra ràng buộc trước khi xóa                  |
| Nút Hủy         | button  | -     | -          | -              | -                | -                  | Khi bấm, đóng popup, không thực hiện xóa                                      |

</div>
