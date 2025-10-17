# Màn hình: Import dữ liệu danh mục đơn vị
Màn hình cho phép người dùng import dữ liệu danh mục đơn vị từ file.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền quản lý danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Nút import dữ liệu
- Hiển thị trên màn hình danh sách danh mục đơn vị

### Form Import dữ liệu
- Hiển thị khi người dùng chọn thao tác "Import dữ liệu"
<div style="overflow-x:auto">
Tiêu đề: Import dữ liệu danh mục đơn vị

| Thành phần  | Control    | Field | Bắt buộc (Y/N) | Mô tả                                            |
|:------------|:-----------|:------|:---------------|:-------------------------------------------------|
| File import | File input | -     | Y              | Cho phép người dùng chọn file import từ thiết bị |
| Nút Import  | Button     | -     | -              | Nút "Import dữ liệu" để bắt đầu quá trình import |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Field | Bắt buộc (Y/N) | Mô tả                                                                                                            |
|:---------------------|:--------|:------|:---------------|:-----------------------------------------------------------------------------------------------------------------|
| Thông báo thành công | Label   | -     | -              | Hiển thị khi import thành công: **"Import dữ liệu thành công"**                                                  |
| Thông báo thất bại   | Label   | -     | -              | Hiển thị khi import thất bại: **"Import dữ liệu thất bại"**                                                       |
| Tải file lỗi         | Link    | -     | -              | Hiển thị khi import thất bại, cho phép người dùng tải về file ghi chú từng bản ghi bị lỗi để xem chi tiết và xử lý |

</div>


## Chức năng

<div style="overflow-x:auto">

| Tên            | Loại   | Mô tả                                                                                                              |
|:---------------|:-------|:-------------------------------------------------------------------------------------------------------------------|
| Import dữ liệu | Button | Kiểm tra định dạng file, đọc và kiểm tra dữ liệu, tự động import dữ liệu hợp lệ vào hệ thống mà không cần xác nhận |
| Tải file lỗi   | Link   | Khi import thất bại, cho phép người dùng tải về file ghi chú từng bản ghi bị lỗi để xem chi tiết và xử lý          |

</div>
