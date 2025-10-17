# Màn hình: Thêm mới tổ chức công chứng
Form cho phép thêm mới thông tin một tổ chức hành nghề công chứng.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền thêm mới tổ chức công chứng.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=208-26693&t=VeTqJhXDfKkDczGX-1]

## Thành phần

### Form nhập liệu

<div style="overflow-x:auto">

| Trường thông tin       | Control         | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                                                                                                           |
|:-----------------------|:----------------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tên tổ chức công chứng | text            | tenDonVi         | 250        | Y              |                  | Y                  |                                                                                                                                                                                                                 |
| Sở Tư pháp quản lý     | int             | thuocDonVi       | 250        | Y              |                  | N                  | Tự động chọn Sở Tư pháp giống với người dùng. Disable, không cho phép thay đổi                                                                                                                                  |
| Địa chỉ                | text            | diaChiChiTiet    | 500        | Y              |                  | Y                  | Placeholder: Nhập địa chỉ số nhà, tổ, thôn, xóm                                                                                                                                                                 |
| Tỉnh/Thành phố         | combobox search | diaChiTinhThanh  | 250        | Y              |                  | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7**                                                                                                                                                                  |
| Phường/Xã              | combobox search | diaChiPhuongXa   | 250        | Y              |                  | Y                  | Chọn từ danh mục phường xã mới **BR9.8**,                                                                                                                                                                       |
| Số điện thoại          | text            | dienThoai        | 10         | N              |                  | Y                  | **BR9.1**,**BR9.4**                                                                                                                                                                                             |
| Email                  | text            | email            | 255        | N              |                  | Y                  | **BR9.9**                                                                                                                                                                                                       |
| Mã số thuế             | text            | maSoThue         | 250        | N              |                  | Y                  |                                                                                                                                                                                                                 |
| Trưởng văn phòng       | combobox search | truongVanPhongId | 50         | Y              |                  | Y                  | Click vào cho phép chọn công chứng viên từ danh sách (entity CongChungVien), cho phép điền và tìm kiếm theo số giấy tờ/tên công chứng viên, danh sách hiển thị theo cấu trúc "Số giấy tờ - Tên công chứng viên" |
| Trạng thái hoạt động   | combobox search | trangThai        | 50         | Y              | Đang hoạt động   | Y                  | Chọn trạng thái hoạt động theo danh sách đã liệt kê trong entity                                                                                                                                                |

</div>

### Chức năng
<div style="overflow-x:auto">

| Tên | Loại   | Mô tả                                                                                                    |
|:----|:-------|:---------------------------------------------------------------------------------------------------------|
| Lưu | Button | Lưu dữ liệu nhập vào. Nếu hợp lệ thì cập nhật dữ liệu và đóng màn hình. Chi tiết trong **UC_Org_Create** |
| Hủy | Button | Hiển thị popup xác nhận hủy thao tác                                                                     |
