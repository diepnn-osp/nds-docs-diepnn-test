# Màn hình: Đăng ký chữ ký số
Form cho phép công chứng viên/nhân viên TCHNCC đăng ký chữ ký số mới.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền đăng ký chữ ký số.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=329-22035&t=qwdm1CHMm4I6o7Ud-1]
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=343-39909&t=qwdm1CHMm4I6o7Ud-1]

## Thành phần

### Thông tin đăng ký chữ ký số (ENT_ChuKySo)

<div style="overflow-x:auto">

| Trường thông tin | Control         | Field           | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                                                                                                                                                                                                                    |
|:-----------------|:----------------|:----------------|:-----------|:---------------|:-----------------|:-------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Công chứng viên  | combobox search | congChungVienId | -          | Y              | -                | Y                  | Hiển thị nếu loại chữ ký số = Cá nhân, chọn 1 từ danh sách công chứng viên của tổ chức công chứng. Danh sách hiển thị họ và tên                                                                                                                          |
| Loại chữ ký số   | combobox search | loaiChuKySo     | 10         | Y              | Cá nhân          | Y                  | Cá nhân / Tổ chức                                                                                                                                                                                                                                        |
| Nhà cung cấp     | combobox search | nhaCungCap      | 50         | Y              | -                | Y                  | Chọn nhà cung cấp dịch vụ từ danh sách: FPT-CA, VNPT-CA, CMC-CA, Viettel-CA, CA2, Safe-CA, SmartSugb, Newtel-CA, EFY-CA, TrustCA, NC-CA, LCS-CA, CMC-CA, EASY-CA, FASTCA, I-CA, Hilo-CA, ONE-CA, WINCA, MATBAO-CA, E-CA, MOBIFONECA, VNPAY-CA, IntrustCA |
| Số serial        | text            | soSerial        | 100        | Y              | -                | Y                  | Điền số serial                                                                                                                                                                                                                                           |
| Ngày hiệu lực    | date            | ngayHieuLuc     | 20         | Y              | -                | Y                  | Ngày bắt đầu hiệu lực của chữ ký số. Chọn từ lịch                                                                                                                                                                                                        |
| Ngày hết hạn     | date            | ngayHetHan      | 20         | Y              | -                | Y                  | Ngày hết hạn, chọn từ lịch phải lớn hơn hoặc bằng ngày hiệu lực. Hiển thị cảnh báo "Ngày hết hạn không hợp lệ" nếu không đúng quy tắc                                                                                                                    |
| Ghi chú          | textarea        | ghiChu          | 500        | N              | -                | Y                  | Ghi chú dùng                                                                                                                                                                                                                                             |
</div>

### Chức năng

<div style="overflow-x:auto">

| Tên                   | Loại   | Mô tả                                                                                                                                     |
|:----------------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------|
| Tải xuống mẫu đăng ký | button | Tải xuống mẫu đăng ký chữ ký số (=> Updating)                                                                                             |
| Tải lên File đính kèm | button | Upload file đính kèm đã ký số (định dạng PDF), tối đa 10mb. Hiển thị tên file bên cạnh sau khi tải thành công, có thể bấm vào để preview. |
| Trình duyệt           | Button | Kiểm tra hợp lệ và lưu vào ENT_ChuKySo với trạng thái = "Chờ duyệt"                                                                       |
| Lưu nháp              | Button | Lưu dữ liệu với trạng thái = "Mới tạo", không bắt buộc đầy đủ thông tin                                                                   |
| Hủy                   | Button | Hiển thị popup xác nhận hủy thao tác                                                                                                      |

</div>
