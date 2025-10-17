# Màn hình: Xem lịch sử cập nhật thông tin chữ ký số
Popup hiển thị danh sách lịch sử cập nhật của một hồ sơ đăng ký chữ ký số.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.  
- Người dùng có quyền xem lịch sử cập nhật thông tin chữ ký số.  

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=329-21660&t=qwdm1CHMm4I6o7Ud-1]

## Thành phần

### Lịch sử
#### Thêm mới
<div style="overflow-x:auto">
| Trường thông tin | Control  | Field     | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                 |
|:-----------------|:---------|:----------|:-----------|:---------------|:-----------------|:-------------------|:------------------------------------------------------|
| Thời gian        | datetime | updatedAt | -          | -              | -                | -                  | Thời điểm thực hiện cập nhật                          |
| Người thực hiện  | text     | updatedBy | 100        | -              | -                | -                  | Người thực hiện thay đổi                              |
| Thao tác         | text     | thaoTac   | 200        | -              | -                | -                  | Thêm mới                                              |
| Nội dung         | text     | -         | 500        | -              | -                | -                  | Trình duyệt/Lưu nháp thông tin đăng ký chữ ký số + ID |

</div>

#### Cập nhật
<div style="overflow-x:auto">

| Trường thông tin   | Control  | Field                 | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                            |
|:-------------------|:---------|:----------------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------|
| Thời gian          | datetime | updatedAt             | -          | -              | -                | -                  | Thời điểm thực hiện cập nhật     |
| Người thực hiện    | text     | updatedBy             | 100        | -              | -                | -                  | Người thực hiện thay đổi         |
| Thao tác           | text     | thaoTac               | 200        | -              | -                | -                  | Cập nhật                         |
| Thông tin thay đổi | text     | truongThongtinCapNhat | 200        | -              | -                | -                  | Tên trường dữ liệu được thay đổi |
| Giá trị cũ         | text     | giaTriCu              | 500        | -              | -                | -                  | Giá trị trước khi thay đổi       |
| Giá trị mới        | text     | giaTriMoi             | 500        | -              | -                | -                  | Giá trị sau khi thay đổi         |

</div>

### Thông báo hệ thống
- Không có dữ liệu: hiển thị **"Không tìm thấy lịch sử cập nhật thông tin chữ ký số"**.  
- Lỗi hệ thống: hiển thị **"Không tải được thông tin, vui lòng thử lại"**.  

### Chức năng

<div style="overflow-x:auto">

| Tên        | Loại   | Mô tả                                                   |
| :--------- | :----- | :------------------------------------------------------ |
| Đóng       | Button | Đóng popup, quay lại màn hình danh sách **SCR_Sign_List** |
| Quay lại   | Icon   | Chức năng tương tự nút Đóng                             |

</div>


