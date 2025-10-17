# Màn hình: Xác nhận xóa giao dịch công chứng
Popup xác nhận khi người dùng thực hiện thao tác xóa giao dịch công chứng từ màn hình danh sách.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xóa giao dịch công chứng.
- Giao dịch ở trạng thái lưu nháp.

## Nguyên mẫu
[]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần            | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                              |
|:----------------------|:--------|:------|:---------------|:-----------------------------------------------------------------------------------|
| Thông báo chính       | text    | -     | -              | Hiển thị nội dung: **“Bạn có chắc chắn muốn xóa giao dịch công chứng này không?”** |
| Thông báo phụ         | text    | -     | -              | Hiển thị nội dung: **“Hành động này không thể khôi phục”**                         |
| Nút Xác nhận          | button  | -     | -              | Khi bấm, hệ thống thực hiện kiểm tra ràng buộc trước khi xóa (**UC_GDCC_Delete**)  |
| Nút Hủy               | button  | -     | -              | Khi bấm, đóng popup, không thực hiện xóa                                           |
| Biểu tượng đóng popup | button  | -     | -              | Khi bấm, đóng popup, không thực hiện xóa                                           |

</div>
