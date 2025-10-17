# Màn hình: Xác nhận xóa người tham gia giao dịch
Popup xác nhận khi người dùng thực hiện thao tác xóa người tham gia giao dịch từ danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền thêm mới/chỉnh sửa giao dịch công chứng.
- Người dùng đang ở trong màn hình thêm mới/chỉnh sửa giao dịch công chứng.

## Nguyên mẫu
[]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần      | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                  |
|:----------------|:--------|:------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------------------------------------------------------------|
| Thông báo chính | label   | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Bạn có chắc chắn muốn xóa người tham gia giao dịch này không?"** |
| Nút Xác nhận    | button  | -     | -          | -              | -                | -                  | Khi bấm, xóa người tham gia giao dịch khỏi danh sách                                   |
| Nút Hủy         | button  | -     | -          | -              | -                | -                  | Khi bấm, đóng popup, không thực hiện xóa                                               |

</div>
