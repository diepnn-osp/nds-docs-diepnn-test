# Màn hình: Xem lịch sử cập nhật thông tin giao dịch
Popup hiển thị lịch sử cập nhật của một giao dịch.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.  
- Người dùng có quyền xem lịch sử cập nhật thông tin giao dịch.  

## Nguyên mẫu
[]

## Thành phần

### Lịch sử
#### Thêm mới
<div style="overflow-x:auto">
| Trường thông tin | Control  | Field     | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                       |
|:-----------------|:---------|:----------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------------|
| Thời gian        | datetime | UpdatedAt | -          | -              | -                | -                  | Thời điểm thực hiện cập nhật                                |
| Người thực hiện  | text     | UpdatedBy | 100        | -              | -                | -                  | Người thực hiện thay đổi                                    |
| Thao tác         | text     | ThaoTac   | 200        | -              | -                | -                  | Thêm mới                                                    |
| Nội dung         | text     | -         | 500        | -              | -                | -                  | Thêm mới giao dịch thành công/Lưu nháp giao dịch thành công |

</div>

#### Cập nhật
<div style="overflow-x:auto">

| Trường thông tin   | Control  | Field                 | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
|:-------------------|:---------|:----------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------|
| Thời gian          | datetime | UpdatedAt             | -          | -              | -                | -                  | Thời điểm thực hiện cập nhật     |
| Người thực hiện    | text     | UpdatedBy             | 100        | -              | -                | -                  | Người thực hiện thay đổi         |
| Thao tác           | text     | ThaoTac               | 200        | -              | -                | -                  | Cập nhật                         |
| Thông tin thay đổi | text     | TruongThongTinCapNhat | 200        | -              | -                | -                  | Tên trường dữ liệu được thay đổi |
| Giá trị cũ         | text     | GiaTriCu              | 500        | -              | -                | -                  | Giá trị trước khi thay đổi       |
| Giá trị mới        | text     | GiaTriMoi             | 500        | -              | -                | -                  | Giá trị sau khi thay đổi         |

</div> 

### Chức năng

<div style="overflow-x:auto">

| Tên      | Loại   | Mô tả      |
|:---------|:-------|:-----------|
| Đóng     | Button | Đóng popup |
| Quay lại | Icon   | Đóng popup |

</div>


