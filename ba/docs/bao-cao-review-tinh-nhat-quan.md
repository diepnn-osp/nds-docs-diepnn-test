# BÁO CÁO REVIEW TÍNH NHẤT QUÁN TÀI LIỆU BA

## Tổng quan
Báo cáo này tổng hợp các vấn đề về tính nhất quán và logic trong mô tả tài liệu BA hiện tại, dựa trên nguyên tắc trong file `ba/docs/nguyen-tac-review-tai-lieu.md`.

---

## 1. VẤN ĐỀ VỀ CẤU TRÚC SCREEN FILES (.md)

### 1.1. Thiếu section "Mô tả trường"

**Quy tắc**: Theo guideline, Screen files phải có section "Mô tả trường" để mô tả chi tiết các trường thông tin.

**Vấn đề**: TẤT CẢ các Screen files hiện tại đều THIẾU section "Mô tả trường".

**Danh sách files bị ảnh hưởng**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Update.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Delete.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_History.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Detail.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Lookup.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_List.md
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Create.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Create.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Detail.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_History.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Delete.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Update.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_List.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Lookup.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Create.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_List.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Detail.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Delete.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_History.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Update.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_ChungChi_History.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_ChinhSua.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_ThemMoi.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_XemDanhSach.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_TimKiem.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_ChinhSua.md

### 1.2. Thứ tự section không nhất quán

**Quy tắc**: Theo guideline, thứ tự section phải là:
1. Nguyên mẫu
2. Thành phần
3. Mô tả trường
4. Chức năng
5. Điều kiện tiên quyết

**Vấn đề**: Thứ tự hiện tại là:
1. Điều kiện tiên quyết (đặt đầu tiên thay vì cuối)
2. Nguyên mẫu
3. Thành phần
4. Chức năng (nếu có)

**Files bị ảnh hưởng**: TẤT CẢ Screen files

### 1.3. Section "Chức năng" không nhất quán về cấp độ heading

**Quy tắc**: Theo guideline và logic, "Chức năng" nên là subsection (###) của "Thành phần" (##), KHÔNG nên là section cùng cấp.

**Vấn đề**: Có sự không nhất quán:
- Một số files sử dụng `### Chức năng` (subsection - ĐÚNG)
- Một số files sử dụng `## Chức năng` (section ngang hàng - SAI)

**Files sử dụng `## Chức năng` (SAI - cần sửa thành ###)**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_History.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Create.md
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Detail.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Lookup.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Create.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Detail.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_History.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Update.md
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_ChungChi_History.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_Xoa.md
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_Xoa.md

---

## 2. VẤN ĐỀ VỀ TABLE COLUMNS

### 2.1. Cột trong bảng "Thành phần" không nhất quán

**Quy tắc**: Theo guideline, table trong section "Thành phần" phải có các cột:
- Trường thông tin
- Control
- Field
- Max length
- Bắt buộc (Y/N)
- Giá trị mặc định
- Cho phép sửa (Y/N)
- Mô tả

**Vấn đề**: 

#### 2.1.1. Các file thiếu cột so với quy định

**Ví dụ**: `SCR_Org_History.md` chỉ có: Trường thông tin, Control, Field, Bắt buộc (Y/N), Mô tả
- THIẾU: Max length, Giá trị mặc định, Cho phép sửa (Y/N)

**Ví dụ**: `SCR_CCV_Lookup.md` có cột "Bảng kết quả" với: Trường thông tin, Control, Field, Max length, Bắt buộc (Y/N), **Cho phép sửa (Y/N)**, Mô tả
- Không có cột "Giá trị mặc định" - hợp lý vì là bảng hiển thị kết quả, không phải form nhập liệu

#### 2.1.2. Bảng "Chức năng" không nhất quán về cột "Loại"

**Quy tắc**: Theo guideline, bảng Chức năng phải có: Tên, Loại, Mô tả

**Vấn đề phát hiện**:

**Files có header table bị sai format (không căn chỉnh đúng hoặc thiếu thông tin)**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_History.md: | Tên             | Loại   | Mô tả      |
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Create.md: | Tên                   | Loại   | Mô tả                                                                                                                                     |
- ba/[NDS-E-00056] Quản lý chữ ký số/6.screens/ChuKySo/SCR_Sign_Detail.md: | Tên         | Loại   | Mô tả                                                                                                                          |
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Lookup.md: | Tên        | Loại    | Mô tả                                                              |
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Create.md: | Tên     | Loại   | Mô tả                                                                  |
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Detail.md: | Tên                        | Loại   | Mô tả                                                                                  |
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_History.md: | Tên             | Loại   | Mô tả                                                                    |
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Update.md: | Tên     | Loại   | Mô tả                                                              |

---

## 3. VẤN ĐỀ VỀ REFERENCE FORMAT

### 3.1. Format reference đến Screen không nhất quán

**Quy tắc**: Khi reference đến màn hình khác, phải có format `(**SCR_TenChucNang**)`

**Vấn đề phát hiện**:

**Files có reference không đúng format**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Detail.md
  Line 49:| Chỉnh sửa | Button | Mở form chỉnh sửa tổ chức công chứng (SCR_Org_Update), chỉ hiển thị khi người dùng có quyền |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý đồng bộ danh mục dùng chung/4.usecases/[NDS-0-00577] Đồng bộ danh mục dân tộc/XemDanhSach/UC_DMDantoc_List.md
  Line 32:4. Hiển thị danh sách trên giao diện (SCR_DMDantoc_List).
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý đồng bộ danh mục dùng chung/4.usecases/[NDS-0-00209] Đồng bộ danh mục phường-xã mới/XemDanhSach/UC_DMPhuongxa_new_List.md
  Line 32:4. Hiển thị danh sách trên giao diện (SCR_DMPhuongxa_new_List).
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Giayto/SCR_BenLQ_XemDanhSach.md
  Line 35:| Thêm mới     | Button | Mở form thêm mới danh mục giấy tờ (SCR_Giayto_Themoi)                                                         |
  Line 36:| Sửa          | Button | Mở form Sửa thông tin danh mục giấy tờ (SCR_Giayto_ChinhSua)                                                  |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TTGiaodich/SCR_TTGiaodich_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục trạng thái giao dịch công chứng (SCR_TTGiaodich_Themoi)                                                     |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục trạng thái giao dịch công chứng (SCR_TTGiaodich_ChinhSua)                                              |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_LoaiGDCC/SCR_LoaiGDCC_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục Loại giao dịch công chứng (SCR_LoaiGDCC_Themoi)                                                    |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục Loại giao dịch công chứng (SCR_LoaiGDCC_ChinhSua)                                             |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Chucvu/SCR_Chucvu_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục chức vụ (SCR_Chucvu_Themoi)                                                     |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục chức vụ (SCR_Chucvu_ChinhSua)                                              |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_TenGDCC/SCR_TenGDCC_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục Tên giao dịch công chứng (SCR_TenGDCC_Themoi)                                                     |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục Tên giao dịch công chứng (SCR_TenGDCC_ChinhSua)                                              |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_Loaitaisan/SCR_Loaitaisan_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục loại tài sản (SCR_Loaitaisan_Themoi)                                                     |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục loại tài sản (SCR_Loaitaisan_ChinhSua)                                              |
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/6.screens/DM_BenLQ/SCR_BenLQ_XemDanhSach.md
  Line 34:| Thêm mới     | Button | Mở form thêm mới danh mục bên liên quan (SCR_BenLQ_Themoi)                                                    |
  Line 35:| Sửa          | Button | Mở form Sửa thông tin danh mục bên liên quan (SCR_BenLQ_ChinhSua)                                             |

### 3.2. Format reference đến Use Case không nhất quán

**Quy tắc**: Khi reference đến UC khác, phải có format `(**UC_TenChucNang**)`

**Vấn đề phát hiện**: Tương tự như SCR references

---

## 4. VẤN ĐỀ VỀ USE CASE FILES

### 4.1. Tiêu đề Use Case không nhất quán

**Quy tắc**: Use Case phải bắt đầu với `# Use Case: [Tên chức năng]`

**Vấn đề phát hiện**:

---

## 5. VẤN ĐỀ VỀ ACTIVITY DIAGRAM

### 5.1. Reference đến Screen trong Activity Diagram

**Quy tắc**: Khi chuyển hướng màn hình trong AD, phải có reference đến file SCR tương ứng

**Ví dụ từ AD_Org_Create.puml**: 
- Line 16: `:Chuyển hướng về danh sách\n(**SCR_Org_List**);`
- Line 19: `:Ở lại màn hình màn hình\n(**SCR_Org_Create**);`

**Vấn đề phát hiện**: Có lỗi chính tả "màn hình màn hình" (lặp từ)

**Files bị ảnh hưởng**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/4.usecases/[NDS-U-00021] ChinhSua/AD_Org_Update.puml
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/4.usecases/[NDS-U-00020] ThemMoi/AD_Org_Create.puml
- ba/[NDS-E-00056] Quản lý chữ ký số/4.usecases/[NDS-U-00060] DangKy/AD_Sign_Create.puml
- ba/[NDS-E-00056] Quản lý chữ ký số/4.usecases/[NDS-U-00061] ChinhSua/AD_Sign_Update.puml
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/4.usecases/[NDS-U-00051] ChinhSua/AD_CCV_Update.puml
- ba/[NDS-E-00046] Quản lý thông tin công chứng viên/4.usecases/[NDS-U-00050] ThemMoi/AD_CCV_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00207] Quản lý danh mục bên liên quan/ThemMoi/AD_DM_BenLQ_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00207] Quản lý danh mục bên liên quan/ChinhSua/AD_DM_BenLQ_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00204] Quản lý danh mục loại giao dịch công chứng/Themmoi/AD_DM_LoaiGDCC_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00204] Quản lý danh mục loại giao dịch công chứng/ChinhSua/AD_DM_LoaiGDCC_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00206] Quản lý danh mục loại tài sản giao dịch công chứng/ThemMoi/AD_DM_Loaitaisan_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00206] Quản lý danh mục loại tài sản giao dịch công chứng/ChinhSua/AD_DM_Loaitaisan_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00425] Quản lý danh mục trạng thái giao dịch công chứng/ThemMoi/AD_DM_TTGiaodich_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00425] Quản lý danh mục trạng thái giao dịch công chứng/ChinhSua/AD_DM_TTGiaodich_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00592] Quản lý danh mục chức vụ/ThemMoi/AD_DM_Chucvu_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00592] Quản lý danh mục chức vụ/ChinhSua/AD_DM_Chucvu_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00205] Quản lý danh mục tên giao dịch công chứng/ThemMoi/AD_DM_TenGDCC_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00205] Quản lý danh mục tên giao dịch công chứng/ChinhSua/AD_DM_TenGDCC_Update.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00210] Quản lý danh mục loại giấy tờ tùy thân/ThemMoi/AD_DM_Giayto_Create.puml
- ba/[NDS-E-00203] Quản trị hệ thống/[NDS-E-00203] Quản lý danh mục dùng chung/4.usecases/[NDS-U-00210] Quản lý danh mục loại giấy tờ tùy thân/ChinhSua/AD_DM_Giayto_Update.puml

---

## 6. VẤN ĐỀ KHÁC

### 6.1. Placeholder không nhất quán

**Quy tắc** (BR9.11): Mặc định placeholder luôn là "Nhập/Chọn + tên label". Nếu có thay đổi, chi tiết trong screen.

**Vấn đề phát hiện**:
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_Update.md có placeholder không theo quy tắc:
  20:| Địa chỉ                | text     | diaChiChiTiet    | 500        | Y              |                  | Y                  | Placeholder: Điền địa chỉ số nhà, tổ, thôn, xóm                                                                                                                                                                 |
- ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_List.md có placeholder không theo quy tắc:
  34:| Ô tìm kiếm chung            | Input           | Chỉ hiển thị khi người dùng có quyền tìm kiếm tổ chức công chứng, nhập tên tổ chức công chứng để tìm kiếm. Placeholder: "Điền tên tổ chức công chứng"                     |

### 6.2. Tên bảng/section trong "Thành phần" không nhất quán

**Vấn đề**: Các tên subsection trong "Thành phần" không nhất quán:
- "Bảng chính" 
- "Form nhập liệu"
- "Form tìm kiếm"
- "Bảng kết quả"
- "Bảng kết quả tra cứu"
- "Form tra cứu"
- "Popup xác nhận"
- "Form hiển thị thông tin"
- "Form chỉnh sửa thông tin"

**Đề xuất**: Cần chuẩn hóa tên các subsection theo mục đích sử dụng.

### 6.3. Mô tả trong bảng "Chức năng" không nhất quán về format reference

**Vấn đề**: 
- Một số dùng `(**UC_XXX**)` 
- Một số dùng `(UC_XXX)` (thiếu **)
- Một số dùng `(**SCR_XXX**)`

**Cần thống nhất**: Luôn dùng `(**UC_XXX**)` hoặc `(**SCR_XXX**)` với bold formatting.

---

## 7. TỔNG HỢP ĐỀ XUẤT SỬA CHỮA

### 7.1. Ưu tiên cao

1. **Thêm section "Mô tả trường"** vào TẤT CẢ Screen files
   - Mô tả rõ ràng, ngắn gọn
   - Có reference đến Business Rules khi cần
   - Có placeholder cho input fields

2. **Sửa thứ tự section** trong Screen files theo đúng guideline:
   - Nguyên mẫu (đầu tiên)
   - Thành phần
   - Mô tả trường
   - Chức năng
   - Điều kiện tiên quyết (cuối cùng)

3. **Thống nhất cấp độ heading "Chức năng"**:
   - Đổi `## Chức năng` thành `### Chức năng` (subsection của Thành phần)

4. **Sửa lỗi chính tả** trong Activity Diagrams:
   - "màn hình màn hình" → "màn hình"

### 7.2. Ưu tiên trung bình

5. **Chuẩn hóa table columns** trong section "Thành phần":
   - Đảm bảo đủ 8 cột theo quy định
   - Xem xét từng loại màn hình (danh sách, form nhập, popup) để quyết định cột nào cần thiết

6. **Chuẩn hóa format reference**:
   - UC reference: luôn dùng `(**UC_TenChucNang**)`
   - SCR reference: luôn dùng `(**SCR_TenChucNang**)`

7. **Sửa tiêu đề Use Case files**:
   - Đảm bảo format: `# Use Case: [Tên chức năng]`

### 7.3. Ưu tiên thấp

8. **Chuẩn hóa tên subsection** trong "Thành phần"
9. **Kiểm tra và sửa placeholder** theo BR9.11

---

## 8. KẾT LUẬN

### Số lượng vấn đề phát hiện:
- **Vấn đề nghiêm trọng**: 
  - 100% Screen files thiếu section "Mô tả trường"
  - 100% Screen files sai thứ tự section
  
- **Vấn đề cần sửa**: 
  - ~50% files có `## Chức năng` thay vì `### Chức năng`
  - Nhiều files có table columns không đầy đủ
  - Nhiều files có reference format không nhất quán

- **Vấn đề nhỏ**: 
  - Lỗi chính tả rải rác
  - Placeholder không theo quy tắc
  - Tên subsection không nhất quán

### Khuyến nghị:
1. Cập nhật guideline `ba/docs/nguyen-tac-review-tai-lieu.md` cho rõ ràng hơn về:
   - Thứ tự section (Điều kiện tiên quyết nên đặt đầu hay cuối?)
   - "Chức năng" là section hay subsection?
   
2. Tạo template chuẩn cho từng loại màn hình:
   - Template cho màn danh sách
   - Template cho màn form nhập/sửa
   - Template cho màn tra cứu
   - Template cho popup

3. Thực hiện sửa chữa theo thứ tự ưu tiên đã nêu trên.

