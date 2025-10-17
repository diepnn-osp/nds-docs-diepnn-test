# Màn hình: Danh sách tổ chức công chứng
Nơi tập trung để xem và quản lý tổ chức công chứng trên hệ thống.

## Điều kiện tiên quyết
- Người dùng đã đăng nhập và có quyền xem danh sách tổ chức công chứng.

## Nguyên mẫu
[https://www.figma.com/design/G1GnG3ecpubkOPJjxrEiRo/CSDL.CC_V1?node-id=218-22022&t=VeTqJhXDfKkDczGX-1]

## Thành phần

### Bảng chính
- Các cột trong bảng danh sách tổ chức công chứng hiển thị theo thứ tự bên dưới

<div style="overflow-x:auto">

| Trường thông tin       | Control | Field                                            | Max length | Bắt buộc (Y/N) | Giá trị mặc định | Cho phép sửa (Y/N) | Mô tả                                                               |
|:-----------------------|:--------|:-------------------------------------------------|:-----------|:---------------|:-----------------|:-------------------|:--------------------------------------------------------------------|
| STT                    | text    | -                                                | -          | -              |                  | -                  | Số thứ tự bản ghi                                                   |
| Tên tổ chức công chứng | text    | tenDonVi                                         | -          | -              |                  | -                  | Tên của tổ chức hành nghề công chứng                                |
| Sở Tư pháp             | text    | tenDonVi                                         | -          | -              |                  | -                  | Tên Sở Tư pháp quản lý (Chỉ hiển thị cột này cho người dùng cấp bộ) |
| Trưởng văn phòng       | text    | hoDem + ten                                      | -          | -              |                  | -                  | Tên công chứng viên lấy theo ID trưởng văn phòng công chứng         |
| Địa chỉ trụ sở         | text    | diaChiChiTiet + diaChiTinhThanh + diaChiPhuongXa | -          | -              |                  | -                  | Địa chỉ trụ sở hiện tại: Địa chỉ - Phường/xã - Tỉnh/Thành phố       |
| Trạng thái hoạt động   | text    | trangThai          | -          | -              |                  | -                  | Hiển thị trạng thái đã lưu. Nếu là "Đang hoạt động" thì label màu xanh, nếu "Giải thể" hoặc, "Chấm dứt hoạt động" hiện màu đỏ, còn lại màu vàng
| Chức năng              | icon    | -                  | -          | -              |                  | -                  | Hiển thị danh sách nút: Xem chi tiết, sửa, xóa, xem lịch sử (tùy theo phân quyền) |

</div> 

### Chức năng

<div style="overflow-x:auto">

| Tên                         | Loại            | Mô tả                                                                                                       |
|:----------------------------|:----------------|:------------------------------------------------------------------------------------------------------------|
| Ô tìm kiếm chung            | Input           | Nhập tên tổ chức công chứng để tìm kiếm. Placeholder: "Điền tên tổ chức công chứng"                         |
| Ô chọn tên Sở Tư pháp       | combobox search | Chọn 1 từ danh sách Sở Tư pháp                                                                              |
| Ô chọn trạng thái           | combobox search | Chọn 1 trạng thái từ danh sách trạng thái hoạt động của tổ chức công chứng (Giống với **SCR_Org_Create**)   |
| Biểu tượng tìm kiếm         | Button          | Bấm vào thực hiện tìm kiếm theo thông tin đã nhập và lựa chọn (**UC_Org_Search**)                           |
| Biểu tượng reset            | Button          | Bấm vào thực hiện reset kết quả tìm kiếm, hiển thị lại danh sách mặc định                                   |
| Nút xuất danh sách          | Button          | Hiển thị nếu có quyền, click sẽ xuất danh sách theo điều kiện đã tìm (UC_Org_Export)                        |
| Nút thêm mới                | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình thêm tổ chức công chứng (UC_Org_Create)                         |
| Biểu tượng xem chi tiết     | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình xem chi tiết tổ chức công chứng (UC_Org_Detail)                 |
| Biểu tượng sửa              | Button          | Hiển thị nếu có quyền, click sẽ mở màn hình chỉnh sửa tổ chức công chứng (UC_Org_Update)                    |
| Biểu tượng xóa              | Button          | Hiển thị nếu có quyền, click sẽ mở popup xác nhận xóa tổ chức công chứng (UC_Org_Delete)                    |
| Biểu tượng lịch sử cập nhật | Button          | Hiển thị nếu có quyền, click sẽ mở popup xem lịch sử cập nhật thông tin tổ chức công chứng (UC_Org_History) |

</div>
