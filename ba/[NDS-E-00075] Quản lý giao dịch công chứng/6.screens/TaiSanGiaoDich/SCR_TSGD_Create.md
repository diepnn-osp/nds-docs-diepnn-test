# Màn hình: Thêm mới tài sản
Popup cho phép người dùng nhập thông tin chi tiết về tài sản để thêm vào giao dịch công chứng.  

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền tạo hoặc chỉnh sửa giao dịch công chứng.
- Người dùng đang thao tác trong **màn hình thêm mới hoặc chỉnh sửa giao dịch công chứng**.
- Người dùng click vào nút thêm mới tài sản

## Nguyên mẫu
[]

## Thông tin chung

<div style="overflow-x:auto">

| Trường thông tin           | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                    |
|:---------------------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:-------------------------------------------------------------------------|
| Loại tài sản               | combobox search | LoaiTaiSan      | -          | Y              | -                | -                  | Chọn 1 loại tài sản từ danh sách liên kết với tên giao dịch đã lựa chọn. |
| Số giấy chứng nhận/đăng ký | text            | SoGiayChungNhan | 50         | Y              | -                | -                  | Số hiệu của giấy chứng nhận quyền sở hữu / quyền sử dụng/Đăng ký.        |
| Ngày cấp                   | date            | NgayCap         | -          | N              | -                | -                  | Ngày cấp giấy chứng nhận quyền sở hữu / sử dụng.                         |
| Nơi cấp                    | text            | NoiCap          | 250        | N              | -                | -                  | Cơ quan cấp giấy chứng nhận quyền sở hữu / sử dụng.                      |
| Chủ sở hữu                 | text            | ChuSoHuu        | 250        | Y              | -                | -                  | Họ tên hoặc tên tổ chức chủ sở hữu tài sản.                              |
| Ghi chú                    | text            | GhiChu          | 500        | N              | -                | -                  | Ghi chú thêm về tài sản nếu có.                                          |

</div>

## Thông tin tài sản

### Ô tô / Xe máy

| Trường thông tin | Control | Field        | Max length | Bắt buộc (Y/N) | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:--------|:-------------|:-----------|:---------------|:-------------------|:------|
| Biển kiểm soát   | text    | BienKiemSoat | 20         | N              | -                  |       |
| Số khung         | text    | SoKhung      | 50         | Y              | -                  |       |
| Số máy           | text    | SoMay        | 50         | Y              | -                  |       |
| Nhãn hiệu        | text    | NhanHieu     | 150        | N              | -                  |       |
| Số loại          | text    | SoLoai       | 150        | N              | -                  |       |
| Loại xe          | text    | LoaiXe       | 150        | N              | -                  |       |
| Màu sơn          | text    | MauSon       | 150        | N              | -                  |       |
| Năm sản xuất     | number  | NamSanXuat   | 4          | N              | -                  |       |
| Dung tích        | text    | DungTich     | 20         | N              | -                  |       |
| Trọng tải        | text    | TrongTai     | 20         | N              | -                  |       |
| Số chỗ ngồi      | number  | SoChoNgoi    | 5          | N              | -                  |       |

---

### Đất 

| Trường thông tin    | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:--------------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN       | text            | SoVaoSoGCN     | 50         | N              | -                | -                  |                                                |
| Thửa đất số         | text            | ThuaDatSo      | 50         | N              | -                | -                  |                                                |
| Tờ bản đồ số        | text            | ToBanDoSo      | 50         | N              | -                | -                  |                                                |
| Diện tích           | number          | DienTich       | 20         | N              | -                | -                  |                                                |
| Loại đất / Mục đích | text            | MucDich        | 200        | N              | -                | -                  |                                                |
| Thời hạn sử dụng    | text            | ThoiHan        | 200        | N              | -                | -                  |                                                |
| Hình thức sử dụng   | Dropdown        | HinhThuc       | 200        | N              | -                | -                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ             | text            | DiaChi         | 500        | N              | -                | -                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố      | combobox search | TinhThanhPho   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã           | combobox search | PhuongXa       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ          | text            | DiaChiCu       | 500        | N              | -                | -                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ       | combobox search | TinhThanhPhoCu | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ       | combobox search | QuanHuyenCu    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ        | combobox search | PhuongXaCu     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

---

### Đất và tài sản gắn liền với đất
| Trường thông tin              | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:------------------------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN                 | text            | SoVaoSoGCN     | 50         | N              | -                | -                  |                                                |
| Thửa đất số                   | text            | ThuaDatSo      | 50         | N              | -                | -                  |                                                |
| Tờ bản đồ số                  | text            | ToBanDoSo      | 50         | N              | -                | -                  |                                                |
| Diện tích                     | number          | DienTich       | 20         | N              | -                | -                  |                                                |
| Loại đất / Mục đích           | text            | MucDich        | 200        | N              | -                | -                  |                                                |
| Thời hạn sử dụng              | text            | ThoiHan        | 200        | N              | -                | -                  |                                                |
| Hình thức sử dụng             | Dropdown        | HinhThuc       | 200        | N              | -                | -                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ                       | text            | DiaChi         | 500        | N              | -                | -                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố                | combobox search | TinhThanhPho   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã                     | combobox search | PhuongXa       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ                    | text            | DiaChiCu       | 500        | N              | -                | -                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ                 | combobox search | TinhThanhPhoCu | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ                 | combobox search | QuanHuyenCu    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ                  | combobox search | PhuongXaCu     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |
| Loại tài sản gắn liền với đất | combobox search | LoaiTaiSan     | -          | Y              | -                | -                  | Chọn 1 từ danh sách trong entity               |
| Tên tài sản                   | text            | TenTaiSan      | 200        | N              | -                | -                  |                                                |
| Diện tích tài sản             | number          | DienTichTaiSan | 20         | N              | -                | -                  |                                                |
| Thời hạn sở hữu               | text            | ThoiHanSoHuu   | 200        | N              | -                | -                  |                                                |
| Hình thức sở hữu              | text            | HinhThucSoHuu  | 200        | N              | -                | -                  |                                                |

---

### Hợp đồng mua bán BĐS
| Trường thông tin | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-----------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số hợp đồng      | text            | SoHopDong      | 50         | Y              | -                | -                  |                                                |
| Tên hợp đồng     | text            | TenHopDong     | 200        | N              | -                | -                  |                                                |
| Ngày hợp đồng    | date            | NgayHopDong    | -          | N              | -                | -                  |                                                |
| Bên bán          | textarea        | BenBan         | 500        | N              | -                | -                  |                                                |
| Bên mua          | textarea        | BenMua         | 500        | N              | -                | -                  |                                                |
| Tên tài sản      | text            | TenTaiSan      | 200        | N              | -                | -                  |                                                |
| Diện tích        | number          | DienTich       | 20         | N              | -                | -                  |                                                |
| Thời hạn sở hữu  | text            | ThoiHanSoHuu   | 200        | N              | -                | -                  |                                                |
| Hình thức sở hữu | text            | HinhThucSoHuu  | 200        | N              | -                | -                  |                                                |
| Địa chỉ          | text            | DiaChi         | 500        | N              | -                | -                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố   | combobox search | TinhThanhPho   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã        | combobox search | PhuongXa       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ       | text            | DiaChiCu       | 500        | N              | -                | -                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ    | combobox search | TinhThanhPhoCu | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ    | combobox search | QuanHuyenCu    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ     | combobox search | PhuongXaCu     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

---

### Bất động sản khác
| Trường thông tin    | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:--------------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Số vào sổ GCN       | text            | SoVaoSoGCN     | 100        | N              | -                | -                  |                                                |
| Thửa đất số         | text            | ThuaDatSo      | 50         | N              | -                | -                  |                                                |
| Tờ bản đồ số        | text            | ToBanDoSo      | 50         | N              | -                | -                  |                                                |
| Diện tích           | number          | DienTich       | 20         | N              | -                | -                  |                                                |
| Loại đất / Mục đích | text            | MucDich        | 200        | N              | -                | -                  |                                                |
| Thời hạn sử dụng    | text            | ThoiHan        | 200        | N              | -                | -                  |                                                |
| Hình thức sử dụng   | Dropdown        | HinhThuc       | 200        | N              | -                | -                  | Chọn 1 Sử dụng riêng/Sử dụng chung             |
| Địa chỉ             | text            | DiaChi         | 500        | N              | -                | -                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố      | combobox search | TinhThanhPho   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã           | combobox search | PhuongXa       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ cũ          | text            | DiaChiCu       | 500        | N              | -                | -                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ       | combobox search | TinhThanhPhoCu | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ       | combobox search | QuanHuyenCu    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ        | combobox search | PhuongXaCu     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

### Tàu biển
| Trường thông tin    | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tàu             | text    | TenTau           | 200        | N              | -                | -                  |       |
| Hô hiệu             | text    | HoHieu           | 50         | N              | -                | -                  |       |
| Loại tàu            | text    | LoaiTau          | 100        | N              | -                | -                  |       |
| Năm đóng tàu        | number  | NamDongTau       | 4          | N              | -                | -                  |       |
| Nơi đóng tàu        | text    | NoiDongTau       | 500        | N              | -                | -                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | 10         | N              | -                | -                  |       |
| Chiều rộng          | number  | ChieuRong        | 10         | N              | -                | -                  |       |
| Chiều cao mạn tàu   | number  | ChieuCaoManTau   | 10         | N              | -                | -                  |       |
| Mức nước tối đa     | number  | MucNuocToiDa     | 10         | N              | -                | -                  |       |
| Dung tích toàn phần | number  | DungTichToanPhan | 10         | N              | -                | -                  |       |
| Dung tích thực dụng | number  | DungTichThucDung | 10         | N              | -                | -                  |       |
| Trọng tải toàn phần | number  | TrongTaiToanPhan | 10         | N              | -                | -                  |       |
| Công suất máy chính | text    | CongSuatMayChinh | 100        | N              | -                | -                  |       |
| Cảng đăng ký        | text    | CangDangKy       | 200        | N              | -                | -                  |       |
| Ngày đăng ký        | date    | NgayDangKy       | -          | N              | -                | -                  |       |
| Cơ quan đăng kiểm   | text    | CoQuanDangKiem   | 200        | N              | -                | -                  |       |
| Số đăng ký          | text    | SoDangKy         | 100        | N              | -                | -                  |       |

### Tàu kéo - Ghe - Thuyền
| Trường thông tin    | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên phương tiện     | text    | TenPhuongTien    | 200        | N              | -                | -                  |       |
| Hô hiệu             | text    | HoHieu           | 50         | N              | -                | -                  |       |
| Loại phương tiện    | text    | LoaiPhuongTien   | 100        | N              | -                | -                  |       |
| Cấp phương tiện     | text    | CapPhuongTien    | 100        | N              | -                | -                  |       |
| Công dụng           | text    | CongDung         | 200        | N              | -                | -                  |       |
| Năm đóng            | number  | NamDong          | 4          | N              | -                | -                  |       |
| Nơi đóng            | text    | NoiDong          | 200        | N              | -                | -                  |       |
| Chiều dài thiết kế  | number  | ChieuDaiThietKe  | 10         | N              | -                | -                  |       |
| Chiều dài lớn nhất  | number  | ChieuDaiLonNhat  | 10         | N              | -                | -                  |       |
| Chiều rộng thiết kế | number  | ChieuRongThietKe | 10         | N              | -                | -                  |       |
| Chiều rộng lớn nhất | number  | ChieuRongLonNhat | 10         | N              | -                | -                  |       |
| Chiều cao mạn       | number  | ChieuCaoMan      | 10         | N              | -                | -                  |       |
| Chiều chìm          | number  | ChieuChim        | 10         | N              | -                | -                  |       |
| Mạn khô             | number  | ManKho           | 10         | N              | -                | -                  |       |
| Vật liệu vỏ         | text    | VatLieuVo        | 100        | N              | -                | -                  |       |
| Máy chính           | text    | MayChinh         | 200        | N              | -                | -                  |       |
| Trọng tải toàn phần | text    | TrongTaiToanPhan | 200        | N              | -                | -                  |       |

### Tàu cá
| Trường thông tin          | Control | Field            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:--------------------------|:--------|:-----------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tàu cá                | text    | TenTau           | 200        | N              | -                | -                  |       |
| Hô hiệu                   | text    | HoHieu           | 50         | N              | -                | -                  |       |
| Số đăng ký tàu cá         | text    | SoDangKy         | 100        | N              | -                | -                  |       |
| Loại tàu cá               | text    | LoaiTau          | 100        | N              | -                | -                  |       |
| Năm đóng tàu              | number  | NamDongTau       | 4          | N              | -                | -                  |       |
| Nơi đóng tàu              | text    | NoiDongTau       | 200        | N              | -                | -                  |       |
| Chiều dài lớn nhất (m)    | number  | ChieuDaiLonNhat  | 10         | N              | -                | -                  |       |
| Chiều rộng (m)            | number  | ChieuRong        | 10         | N              | -                | -                  |       |
| Chiều cao mạn tàu (m)     | number  | ChieuCaoManTau   | 10         | N              | -                | -                  |       |
| Mức nước tối đa (m)       | number  | MucNuocToiDa     | 10         | N              | -                | -                  |       |
| Dung tích toàn phần (GT)  | number  | DungTichToanPhan | 10         | N              | -                | -                  |       |
| Dung tích thực dụng (NT)  | number  | DungTichThucDung | 10         | N              | -                | -                  |       |
| Trọng tải toàn phần (DWT) | number  | TrongTaiToanPhan | 10         | N              | -                | -                  |       |
| Công suất máy chính       | text    | CongSuatMayChinh | 100        | N              | -                | -                  |       |
| Cảng đăng ký              | text    | CangDangKy       | 200        | N              | -                | -                  |       |
| Ngày đăng ký              | date    | NgayDangKy       | -          | N              | -                | -                  |       |
| Cơ quan đăng kiểm         | text    | CoQuanDangKiem   | 200        | N              | -                | -                  |       |


### Tàu bay
| Trường thông tin  | Control | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Số hiệu đăng ký   | text    | SoHieuDangKy   | 100        | N              | -                | -                  |       |
| Loại tàu bay      | text    | LoaiTauBay     | 100        | N              | -                | -                  |       |
| Kiểu loại tàu bay | text    | KieuLoaiTauBay | 100        | N              | -                | -                  |       |
| Nhà sản xuất      | text    | NhaSanXuat     | 200        | N              | -                | -                  |       |
| Quốc gia sản xuất | text    | QuocGiaSanXuat | 100        | N              | -                | -                  |       |
| Năm xuất xưởng    | number  | NamXuatXuong   | 4          | N              | -                | -                  |       |
| Số xuất xưởng     | text    | SoXuatXuong    | 100        | N              | -                | -                  |       |
| Kiểu loại động cơ | text    | KieuLoaiDongCo | 100        | N              | -                | -                  |       |

### Sổ tiết kiệm
| Trường  thông tin | Control | Field       | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:--------|:------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tài sản       | text    | TenTaiSan   | 200        | N              | -                | -                  |       |
| Số dư tiền gửi    | number  | SoDuTienGui | 100        | N              | -                | -                  |       |
| Kỳ hạn            | text    | KyHan       | 100        | N              | -                | -                  |       |
| Loại tiền         | select  | LoaiTien    | 50         | N              | -                | -                  |       |

### Trái phiếu
| Trường thông tin | Control | Field         | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:-----------------|:--------|:--------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên trái phiếu   | text    | TenTraiPhieu  | 200        | N              | -                | -                  |       |
| Số lượng         | number  | SoLuong       | 10         | N              | -                | -                  |       |
| Mệnh giá         | number  | MenhGia       | 100        | N              | -                | -                  |       |
| Tổng mệnh giá    | number  | TongMenhGia   | 100        | N              | -                | -                  |       |
| Kỳ hạn           | text    | KyHan         | 100        | N              | -                | -                  |       |
| Loại trái phiếu  | text    | LoaiTraiPhieu | 100        | N              | -                | -                  |       |

### Cổ phiếu
| Trường thông tin               | Control         | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                          |
|:-------------------------------|:----------------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:-----------------------------------------------|
| Mã số cổ phiếu                 | text            | MaSoCoPhieu    | 50         | N              | -                | -                  |                                                |
| Số lượng                       | number          | SoLuong        | 10          | N              | -                | -                  |                                                |
| Loại cổ phiếu                  | text            | LoaiCoPhieu    | 100        | N              | -                | -                  |                                                |
| Mệnh giá / cổ phiếu            | number          | MenhGia        | 10          | N              | -                | -                  |                                                |
| Tổng mệnh giá                  | number          | TongMenhGia    | 10          | N              | -                | -                  |                                                |
| Địa chỉ công ty phát hành      | text            | DiaChi         | 500        | N              | -                | -                  | Địa chỉ từ 1/7.                                |
| Tỉnh/Thành phố                 | combobox search | TinhThanhPho   | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố mới, **BR9.7** |
| Phường/Xã                      | combobox search | PhuongXa       | -          | N              | -                | -                  | Chọn từ danh mục phường/xã mới, **BR9.8**      |
| Địa chỉ công ty phát hành (cũ) | text            | DiaChiCu       | 500        | N              | -                | -                  | Địa chỉ trước 1/7.                             |
| Tỉnh/Thành cũ                  | combobox search | TinhThanhPhoCu | -          | N              | -                | -                  | Chọn từ danh mục tỉnh/thành phố cũ, **BR9.7**  |
| Quận/Huyện cũ                  | combobox search | QuanHuyenCu    | -          | N              | -                | -                  | Chọn từ danh mục quận/huyện cũ, **BR9.12**     |
| Phường/Xã cũ                   | combobox search | PhuongXaCu     | -          | N              | -                | -                  | Chọn từ danh mục phường/xã cũ, **BR9.8**       |

### Tài sản khác
| Trường thông tin  | Control  | Field          | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả |
|:------------------|:---------|:---------------|:-----------|:---------------|:-----------------|:-------------------|:------|
| Tên tài sản       | text     | TenTaiSan      | 200        | N              | -                | -                  |       |
| Thông tin tài sản | textarea | ThongTinTaiSan | 1000       | N              | -                | -                  |       |

## Chức năng
| Tên             | Loại       | Mô tả                                                  |
|:----------------|:-----------|:-------------------------------------------------------|
| Lưu             | Button     | Thực hiện kiểm tra thông tin và lưu **UC_TSGD_Create** |
| Hủy             | Button     | Mở popup xác nhận hủy                                  |
| Biểu tượng đóng | Button     | Đóng popup                                              |
