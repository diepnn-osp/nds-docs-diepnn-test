# Màn hình: Lịch sử cập nhật tổ chức công chứng
Popup hiển thị lịch sử cập nhật thông tin tổ chức công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem lịch sử cập nhật tổ chức công chứng.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=208-26816&t=VeTqJhXDfKkDczGX-1]

## Thành phần

### Lịch sử

#### Thêm mới
<div style="overflow-x:auto">

| Trường thông tin | Control  | Field     | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                           |
|:-----------------|:---------|:----------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------|
| Thời gian        | datetime | updatedAt | -              | Thời điểm thực hiện cập nhật    |
| Người thực hiện  | text     | updatedBy | -              | Người thực hiện thay đổi        |
| Thao tác         | text     | thaoTac   | -              | Thêm mới                        |
| Nội dung         | text     | -         | -              | Tạo mới tổ chức công chứng + ID |

</div>

#### Cập nhật
<div style="overflow-x:auto">

| Trường thông tin   | Control  | Field                 | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
|:-------------------|:---------|:----------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------|
| Thời gian          | datetime | updatedAt             | -              | Thời điểm thực hiện cập nhật     |
| Người thực hiện    | text     | updatedBy             | -              | Người thực hiện thay đổi         |
| Thao tác           | text     | thaoTac               | -              | Cập nhật                         |
| Thông tin thay đổi | text     | truongThongtinCapNhat | -              | Tên trường dữ liệu được thay đổi |
| Giá trị cũ         | text     | giaTriCu              | -              | Giá trị trước khi thay đổi       |
| Giá trị mới        | text     | giaTriMoi             | -              | Giá trị sau khi thay đổi         |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên             | Loại   | Mô tả      |
|:----------------|:-------|:-----------|
| Quay lại / Đóng | Button | Đóng popup |

</div>

