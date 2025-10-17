# Màn hình: Chỉnh sửa thông tin danh mục đơn vị
Form cho phép chỉnh sửa thông tin danh mục đơn vị.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền chỉnh sửa thông tin danh mục đơn vị.
- Danh mục đơn vị cần chỉnh sửa đã tồn tại trong hệ thống.

## Nguyên mẫu
[]

## Thành phần

### Form chỉnh sửa
- Tự động hiển thị thông tin đã lưu
<div style="overflow-x:auto">
Tiêu đề: Chỉnh sửa thông tin danh mục

| Trường thông tin | Control | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                             |
| :--------------- | :------ | :----------- | :--------- | :------------- | :--------------- | :----------------- | :-------------------------------- |
| Mã danh mục      | Text    | MaDM_Donvi   | -          | N              | Tự sinh          | N                  | Mã danh mục tự sinh theo hệ thống |
| Tên đơn vị       | Text    | TenDonVi     | 250        | Y              | -                | Y                  | Nhập tên đơn vị                   |
| Loại đơn vị      | Select  | LoaiDonVi    | -          | Y              | -                | Y                  | Chọn loại đơn vị (Bộ Tư Pháp, Sở Tư pháp, Tổ chức hành nghề công chứng, Đơn vị gửi thông tin ngăn chặn) |
| Đơn vị cha       | Select  | DonViChaId   | -          | N              | -                | Y                  | Chọn đơn vị cha (nếu có)          |
| Số điện thoại    | Text    | DienThoai    | 20         | N              | -                | Y                  | Nhập số điện thoại                |
| Email            | Text    | Email        | 100        | N              | -                | Y                  | Nhập thông tin email              |
| Fax              | Text    | Fax          | 20         | N              | -                | Y                  | Nhập thông tin số fax             |
| Website          | Text    | WebSite      | 100        | N              | -                | Y                  | Nhập thông tin website            |
| Tỉnh/Thành phố   | Select  | TinhThanh    | -          | N              | -                | Y                  | Chọn tỉnh/thành phố               |
| Phường/Xã        | Text    | PhuongXa     | 100        | N              | -                | Y                  | Nhập địa chỉ phường/xã            |
| Địa chỉ          | Text    | DiaChi       | 250        | N              | -                | Y                  | Nhập địa chỉ số nhà, tổ, thông, xóm |
| Thông tin khác   | Text    | ThongTinKhac | 500        | N              | -                | Y                  | Nhập thông tin khác               |
| Trạng thái       | Select  | TrangThai    | -          | Y              | Hoạt động        | Y                  | Chọn trạng thái (Hoạt động, Ngừng hoạt động) |

</div>

### Thông báo kết quả

<div style="overflow-x:auto">
| Thành phần           | Control | Bắt buộc (Y/N) | Mô tả                                                                                   |
| :------------------- | :------ | :------------- | :-------------------------------------------------------------------------------------- |
| Thông báo thành công | Label   | -              | Hiển thị khi chỉnh sửa thành công: **"Chỉnh sửa thông tin danh mục đơn vị thành công"** |
| Thông báo lỗi        | Label   | -              | Hiển thị khi có lỗi: **"Nhập thiếu thông tin bắt buộc"** hoặc **"Lỗi hệ thống"**        |

</div>

### Popup xác nhận hủy

<div style="overflow-x:auto">
| Thành phần         | Control | Bắt buộc (Y/N) | Mô tả                                                                 |
| :----------------- | :------ | :------------- | :-------------------------------------------------------------------- |
| Thông báo xác nhận | Label   | -              | Hiển thị: **"Bạn có chắc muốn hủy thao tác chỉnh sửa?"**              |
| Nút Đồng ý         | Button  | -              | Xác nhận hủy thao tác và quay về danh sách (**SCR_DM_Donvi_List**) |
| Nút Không          | Button  | -              | Ở lại màn hình chỉnh sửa (**SCR_DM_Donvi_Update**)                 |

</div>

## Chức năng

<div style="overflow-x:auto">

| Tên           | Loại   | Mô tả                                                                                   |
| :------------ | :----- | :-------------------------------------------------------------------------------------- |
| Lưu thông tin | Button | Kiểm tra hợp lệ, ghi nhận dữ liệu vào **ENT_DM_Donvi** và hiển thị thông báo thành công |
| Đóng          | Button | Hiển thị popup xác nhận hủy thao tác                                                    |

</div>
