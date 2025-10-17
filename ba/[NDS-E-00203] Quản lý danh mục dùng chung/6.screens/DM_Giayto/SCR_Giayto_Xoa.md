# Màn hình: Xác nhận xóa thông tin giấy tờ
Popup xác nhận khi người dùng thực hiện thao tác xóa thông tin giấy tờ .

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xóa thông tin giấy tờ.
- Người dùng chỉ có thể xóa thông tin giấy tờ khi danh mục đang không được sử dụng.

## Nguyên mẫu
[]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">

| Thành phần      | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                                      |
|:----------------|:--------|:------|:---------------|:-------------------------------------------------------------------------------------------|
| Thông báo chính | label   | -     | -              | Hiển thị nội dung: **“Bạn có chắc chắn muốn xóa Thông tin danh mục giấy tờ không?”**       |
| Nút Xác nhận    | button  | -     | -              | Khi bấm, hệ thống kiểm tra ràng buộc trước khi xóa                                         |
| Nút Hủy         | button  | -     | -              | Khi bấm, đóng popup, không thực hiện xóa                                                   |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên        | Loại   | Mô tả                                                                                |
| :--------- | :----- | :----------------------------------------------------------------------------------- |
| Xác nhận   | Button | Thực hiện kiểm tra điều kiện xóa và xóa thông tin danh mục giấy tờ nếu hợp lệ        |
| Hủy        | Button | Đóng popup, không thực hiện thay đổi dữ liệu                                         |

</div>
