# Màn hình: Thêm mới người tham gia giao dịch
Popup cho phép người dùng nhập thông tin chi tiết về người tham gia giao dịch để thêm vào giao dịch công chứng.  

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Người dùng đang thao tác trong **màn hình thêm mới hoặc chỉnh sửa giao dịch công chứng**.
- Người dùng click vào nút thêm mới người tham gia giao dịch

---

## Thông tin chung

<div style="overflow-x:auto">
| Trường thông tin     | Control  | Field | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                       |
|:---------------------|:---------|:------|:-----------|:---------------|:-----------------|:-------------------|:----------------------------|
| Chọn cá nhân/tổ chức | Dropdown | -     | -          | Y              | Cá nhân          | Y                  | Form cập nhật theo lựa chọn |
</div>

### Form cá nhân
| Trường thông tin        | Control         | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|-------------------------|-----------------|------------------|------------|----------------|------------------|--------------------|------------------------------------------------|
| Họ và tên               | text            | HoDem + Ten      | 100        | Y              | -                | -                  |                                                |
| Ngày sinh               | date            | NgaySinh         | -          | Y              | -                | -                  | **BR9.3**                                      |
| Số giấy tờ nhân thân    | text            | SoGiayToNhanThan | 20         | Y              | -                | -                  | **BR9.10**                                     |
| Ngày cấp                | date            | NgayCap          | -          | Y              | -                | -                  | **BR9.3**                                      |
| Nơi cấp                 | text            | NoiCap           | 100        | Y              | -                | -                  |                                                |
| Địa chỉ hiện tại        | text            | DiaChi           | 500        | Y              | -                | -                  |                                                |
| Tỉnh/Thành phố hiện tại | combobox search | TinhThanhPho     | -          | Y              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã hiện tại      | combobox search | PhuongXa         | -          | Y              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ              | text            | DiaChiCu         | 500        | N              | -                | -                  |                                                |
| Tỉnh/Thành phố cũ       | combobox search | TinhThanhPhoCu   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ           | combobox search | QuanHuyenCu      | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ            | combobox search | PhuongXaCu       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |
| Số điện thoại           | text            | DienThoai        | 20         | N              | -                | -                  | **BR9.4**                                      |
| Giới tính               | combobox search | GioiTinh         | -          | Y              | -                | -                  | Chọn 1 từ danh mục giới tính                   |
| Email                   | text            | Email            | 255        | N              | -                | -                  | **BR9.9**                                      |
| Quốc tịch               | combobox search | QuocTich         | -          | Y              | Việt Nam         | Y                  | Chọn 1 từ danh mục quốc tịch                   |
| Thông tin khác          | textarea        | ThongTinKhac     | 500        | N              | -                | -                  |                                                |

### Form tổ chức
| Trường thông tin                 | Control         | Field                      | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|----------------------------------|-----------------|----------------------------|------------|----------------|------------------|--------------------|------------------------------------------------|
| Tên tổ chức                      | text            | TenToChuc                  | 200        | Y              | -                | -                  |                                                |
| Số giấy tờ pháp nhân             | text            | SoGiayToPhapNhan           | 50         | Y              | -                | -                  |                                                |
| Ngày cấp                         | date            | NgayCap                    | -          | Y              | -                | -                  | **BR9.3**                                      |
| Nơi cấp                          | text            | NoiCap                     | 100        | Y              | -                | -                  |                                                |
| Số điện thoại tổ chức            | text            | DienThoaiToChuc            | 20         | N              | -                | -                  | **BR9.4**                                      |
| Địa chỉ tổ chức hiện tại         | text            | DiaChiToChuc               | 500        | Y              | -                | -                  |                                                |
| Tỉnh/Thành phố tổ chức           | combobox search | TinhThanhPhoToChuc         | -          | Y              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã tổ chức                | combobox search | PhuongXaToChuc             | -          | Y              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ tổ chức cũ               | text            | DiaChiCuToChuc             | 500        | N              | -                | -                  |                                                |
| Tỉnh/Thành phố tổ chức cũ        | combobox search | TinhThanhPhoCuToChuc       | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ tổ chức            | combobox search | QuanHuyenCuToChuc          | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã tổ chức cũ             | combobox search | PhuongXaCuToChuc           | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |
| Người đại diện                   | text            | NguoiDaiDien               | 100        | Y              | -                | -                  |                                                |
| Chức vụ người đại diện           | text            | ChucVuNguoiDaiDien         | 100        | Y              | -                | -                  |                                                |
| Ngày sinh người đại diện         | date            | NgaySinh                   | -          | Y              | -                | -                  | **BR9.3**                                      |
| Số giấy tờ nhân thân             | text            | SoGiayToNhanThan           | 20         | Y              | -                | -                  | **BR9.10**                                     |
| Ngày cấp                         | date            | NgayCap                    | -          | Y              | -                | -                  | **BR9.3**                                      |
| Nơi cấp                          | text            | NoiCap                     | 100        | Y              | -                | -                  |                                                |
| Địa chỉ người đại diện           | text            | DiaChiNguoiDaiDien         | 500        | Y              | -                | -                  |                                                |
| Tỉnh/Thành phố người đại diện    | combobox search | TinhThanhPhoNguoiDaiDien   | -          | Y              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã người đại diện         | combobox search | PhuongXaNguoiDaiDien       | -          | Y              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ người đại diện        | text            | DiaChiCuNguoiDaiDien       | 500        | N              | -                | -                  |                                                |
| Tỉnh/Thành phố cũ người đại diện | combobox search | TinhThanhPhoCuNguoiDaiDien | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ người đại diện     | combobox search | QuanHuyenCuNguoiDaiDien    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ người đại diện      | combobox search | PhuongXaCuNguoiDaiDien     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

## Chức năng
| Tên             | Loại   | Mô tả                                                   |
|:----------------|:-------|:--------------------------------------------------------|
| Lưu             | Button | Thực hiện kiểm tra thông tin và lưu **UC_NTGGD_Create** |
| Hủy             | Button | Mở popup xác nhận hủy                                   |
| Biểu tượng đóng | Button | Đóng popup                                              |