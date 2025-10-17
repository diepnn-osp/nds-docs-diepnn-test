# Màn hình: Danh sách người tham gia giao dịch

Danh sách người tham gia giao dịch hiện thị trong form thêm mới, chỉnh sửa và trang chi tiết giao dịch công chứng

## Điều kiện tiên quyết
- Nếu ở màn hình tạo lập/chỉnh sửa, người dùng cần đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Nếu ở màn hình chi tiết, người dùng cần đã đăng nhập và có quyền xem chi tiết giao dịch công chứng.
- Đã có dữ liệu người tham gia giao dịch

## Nguyên mẫu
[]

## Thành phần

### Danh sách người tham gia giao dịch (Cá nhân)

- Với mỗi bên liên quan, hiển thị bảng danh sách cá nhân tham gia giao dịch đã được thêm

| Trường thông tin  | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                                   |
|-------------------|---------|-------|------------|----------------|------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| STT               | text    | -     | -          | -              | -                | -                  | Hiển thị STT người tham gia giao dịch                                                                                                   |
| Thông tin chung   | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "HoDem + Ten, Giới tính: GioiTinh, Ngày sinh: NgaySinh, QuocTich", thông tin nào không có bỏ trống, cắt dấu "," |
| Thông tin giấy tờ | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "SoGiayTo, NgayCap, NoiCap"                                                                                     |
| Địa chỉ hiện tại  | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "DiaChi, PhuongXa, TinhThanhPho"                                                                                |
| Thông tin khác    | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "Email, ThongTinKhac"                                                                                           |

### Danh sách người tham gia giao dịch (Tổ chức)

- Với mỗi bên liên quan, hiển thị bảng danh sách tổ chức tham gia giao dịch đã được thêm

| Trường thông tin                 | Control | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                                                                 |
|----------------------------------|---------|-------|------------|----------------|------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STT                              | text    | -     | -          | -              | -                | -                  | Hiển thị STT người tham gia giao dịch                                                                                                                                 |
| Thông tin tổ chức                | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "TenToChuc, Số giấy tờ: SoGiayToPhapNhan, NgayCap, NoiCap, DienThoaiToChuc"                   |
| Địa chỉ tổ chức                  | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "DiaChi, PhuongXa, TinhThanhPho"                                                                                                              |
| Thông tin người đại diện         | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "NguoiDaiDien, Chức vụ: ChucVuNguoiDaiDien, Giới tính: GioiTinh, Ngày sinh: NgaySinh, QuocTich", thông tin nào không có bỏ trống, cắt dấu "," |
| Thông tin giấy tờ người đại diện | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "SoGiayTo, NgayCap, NoiCap"                                                                                                                   |
| Địa chỉ người đại diện           | text    | -     | -          | -              | -                | -                  | Hiển thị theo template: "DiaChiNguoiDaiDien, PhuongXaNguoiDaiDien, TinhThanhPhoNguoiDaiDien"                                                                          |
| Thông tin khác                   | text    | ThongTinKhac | -          | -              | -                | -                  |                                                                                                                                                                       |