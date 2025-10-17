# Màn hình: Popup chi tiết thông tin tài sản
Popup chi tiết thông tin tài sản hiển thị khi người dùng bấm xem chi tiết thông tin 1 tài sản

## Điều kiện tiên quyết
- Nếu ở màn hình tạo lập/chỉnh sửa, người dùng cần đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Nếu ở màn hình chi tiết, người dùng cần đã đăng nhập và có quyền xem chi tiết giao dịch công chứng.
- Đã có dữ liệu tài sản

## Nguyên mẫu
[]

## Thành phần

### Thông tin chung

- Hiển thị dữ liệu đã ghi nhận/lưu
- Với mỗi loại tài sản, hiển thị các thông tin khác nhau.

<div style="overflow-x:auto">

| Trường thông tin   | Control | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-------------------|:--------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số giấy chứng nhận | text    | SoGiayChungNhan | -          | -              | -                | -                  |       |
| Ngày cấp           | date    | NgayCap         | -          | -              | -                | -                  |       |
| Nơi cấp            | text    | NoiCap          | -          | -              | -                | -                  |       |
| Chủ sở hữu         | text    | ChuSoHuu        | -          | -              | -                | -                  |       |
| Ghi chú            | text    | GhiChu          | -          | -              | -                | -                  |       |

</div>

### Thông tin tài sản

- Hiển thị theo từng loại tài sản

#### Ô tô / Xe máy

| Trường thông tin  | Control | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:-------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Biển kiểm soát    | text    | BienKiemSoat | -          | -              | -                | -                  |       |
| Số khung          | text    | SoKhung      | -          | -              | -                | -                  |       |
| Số máy            | text    | SoMay        | -          | -              | -                | -                  |       |
| Nhãn hiệu         | text    | NhanHieu     | -          | -              | -                | -                  |       |
| Số loại           | text    | SoLoai       | -          | -              | -                | -                  |       |
| Loại xe           | text    | LoaiXe       | -          | -              | -                | -                  |       |
| Màu sơn           | text    | MauSon       | -          | -              | -                | -                  |       |
| Năm sản xuất      | number  | NamSanXuat   | -          | -              | -                | -                  |       |
| Dung tích xi-lanh | text    | DungTich     | -          | -              | -                | -                  |       |
| Trọng tải         | text    | TrongTai     | -          | -              | -                | -                  |       |
| Số chỗ ngồi       | number  | SoChoNgoi    | -          | -              | -                | -                  |       |

---

#### Đất 

| Trường thông tin    | Control | Field                                                | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số vào sổ GCN       | text    | SoVaoSoGCN                                           | -          | -              | -                | -                  |       |
| Thửa đất số         | text    | ThuaDatSo                                            | -          | -              | -                | -                  |       |
| Tờ bản đồ số        | text    | ToBanDoSo                                            | -          | -              | -                | -                  |       |
| Diện tích           | number  | DienTich                                             | -          | -              | -                | -                  |       |
| Loại đất / Mục đích | text    | MucDich                                              | -          | -              | -                | -                  |       |
| Thời hạn sử dụng    | text    | ThoiHan                                              | -          | -              | -                | -                  |       |
| Hình thức sử dụng   | text    | HinhThuc                                             | -          | -              | -                | -                  |       |
| Địa chỉ cũ          | text    | DiaChiCu + PhuongXaCu + QuanHuyenCu + TinhThanhPhoCu | -          | -              | -                | -                  |       |
| Địa chỉ mới         | text    | DiaChi + PhuongXa + TinhThanhPho                     | -          | -              | -                | -                  |       |

---

#### Đất và tài sản gắn liền với đất

| Trường thông tin              | Control | Field                                                | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------------------|:--------|:-----------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số vào sổ GCN                 | text    | SoVaoSoGCN                                           | -          | -              | -                | -                  |       |
| Thửa đất số                   | text    | ThuaDatSo                                            | -          | -              | -                | -                  |       |
| Tờ bản đồ số                  | text    | ToBanDoSo                                            | -          | -              | -                | -                  |       |
| Diện tích                     | number  | DienTich                                             | -          | -              | -                | -                  |       |
| Loại đất / Mục đích           | text    | MucDich                                              | -          | -              | -                | -                  |       |
| Thời hạn sử dụng              | text    | ThoiHan                                              | -          | -              | -                | -                  |       |
| Hình thức sử dụng             | text    | HinhThuc                                             | -          | -              | -                | -                  |       |
| Địa chỉ cũ                    | text    | DiaChiCu + PhuongXaCu + QuanHuyenCu + TinhThanhPhoCu | -          | -              | -                | -                  |       |
| Địa chỉ mới                   | text    | DiaChi + PhuongXa + TinhThanhPho                     | -          | -              | -                | -                  |       |
| Loại tài sản gắn liền với đất | text    | LoaiTaiSan                                           | -          | -              | -                | -                  |       |
| Tên tài sản                   | text    | TenTaiSan                                            | -          | -              | -                | -                  |       |
| Diện tích tài sản             | number  | DienTichTaiSan                                       | -          | -              | -                | -                  |       |
| Thời hạn sở hữu               | text    | ThoiHanSoHuu                                         | -          | -              | -                | -                  |       |
| Hình thức sở hữu              | text    | HinhThucSoHuu                                        | -          | -              | -                | -                  |       |

---

#### Hợp đồng mua bán BĐS

| Trường thông tin | Control  | Field                                                | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:---------|:-----------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số hợp đồng      | text     | SoHopDong                                            | -          | -              | -                | -                  |       |
| Tên hợp đồng     | text     | TenHopDong                                           | -          | -              | -                | -                  |       |
| Ngày hợp đồng    | date     | NgayHopDong                                          | -          | -              | -                | -                  |       |
| Bên bán          | textarea | BenBan                                               | -          | -              | -                | -                  |       |
| Bên mua          | textarea | BenMua                                               | -          | -              | -                | -                  |       |
| Tên tài sản      | text     | TenTaiSan                                            | -          | -              | -                | -                  |       |
| Diện tích        | number   | DienTich                                             | -          | -              | -                | -                  |       |
| Thời hạn sở hữu  | text     | ThoiHanSoHuu                                         | -          | -              | -                | -                  |       |
| Hình thức sở hữu | text     | HinhThucSoHuu                                        | -          | -              | -                | -                  |       |
| Địa chỉ cũ       | text     | DiaChiCu + PhuongXaCu + QuanHuyenCu + TinhThanhPhoCu | -          | -              | -                | -                  |       |
| Địa chỉ mới      | text     | DiaChi + PhuongXa + TinhThanhPho                     | -          | -              | -                | -                  |       |

---

#### Bất động sản khác

| Trường thông tin    | Control | Field                                                | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số vào sổ GCN       | text    | SoVaoSoGCN                                           | -          | -              | -                | -                  |       |
| Thửa đất số         | text    | ThuaDatSo                                            | -          | -              | -                | -                  |       |
| Tờ bản đồ số        | text    | ToBanDoSo                                            | -          | -              | -                | -                  |       |
| Diện tích           | number  | DienTich                                             | -          | -              | -                | -                  |       |
| Loại đất / Mục đích | text    | MucDich                                              | -          | -              | -                | -                  |       |
| Thời hạn sử dụng    | text    | ThoiHan                                              | -          | -              | -                | -                  |       |
| Hình thức sử dụng   | text    | HinhThuc                                             | -          | -              | -                | -                  |       |
| Địa chỉ cũ          | text    | DiaChiCu + PhuongXaCu + QuanHuyenCu + TinhThanhPhoCu | -          | -              | -                | -                  |       |
| Địa chỉ mới         | text    | DiaChi + PhuongXa + TinhThanhPho                     | -          | -              | -                | -                  |       |

---
 
#### Tàu biển

| Trường thông tin    | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tàu             | text    | TenTau           | -          | -              | -                | -                  |       |
| Hô hiệu             | text    | HoHieu           | -          | -              | -                | -                  |       |
| Loại tàu            | text    | LoaiTau          | -          | -              | -                | -                  |       |
| Năm đóng tàu        | number  | NamDongTau       | -          | -              | -                | -                  |       |
| Nơi đóng tàu        | text    | NoiDongTau       | -          | -              | -                | -                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | -          | -              | -                | -                  |       |
| Chiều rộng          | number  | ChieuRong        | -          | -              | -                | -                  |       |
| Chiều cao mạn tàu   | number  | ChieuCaoManTau   | -          | -              | -                | -                  |       |
| Mức nước tối đa     | number  | MucNuocToiDa     | -          | -              | -                | -                  |       |
| Dung tích toàn phần | number  | DungTichToanPhan | -          | -              | -                | -                  |       |
| Dung tích thực dụng | number  | DungTichThucDung | -          | -              | -                | -                  |       |
| Trọng tải toàn phần | number  | TrongTaiToanPhan | -          | -              | -                | -                  |       |
| Công suất máy chính | text    | CongSuatMayChinh | -          | -              | -                | -                  |       |
| Cảng đăng ký        | text    | CangDangKy       | -          | -              | -                | -                  |       |
| Ngày đăng ký        | date    | NgayDangKy       | -          | -              | -                | -                  |       |
| Cơ quan đăng kiểm   | text    | CoQuanDangKiem   | -          | -              | -                | -                  |       |
| Số đăng ký          | text    | SoDangKy         | -          | -              | -                | -                  |       |

---

#### Tàu kéo - Ghe - Thuyền

| Trường thông tin    | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên phương tiện     | text    | TenPhuongTien    | -          | -              | -                | -                  |       |
| Hô hiệu             | text    | HoHieu           | -          | -              | -                | -                  |       |
| Loại phương tiện    | text    | LoaiPhuongTien   | -          | -              | -                | -                  |       |
| Cấp phương tiện     | text    | CapPhuongTien    | -          | -              | -                | -                  |       |
| Công dụng           | text    | CongDung         | -          | -              | -                | -                  |       |
| Năm đóng            | number  | NamDong          | -          | -              | -                | -                  |       |
| Nơi đóng            | text    | NoiDong          | -          | -              | -                | -                  |       |
| Chiều dài thiết kế  | number  | ChieuDaiThietKe  | -          | -              | -                | -                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | -          | -              | -                | -                  |       |
| Chiều rộng thiết kế | number  | ChieuRongThietKe | -          | -              | -                | -                  |       |
| Chiều rộng lớn nhất | number  | ChieuRongLonNhat | -          | -              | -                | -                  |       |
| Chiều cao mạn       | number  | ChieuCaoMan      | -          | -              | -                | -                  |       |
| Chiều chìm          | number  | ChieuChim        | -          | -              | -                | -                  |       |
| Mạn khô             | number  | ManKho           | -          | -              | -                | -                  |       |
| Vật liệu vỏ         | text    | VatLieuVo        | -          | -              | -                | -                  |       |
| Máy chính           | text    | MayChinh         | -          | -              | -                | -                  |       |
| Trọng tải toàn phần | text    | TrongTaiToanPhan | -          | -              | -                | -                  |       |

---

#### Tàu cá

| Trường thông tin          | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tàu cá                | text    | TenTau           | -          | -              | -                | -                  |       |
| Hô hiệu                   | text    | HoHieu           | -          | -              | -                | -                  |       |
| Số đăng ký tàu cá         | text    | SoDangKy         | -          | -              | -                | -                  |       |
| Loại tàu cá               | text    | LoaiTau          | -          | -              | -                | -                  |       |
| Năm đóng tàu              | number  | NamDongTau       | -          | -              | -                | -                  |       |
| Nơi đóng tàu              | text    | NoiDongTau       | -          | -              | -                | -                  |       |
| Chiều dài lớn nhất (m)    | number  | ChieuDaiLonNhat  | -          | -              | -                | -                  |       |
| Chiều rộng (m)            | number  | ChieuRong        | -          | -              | -                | -                  |       |
| Chiều cao mạn tàu (m)     | number  | ChieuCaoManTau   | -          | -              | -                | -                  |       |
| Mức nước tối đa (m)       | number  | MucNuocToiDa     | -          | -              | -                | -                  |       |
| Dung tích toàn phần (GT)  | number  | DungTichToanPhan | -          | -              | -                | -                  |       |
| Dung tích thực dụng (NT)  | number  | DungTichThucDung | -          | -              | -                | -                  |       |
| Trọng tải toàn phần (DWT) | number  | TrongTaiToanPhan | -          | -              | -                | -                  |       |
| Công suất máy chính       | text    | CongSuatMayChinh | -          | -              | -                | -                  |       |
| Cảng đăng ký              | text    | CangDangKy       | -          | -              | -                | -                  |       |
| Ngày đăng ký              | date    | NgayDangKy       | -          | -              | -                | -                  |       |
| Cơ quan đăng kiểm         | text    | CoQuanDangKiem   | -          | -              | -                | -                  |       |

---

#### Tàu bay

| Trường thông tin  | Control | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số hiệu đăng ký   | text    | SoHieuDangKy   | -          | -              | -                | -                  |       |
| Loại tàu bay      | text    | LoaiTauBay     | -          | -              | -                | -                  |       |
| Kiểu loại tàu bay | text    | KieuLoaiTauBay | -          | -              | -                | -                  |       |
| Nhà sản xuất      | text    | NhaSanXuat     | -          | -              | -                | -                  |       |
| Quốc gia sản xuất | text    | QuocGiaSanXuat | -          | -              | -                | -                  |       |
| Năm xuất xưởng    | number  | NamXuatXuong   | -          | -              | -                | -                  |       |
| Số xuất xưởng     | text    | SoXuatXuong    | -          | -              | -                | -                  |       |
| Kiểu loại động cơ | text    | KieuLoaiDongCo | -          | -              | -                | -                  |       |

---

#### Sổ tiết kiệm

| Trường  thông tin | Control | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tài sản       | text    | TenTaiSan   | -          | -              | -                | -                  |       |
| Số dư tiền gửi    | number  | SoDuTienGui | -          | -              | -                | -                  |       |
| Kỳ hạn            | text    | KyHan       | -          | -              | -                | -                  |       |
| Loại tiền         | select  | LoaiTien    | -          | -              | -                | -                  |       |

---

#### Trái phiếu

| Trường thông tin | Control | Field         | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:--------|:--------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên trái phiếu   | text    | TenTraiPhieu  | -          | -              | -                | -                  |       |
| Số lượng         | number  | SoLuong       | -          | -              | -                | -                  |       |
| Mệnh giá         | number  | MenhGia       | -          | -              | -                | -                  |       |
| Tổng mệnh giá    | number  | TongMenhGia   | -          | -              | -                | -                  |       |
| Kỳ hạn           | text    | KyHan         | -          | -              | -                | -                  |       |
| Loại trái phiếu  | text    | LoaiTraiPhieu | -          | -              | -                | -                  |       |

---

#### Cổ phiếu

| Trường thông tin                | Control | Field                                                | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------------------|:--------|:-----------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Mã số cổ phiếu                  | text    | MaSoCoPhieu                                          | -          | -              | -                | -                  |       |
| Số lượng                        | number  | SoLuong                                              | -          | -              | -                | -                  |       |
| Loại cổ phiếu                   | text    | LoaiCoPhieu                                          | -          | -              | -                | -                  |       |
| Mệnh giá / cổ phiếu             | number  | MenhGia                                              | -          | -              | -                | -                  |       |
| Tổng mệnh giá                   | number  | TongMenhGia                                          | -          | -              | -                | -                  |       |
| Địa chỉ công ty phát hành (cũ)  | text    | DiaChiCu + PhuongXaCu + QuanHuyenCu + TinhThanhPhoCu | -          | -              | -                | -                  |       |
| Địa chỉ công ty phát hành (mới) | text    | DiaChi + PhuongXa + TinhThanhPho                     | -          | -              | -                | -                  |       |

---

#### Tài sản khác

| Trường thông tin  | Control  | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:---------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tài sản       | text     | TenTaiSan      | -          | -              | -                | -                  |       |
| Thông tin tài sản | textarea | ThongTinTaiSan | -          | -              | -                | -                  |       |


### Nút chức năng

| Tên  | Loại   | Mô tả                |
|:-----|:-------|:---------------------|
| Đóng | Button | Click vào đóng popup |