# Màn hình: Chỉnh sửa tài sản
Popup cho phép người dùng chỉnh sửa thông tin chi tiết về tài sản trong giao dịch công chứng.  

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Người dùng đang thao tác trong **màn hình thêm mới hoặc chỉnh sửa giao dịch công chứng**.
- Người dùng đã bấm vào nút chỉnh sửa 1 tài sản

## Nguyên mẫu
[]

## Thông tin chung
- Các thông tin đã được ghi nhận khi tạo mới sẽ được đổ ra popup chỉnh sửa thông tin
<div style="overflow-x:auto">

| Trường thông tin   | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                    |
|:-------------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:-------------------------------------------------------------------------|
| Loại tài sản       | combobox search | LoaiTaiSan      | -          | Y              | -                | Y                  | Chọn 1 loại tài sản từ danh sách liên kết với tên giao dịch đã lựa chọn. |
| Số giấy chứng nhận | text            | SoGiayChungNhan | 50         | Y              | -                | Y                  | Số hiệu của giấy chứng nhận quyền sở hữu / quyền sử dụng.                |
| Ngày cấp           | date            | NgayCap         | -          | N              | -                | Y                  | Ngày cấp giấy chứng nhận quyền sở hữu / sử dụng.                         |
| Nơi cấp            | text            | NoiCap          | 250        | N              | -                | Y                  | Cơ quan cấp giấy chứng nhận quyền sở hữu / sử dụng.                      |
| Chủ sở hữu         | text            | ChuSoHuu        | 250        | Y              | -                | Y                  | Họ tên hoặc tên tổ chức chủ sở hữu tài sản.                              |
| Ghi chú            | text            | GhiChu          | 500        | N              | -                | Y                  | Ghi chú thêm về tài sản nếu có.                                          |

</div>

## Thông tin tài sản

### Ô tô / Xe máy

| Trường thông tin | Control | Field        | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:--------|:-------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Biển kiểm soát   | text    | BienKiemSoat | 20         | N              | -                | Y                  |       |
| Số khung         | text    | SoKhung      | 50         | Y              | -                | Y                  |       |
| Số máy           | text    | SoMay        | 50         | Y              | -                | Y                  |       |
| Nhãn hiệu        | text    | NhanHieu     | 150        | N              | -                | Y                  |       |
| Số loại          | text    | SoLoai       | 150        | N              | -                | Y                  |       |
| Loại xe          | text    | LoaiXe       | 150        | N              | -                | Y                  |       |
| Màu sơn          | text    | MauSon       | 150        | N              | -                | Y                  |       |
| Năm sản xuất     | number  | NamSanXuat   | 4          | N              | -                | Y                  |       |
| Dung tích        | text    | DungTich     | 20         | N              | -                | Y                  |       |
| Trọng tải        | text    | TrongTai     | 20         | N              | -                | Y                  |       |
| Số chỗ ngồi      | number  | SoChoNgoi    | 5          | N              | -                | Y                  |       |

---

### Đất 

| Trường thông tin    | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:--------------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN       | text            | SoVaoSoGCN     | 50         | N              | -                | Y                  |                                                |
| Thửa đất số         | text            | ThuaDatSo      | 50         | N              | -                | Y                  |                                                |
| Tờ bản đồ số        | text            | ToBanDoSo      | 50         | N              | -                | Y                  |                                                |
| Diện tích           | number            | DienTich       | 20         | N              | -                | Y                  |                                                |
| Loại đất / Mục đích | text            | MucDich        | 200        | N              | -                | Y                  |                                                |
| Thời hạn sử dụng    | text            | ThoiHan        | 200        | N              | -                | Y                  |                                                |
| Hình thức sử dụng   | Dropdown        | HinhThuc       | 200        | N              | -                | Y                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ             | text            | DiaChi         | 500        | N              | -                | Y                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố      | combobox search | TinhThanhPho   | -          | N              | -                | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã           | combobox search | PhuongXa       | -          | N              | -                | Y                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ          | text            | DiaChiCu       | 500        | N              | -                | Y                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ       | combobox search | TinhThanhPhoCu | -          | N              | -                | Y                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ       | combobox search | QuanHuyenCu    | -          | N              | -                | Y                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ        | combobox search | PhuongXaCu     | -          | N              | -                | Y                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

---

### Đất và tài sản gắn liền với đất
| Trường thông tin              | Control         | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:------------------------------|:----------------|:---------------|:-----------|:---------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN                 | text            | SoVaoSoGCN     | 100        | N        | -                | Y                  |                                                |
| Thửa đất số                   | text            | ThuaDatSo      | 50         | N        | -                | Y                  |                                                |
| Tờ bản đồ số                  | text            | ToBanDoSo      | 50         | N        | -                | Y                  |                                                |
| Diện tích                     | number          | DienTich       | 20         | N        | -                | Y                  |                                                |
| Loại đất / Mục đích           | text            | MucDich        | 200        | N        | -                | Y                  |                                                |
| Thời hạn sử dụng              | text            | ThoiHan        | 200        | N        | -                | Y                  |                                                |
| Hình thức sử dụng             | Dropdown        | HinhThuc       | 200        | N        | -                | Y                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ                       | text            | DiaChi         | 500        | N        | -                | Y                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố                | combobox search | TinhThanhPho   | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã                     | combobox search | PhuongXa       | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ                    | text            | DiaChiCu       | 500        | N        | -                | Y                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ                 | combobox search | TinhThanhPhoCu | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ                 | combobox search | QuanHuyenCu    | -          | N        | -                | Y                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ                  | combobox search | PhuongXaCu     | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |
| Loại tài sản gắn liền với đất | combobox search | LoaiTaiSan     | -          | Y        | -                | Y                  | Chọn 1 từ danh sách trong entity               |
| Tên tài sản                   | text            | TenTaiSan      | 200        | N        | -                | Y                  |                                                |
| Diện tích tài sản             | number          | DienTichTaiSan | 20         | N        | -                | Y                  |                                                |
| Thời hạn sở hữu               | text            | ThoiHanSoHuu   | 200        | N        | -                | Y                  |                                                |
| Hình thức sở hữu              | text            | HinhThucSoHuu  | 200        | N        | -                | Y                  |                                                |

---

### Hợp đồng mua bán BĐS
| Trường thông tin | Control         | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:----------------|:---------------|:-----------|:---------|:-----------------|:-------------------|:-----------------------------------------------|
| Số hợp đồng      | text            | SoHopDong      | 100        | Y        | -                | Y                  |                                                |
| Tên hợp đồng     | text            | TenHopDong     | 200        | N        | -                | Y                  |                                                |
| Ngày hợp đồng    | date            | NgayHopDong    | -          | N        | -                | Y                  |                                                |
| Bên bán          | textarea        | BenBan         | 500        | N        | -                | Y                  |                                                |
| Bên mua          | textarea        | BenMua         | 500        | N        | -                | Y                  |                                                |
| Tên tài sản      | text            | TenTaiSan      | 200        | N        | -                | Y                  |                                                |
| Diện tích        | number          | DienTich       | 20         | N        | -                | Y                  |                                                |
| Thời hạn sở hữu  | text            | ThoiHanSoHuu   | 200        | N        | -                | Y                  |                                                |
| Hình thức sở hữu | text            | HinhThucSoHuu  | 200        | N        | -                | Y                  |                                                |
| Địa chỉ          | text            | DiaChi         | 500        | N        | -                | Y                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố   | combobox search | TinhThanhPho   | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã        | combobox search | PhuongXa       | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ       | text            | DiaChiCu       | 500        | N        | -                | Y                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ    | combobox search | TinhThanhPhoCu | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ    | combobox search | QuanHuyenCu    | -          | N        | -                | Y                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ     | combobox search | PhuongXaCu     | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

---

### Bất động sản khác
| Trường thông tin    | Control         | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:--------------------|:----------------|:---------------|:-----------|:---------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN       | text            | SoVaoSoGCN     | 100        | N        | -                | Y                  |                                                |
| Thửa đất số         | text            | ThuaDatSo      | 50         | N        | -                | Y                  |                                                |
| Tờ bản đồ số        | text            | ToBanDoSo      | 50         | N        | -                | Y                  |                                                |
| Diện tích           | number          | DienTich       | 20         | N        | -                | Y                  |                                                |
| Loại đất / Mục đích | text            | MucDich        | 200        | N        | -                | Y                  |                                                |
| Thời hạn sử dụng    | text            | ThoiHan        | 200        | N        | -                | Y                  |                                                |
| Hình thức sử dụng   | Dropdown        | HinhThuc       | 200        | N        | -                | Y                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ             | text            | DiaChi         | 500        | N        | -                | Y                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố      | combobox search | TinhThanhPho   | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã           | combobox search | PhuongXa       | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ          | text            | DiaChiCu       | 500        | N        | -                | Y                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ       | combobox search | TinhThanhPhoCu | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ       | combobox search | QuanHuyenCu    | -          | N        | -                | Y                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ        | combobox search | PhuongXaCu     | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

### Tàu biển
| Trường thông tin    | Control | Field            | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên tàu             | text    | TenTau           | 200        | N        | -                | Y                  |       |
| Hô hiệu             | text    | HoHieu           | 50         | N        | -                | Y                  |       |
| Loại tàu            | text    | LoaiTau          | 100        | N        | -                | Y                  |       |
| Năm đóng tàu        | number  | NamDongTau       | 4          | N        | -                | Y                  |       |
| Nơi đóng tàu        | text    | NoiDongTau       | 500        | N        | -                | Y                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | -          | N        | -                | Y                  |       |
| Chiều rộng          | number  | ChieuRong        | 10         | N        | -                | Y                  |       |
| Chiều cao mạn tàu   | number  | ChieuCaoManTau   | 10         | N        | -                | Y                  |       |
| Mức nước tối đa     | number  | MucNuocToiDa     | 10         | N        | -                | Y                  |       |
| Dung tích toàn phần | number  | DungTichToanPhan | 10         | N        | -                | Y                  |       |
| Dung tích thực dụng | number  | DungTichThucDung | 10         | N        | -                | Y                  |       |
| Trọng tải toàn phần | number  | TrongTaiToanPhan | 10         | N        | -                | Y                  |       |
| Công suất máy chính | text    | CongSuatMayChinh | 100        | N        | -                | Y                  |       |
| Cảng đăng ký        | text    | CangDangKy       | 200        | N        | -                | Y                  |       |
| Ngày đăng ký        | date    | NgayDangKy       | -          | N        | -                | Y                  |       |
| Cơ quan đăng kiểm   | text    | CoQuanDangKiem   | 200        | N        | -                | Y                  |       |
| Số đăng ký          | text    | SoDangKy         | 100        | N        | -                | Y                  |       |

### Tàu kéo - Ghe - Thuyền
| Trường thông tin    | Control | Field            | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên phương tiện     | text    | TenPhuongTien    | 200        | N        | -                | Y                  |       |
| Hô hiệu             | text    | HoHieu           | 50         | N        | -                | Y                  |       |
| Loại phương tiện    | text    | LoaiPhuongTien   | 100        | N        | -                | Y                  |       |
| Cấp phương tiện     | text    | CapPhuongTien    | 100        | N        | -                | Y                  |       |
| Công dụng           | text    | CongDung         | 200        | N        | -                | Y                  |       |
| Năm đóng            | number  | NamDong          | 4          | N        | -                | Y                  |       |
| Nơi đóng            | text    | NoiDong          | 200        | N        | -                | Y                  |       |
| Chiều dài thiết kế  | number  | ChieuDaiThietKe  | 10         | N        | -                | Y                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | 10         | N        | -                | Y                  |       |
| Chiều rộng thiết kế | number  | ChieuRongThietKe | 10         | N        | -                | Y                  |       |
| Chiều rộng lớn nhất | number  | ChieuRongLonNhat | 10         | N        | -                | Y                  |       |
| Chiều cao mạn       | number  | ChieuCaoMan      | 10         | N        | -                | Y                  |       |
| Chiều chìm          | number  | ChieuChim        | 10         | N        | -                | Y                  |       |
| Mạn khô             | number  | ManKho           | 10         | N        | -                | Y                  |       |
| Vật liệu vỏ         | text    | VatLieuVo        | 100        | N        | -                | Y                  |       |
| Máy chính           | text    | MayChinh         | 200        | N        | -                | Y                  |       |
| Trọng tải toàn phần | text    | TrongTaiToanPhan | 200        | N        | -                | Y                  |       |

### Tàu cá
| Trường thông tin          | Control | Field            | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------------|:--------|:-----------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên tàu cá                | text    | TenTau           | 200        | N        | -                | Y                  |       |
| Hô hiệu                   | text    | HoHieu           | 50         | N        | -                | Y                  |       |
| Số đăng ký tàu cá         | text    | SoDangKy         | 100        | N        | -                | Y                  |       |
| Loại tàu cá               | text    | LoaiTau          | 100        | N        | -                | Y                  |       |
| Năm đóng tàu              | number  | NamDongTau       | 4          | N        | -                | Y                  |       |
| Nơi đóng tàu              | text    | NoiDongTau       | 200        | N        | -                | Y                  |       |
| Chiều dài lớn nhất (m)    | number  | ChieuDaiLonNhat  | 10         | N        | -                | Y                  |       |
| Chiều rộng (m)            | number  | ChieuRong        | 10         | N        | -                | Y                  |       |
| Chiều cao mạn tàu (m)     | number  | ChieuCaoManTau   | 10         | N        | -                | Y                  |       |
| Mức nước tối đa (m)       | number  | MucNuocToiDa     | 10         | N        | -                | Y                  |       |
| Dung tích toàn phần (GT)  | number  | DungTichToanPhan | 10         | N        | -                | Y                  |       |
| Dung tích thực dụng (NT)  | number  | DungTichThucDung | 10         | N        | -                | Y                  |       |
| Trọng tải toàn phần (DWT) | number  | TrongTaiToanPhan | 10         | N        | -                | Y                  |       |
| Công suất máy chính       | text    | CongSuatMayChinh | 100        | N        | -                | Y                  |       |
| Cảng đăng ký              | text    | CangDangKy       | 200        | N        | -                | Y                  |       |
| Ngày đăng ký              | date    | NgayDangKy       | -          | N        | -                | Y                  |       |
| Cơ quan đăng kiểm         | text    | CoQuanDangKiem   | 200        | N        | -                | Y                  |       |


### Tàu bay
| Trường thông tin  | Control | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:---------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Số hiệu đăng ký   | text    | SoHieuDangKy   | 100        | N        | -                | Y                  |       |
| Loại tàu bay      | text    | LoaiTauBay     | 100        | N        | -                | Y                  |       |
| Kiểu loại tàu bay | text    | KieuLoaiTauBay | 100        | N        | -                | Y                  |       |
| Nhà sản xuất      | text    | NhaSanXuat     | 200        | N        | -                | Y                  |       |
| Quốc gia sản xuất | text    | QuocGiaSanXuat | 100        | N        | -                | Y                  |       |
| Năm xuất xưởng    | number  | NamXuatXuong   | 4          | N        | -                | Y                  |       |
| Số xuất xưởng     | text    | SoXuatXuong    | 100        | N        | -                | Y                  |       |
| Kiểu loại động cơ | text    | KieuLoaiDongCo | 100        | N        | -                | Y                  |       |

### Sổ tiết kiệm
| Trường  thông tin | Control | Field       | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên tài sản       | text    | TenTaiSan   | 200        | N        | -                | Y                  |       |
| Số dư tiền gửi    | number  | SoDuTienGui | 100        | N        | -                | Y                  |       |
| Kỳ hạn            | text    | KyHan       | 100        | N        | -                | Y                  |       |
| Loại tiền         | select  | LoaiTien    | 50         | N        | -                | Y                  |       |

### Trái phiếu
| Trường thông tin | Control | Field         | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:--------|:--------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên trái phiếu   | text    | TenTraiPhieu  | 200        | N        | -                | Y                  |       |
| Số lượng         | number  | SoLuong       | 10         | N        | -                | Y                  |       |
| Mệnh giá         | number  | MenhGia       | 100        | N        | -                | Y                  |       |
| Tổng mệnh giá    | number  | TongMenhGia   | 100        | N        | -                | Y                  |       |
| Kỳ hạn           | text    | KyHan         | 100        | N        | -                | Y                  |       |
| Loại trái phiếu  | text    | LoaiTraiPhieu | 100        | N        | -                | Y                  |       |

### Cổ phiếu
| Trường thông tin               | Control         | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-------------------------------|:----------------|:---------------|:-----------|:---------|:-----------------|:-------------------|:-----------------------------------------------|
| Mã số cổ phiếu                 | text            | MaSoCoPhieu    | 50         | N        | -                | Y                  |                                                |
| Số lượng                       | number          | SoLuong        | -          | N        | -                | Y                  |                                                |
| Loại cổ phiếu                  | text            | LoaiCoPhieu    | 100        | N        | -                | Y                  |                                                |
| Mệnh giá / cổ phiếu            | number          | MenhGia        | -          | N        | -                | Y                  |                                                |
| Tổng mệnh giá                  | number          | TongMenhGia    | -          | N        | -                | Y                  |                                                |
| Địa chỉ công ty phát hành      | text            | DiaChi         | 500        | N        | -                | Y                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố                 | combobox search | TinhThanhPho   | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã                      | combobox search | PhuongXa       | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ công ty phát hành (cũ) | text            | DiaChiCu       | 500        | N        | -                | Y                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ                  | combobox search | TinhThanhPhoCu | -          | N        | -                | Y                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ                  | combobox search | QuanHuyenCu    | -          | N        | -                | Y                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ                   | combobox search | PhuongXaCu     | -          | N        | -                | Y                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

### Tài sản khác
| Trường thông tin  | Control  | Field          | Max length | Bắt buộc | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:---------|:---------------|:-----------|:---------|:-----------------|:-------------------|:------|
| Tên tài sản       | text     | TenTaiSan      | 200        | N        | -                | Y                  |       |
| Thông tin tài sản | textarea | ThongTinTaiSan | 1000       | N        | -                | Y                  |       |

## Chức năng
| Tên             | Loại   | Mô tả                                                  |
|:----------------|:-------|:-------------------------------------------------------|
| Lưu             | Button | Thực hiện kiểm tra thông tin và lưu **UC_TSGD_Update** |
| Hủy             | Button | Mở popup xác nhận hủy                                  |
| Biểu tượng đóng | Button | Đóng popup                                             |
