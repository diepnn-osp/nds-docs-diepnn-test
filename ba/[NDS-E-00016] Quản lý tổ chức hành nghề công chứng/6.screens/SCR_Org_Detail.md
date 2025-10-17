# Màn hình: Chi tiết tổ chức công chứng
Màn hình hiển thị chi tiết thông tin của một tổ chức hành nghề công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xem thông tin chi tiết tổ chức công chứng.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=208-26757&t=VeTqJhXDfKkDczGX-1]

## Thành phần

### Form hiển thị thông tin

<div style="overflow-x:auto">

| Trường thông tin       | Control  | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                   |
|:-----------------------|:---------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------------------------------------------------|
| Tên tổ chức công chứng | text     | tenDonVi        | -          | -              |                  | N                  | Tên của tổ chức hành nghề công chứng                                                    |
| Sở Tư pháp quản lý     | text     | tenDonVi        | -          | -              |                  | N                  | Tên Sở Tư pháp quản lý                                                                  |
| Địa chỉ                | text     | diaChiChiTiet   | -          | -              |                  | N                  | Địa chỉ trụ sở chính                                                                    |
| Tỉnh/Thành phố         | text     | diaChiTinhThanh | -          | -              |                  | N                  | Tỉnh/Thành phố nơi tổ chức công chứng hoạt động                                         |
| Phường/Xã              | text     | diaChiPhuongXa  | -          | -              |                  | N                  | Phường/Xã thuộc địa chỉ tổ chức                                                         |
| Số điện thoại          | text     | dienThoai       | -          | -              |                  | N                  | Thông tin số điện thoại liên hệ                                                         |
| Email                  | text     | email           | -          | -              |                  | N                  | Email liên hệ                                                                           |
| Mã số thuế             | text     | maSoThue        | -          | -              |                  | N                  | Mã số thuế                                                                              |
| Trưởng văn phòng       | text     | hoDem + ten     | -          | -              |                  | N                  | Hiển thị tên công chứng viên trưởng VP (tìm từ ENT_CongChungVien theo truongVanPhongId) |
| Trạng thái hoạt động   | dropdown | trangThai       | -          | -              | -                | N                  | Trạng thái: Đang hoạt động, Chờ thành lập, Giải thể, …                                  |


</div>

### Danh sách công chứng viên thuộc tổ chức
<div style="overflow-x:auto">

| Trường thông tin | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                         |
|:-----------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------|
| STT              | text    | -                | -          | -              |                  | -                  | Số thứ tự bản ghi                             |
| Họ và tên        | text    | hoDem + ten      | -          | -              |                  | N                  | Hiển thị tên công chứng viên                  |
| Số giấy tờ       | text    | soGiayTo         | -          | -              |                  | N                  | Hiển thị số giấy tờ                           |
| Số thẻ           | text    | soThe            | -          | -              | -                | N                  | Số thẻ của công chứng viên                    |
| Chức vụ          | text    | truongVanPhongId | -          | -              | -                | N                  | Hiển thị "Công chứng viên"/"Trưởng văn phòng" |
| Trạng thái       | text    | trangThai        | -          | -              | -                | N                  | Trạng thái hoạt động của công chứng viên      |
</div>

### Chức năng
<div style="overflow-x:auto">

| Tên       | Loại   | Mô tả                                                                                       |
|:----------|:-------|:--------------------------------------------------------------------------------------------|
| Đóng      | Button | Đóng màn hình chi tiết, về trang danh sách                                                                         |
| Chỉnh sửa | Button | Mở form chỉnh sửa tổ chức công chứng (SCR_Org_Update), chỉ hiển thị khi người dùng có quyền |

</div>
