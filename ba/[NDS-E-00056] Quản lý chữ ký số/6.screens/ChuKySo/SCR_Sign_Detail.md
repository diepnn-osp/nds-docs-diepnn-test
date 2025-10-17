# Màn hình: Chi tiết thông tin  chữ ký số
Màn hình hiển thị chi tiết chữ ký số, trạng thái phê duyệt và thông tin liên quan.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xem chi tiết thông tin chữ ký số.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=329-22099&t=qwdm1CHMm4I6o7Ud-1]

## Thành phần

### Thông tin chi tiết (ENT_ChuKySo)

<div style="overflow-x:auto">

| Trường thông tin | Control   | Field         | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                            |
|:-----------------|:----------|:--------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------------------------|
| Công chứng viên  | text      | hodem + ten   | 250        | -              | -                | N                  | Tên công chứng viên nếu là loại chữ ký số cá nhân                |
| Loại chữ ký số   | text      | loaiChuKySo   | 100        | -              | -                | N                  | Thông tin loại chữ ký số                                         |
| Nhà cung cấp     | text      | nhaCungCap    | 200        | -              | -                | N                  | Nhà cung cấp chứng thư số                                        |
| Số serial        | text      | soSerial      | 100        | -              | -                | N                  | Mã định danh chứng thư số                                        |
| Ngày hiệu lực    | date      | ngayHieuLuc   | -          | -              | -                | N                  | Ngày bắt đầu hiệu lực                                            |
| Ngày hết hạn     | date      | ngayHetHan    | -          | -              | -                | N                  | Ngày hết hạn. Nếu quá hạn, hiển thị thông báo "Hết hạn" bên cạnh |
| File đính kèm    | file/link | fileDinhKem   | -          | -              | -                | N                  | File đính kèm                                                    |
| Ghi chú          | text      | ghiChu        | 500        | -              | -                | N                  | Ghi chú                                                          |
| Trạng thái       | text      | trangThai     | 50         | -              | -                | N                  | Mới tạo / Chờ duyệt / Đã duyệt / Từ chối                         |
| Người duyệt      | text      | nguoiDuyet    | 250        | -              | -                | N                  | Tên người phê duyệt                                              |
| Thời gian duyệt  | datetime  | thoiGianDuyet | -          | -              | -                | N                  | Thời gian phê duyệt                                              |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên         | Loại   | Mô tả                                                                                                                          |
|:------------|:-------|:-------------------------------------------------------------------------------------------------------------------------------|
| Đóng        | Button | Đóng màn hình, quay lại màn hình danh sách (**SCR_Sign_List**)                                                                     |
| Duyệt       | Button | Chỉ hiển thị nếu người dùng có quyền phê duyệt và trạng thái khác "Đã duyệt" và "Từ chối"                               |
| Từ chối     | Button | Chỉ hiển thị nếu người dùng có quyền phê duyệt và trạng thái khác "Đã duyệt" và "Từ chối"                                |
| Chỉnh sửa   | Button | Chỉ hiển thị nếu người dùng có quyền chỉnh sửa → mở màn hình chỉnh sửa, Chỉ hiển thị khi trạng thái là "Mới tạo" hoặc "Chờ duyệt" |
| Trình duyệt | Button | Chỉ hiển thị nếu người dùng có quyền chỉnh sửa và trạng thái là "Mới tạo" → Cập nhật trạng thái = "Chờ duyệt" và lưu lịch sử   |

</div>

