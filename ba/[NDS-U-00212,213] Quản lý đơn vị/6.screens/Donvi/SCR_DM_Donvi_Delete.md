# Màn hình: Xác nhận xóa thông tin danh mục đơn vị
Popup xác nhận khi người dùng thực hiện thao tác xóa thông tin danh mục đơn vị.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xóa thông tin danh mục đơn vị.
- Người dùng chỉ có thể xóa thông tin danh mục đơn vị khi danh mục đang không được sử dụng trong các tính năng nghiệp vụ.

## Nguyên mẫu
[]

## Thành phần

### Popup xác nhận

<div style="overflow-x:auto">
Tiêu đề: Xác nhận xóa danh mục
| Thành phần      | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                                 |
|:----------------|:--------|:------|:---------------|:--------------------------------------------------------------------------------------|
| Thông báo chính | label   | -     | -              | Hiển thị nội dung: **"Bạn có chắc chắn muốn xóa Thông tin danh mục đơn vị không?"**   |
| Nút Xác nhận    | button  | -     | -              | Khi bấm, hệ thống kiểm tra điều kiện xóa (danh mục chưa được sử dụng) trước khi xóa   |
| Nút Hủy         | button  | -     | -              | Khi bấm, đóng popup, không thực hiện xóa và quay về danh sách (**SCR_DM_Donvi_List**) |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                                      |
|:---------------------|:--------|:------|:---------------|:-------------------------------------------------------------------------------------------|
| Thông báo thành công | label   | -     | -              | Hiển thị khi xóa thành công: **"Xóa danh mục thành công"**                                 |
| Thông báo lỗi        | label   | -     | -              | Hiển thị khi có lỗi: **"Danh mục đã được sử dụng, không thể xóa"** hoặc **"Lỗi hệ thống"** |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên      | Loại   | Mô tả                                                                                     |
|:---------|:-------|:------------------------------------------------------------------------------------------|
| Xác nhận | Button | Thực hiện kiểm tra điều kiện xóa và xóa thông tin danh mục đơn vị nếu điều kiện hợp lệ    |
| Hủy      | Button | Đóng popup, không thực hiện thay đổi dữ liệu và quay về danh sách (**SCR_DM_Donvi_List**) |

</div>
