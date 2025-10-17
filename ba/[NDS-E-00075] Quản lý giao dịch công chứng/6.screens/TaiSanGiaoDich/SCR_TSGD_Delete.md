# Màn hình: Xác nhận xóa tài sản giao dịch
Popup xác nhận khi người dùng thực hiện thao tác xóa tài sản giao dịch từ màn hình

## Điều kiện tiên quyết
- Đã tạo tài sản giao dịch
- Người dùng đang ở form tạo lập/chỉnh sửa hồ sơ

## Nguyên mẫu
[]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần            | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                             |
|:----------------------|:--------|:------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------------------------------------------|
| Thông báo chính       | text    | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Bạn có chắc chắn muốn xóa tài sản này không?"**             |
| Thông báo phụ         | text    | -     | -          | -              | -                | -                  | Hiển thị nội dung: **"Hành động này không thể khôi phục"**                        |
| Nút Xác nhận          | button  | -     | -          | -              | -                | -                  | Khi bấm, hệ thống thực hiện kiểm tra ràng buộc trước khi xóa (**UC_TSGD_Delete**) |
| Nút Hủy               | button  | -     | -          | -              | -                | -                  | Khi bấm, đóng popup, không thực hiện xóa                                          |
| Biểu tượng đóng popup | button  | -     | -          | -              | -                | -                  | Khi bấm, đóng popup, không thực hiện xóa                                          |

</div>
