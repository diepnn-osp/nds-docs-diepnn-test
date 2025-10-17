# Màn hình: Thêm mới thông tin danh mục đơn vị
Form cho phép Thêm mới thông tin danh mục đơn vị.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền Thêm mới thông tin danh mục đơn vị.

## Nguyên mẫu
[]

## Thành phần

### Form Thêm mới (DM_Donvi)
- Hiển thị form thêm mới
<div style="overflow-x:auto">
Tiêu đề: Thêm mới danh mục đơn vị

| Trường thông tin | Control | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                   |
|:-----------------|:--------|:-------------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------------------------------------------------------------------------------|
| Mã danh mục      | Text    | MaDM_Donvi   | -          | Y              | Tự sinh          | N                  | Mã danh mục tự sinh theo hệ thống                                                                       |
| Tên đơn vị       | Text    | TenDonVi     | 250        | Y              | -                | Y                  | Nhập tên đơn vị                                                                                         |
| Loại đơn vị      | Select  | LoaiDonVi    | -          | Y              | -                | Y                  | Chọn loại đơn vị (Bộ Tư Pháp, Sở Tư pháp, Tổ chức hành nghề công chứng, Đơn vị gửi thông tin ngăn chặn) |
| Đơn vị cha       | Select  | DonViChaId   | -          | N              | -                | Y                  | Chọn đơn vị cha (nếu có)                                                                                |
| Số điện thoại    | Text    | DienThoai    | 20         | N              | -                | Y                  | Nhập số điện thoại                                                                                      |
| Email            | Text    | Email        | 100        | N              | -                | Y                  | Nhập thông tin email                                                                                    |
| Fax              | Text    | Fax          | 20         | N              | -                | Y                  | Nhập thông tin số fax                                                                                   |
| Website          | Text    | WebSite      | 100        | N              | -                | Y                  | Nhập thông tin website                                                                                  |
| Tỉnh/Thành phố   | Select  | TinhThanh    | -          | N              | -                | Y                  | Chọn tỉnh/thành phố                                                                                     |
| Phường/Xã        | Text    | PhuongXa     | 100        | N              | -                | Y                  | Nhập địa chỉ phường/xã                                                                                  |
| Địa chỉ          | Text    | DiaChi       | 250        | N              | -                | Y                  | Nhập địa chỉ số nhà, tổ, thông, xóm                                                                     |
| Thông tin khác   | Text    | ThongTinKhac | 500        | N              | -                | Y                  | Nhập thông tin khác                                                                                     |
| Trạng thái       | Select  | TrangThai    | -          | Y              | Hoạt động        | Y                  | Chọn trạng thái (Hoạt động, Ngừng hoạt động)                                                            |

</div>

### Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                       |
|:--------------|:-------|:----------------------------------------------------------------------------|
| Lưu thông tin | Button | Kiểm tra hợp lệ, lưu dữ liệu vào **ENT_DM_Donvi** với trạng thái = "Active" |
| Đóng          | Button | Đóng form và quay về danh sách (**SCR_DM_Donvi_List**)                     |

</div>
