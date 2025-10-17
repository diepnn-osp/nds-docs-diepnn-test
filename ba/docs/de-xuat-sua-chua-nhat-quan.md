# ĐỀ XUẤT SỬA CHỮA CHI TIẾT

## Phần 1: Làm rõ Guideline

### Vấn đề cần làm rõ trong `nguyen-tac-review-tai-lieu.md`:

#### 1.1. Thứ tự section trong Screen files

**Hiện tại guideline ghi**:
- Cấu trúc file: "Phải có các section: Nguyên mẫu, Thành phần, Mô tả trường, Chức năng, Điều kiện tiên quyết"

**Nhưng thực tế**:
- TẤT CẢ files đang để "Điều kiện tiên quyết" ở đầu tiên
- Thiếu section "Mô tả trường"

**Đề xuất**: Cập nhật guideline rõ ràng về thứ tự:

**Phương án A** (đề xuất - thân thiện với người đọc):
```markdown
### Cấu trúc file

- Bắt đầu với `# Màn hình: [Tên màn hình]`
- Mô tả ngắn gọn về màn hình (tùy chọn)
- Thứ tự các section BẮT BUỘC:
  1. **Điều kiện tiên quyết** - Mô tả quyền truy cập và điều kiện cần thiết
  2. **Nguyên mẫu** - Link figma (nếu có)
  3. **Thành phần** - Mô tả các trường/bảng/form
  4. **Chức năng** - Mô tả các button/action (subsection của Thành phần)
```

**Lý do**: Người đọc nên biết điều kiện tiên quyết trước khi đọc chi tiết màn hình.

**Phương án B** (theo guideline hiện tại):
```markdown
- Thứ tự các section BẮT BUỘC:
  1. **Nguyên mẫu**
  2. **Thành phần**
  3. **Chức năng** (subsection của Thành phần)
  4. **Điều kiện tiên quyết**
```

#### 1.2. "Mô tả trường" vs "Thành phần"

**Vấn đề**: 
- Guideline yêu cầu có section "Mô tả trường" riêng biệt
- Nhưng thực tế, mô tả trường đang được đặt trong table của section "Thành phần" (cột "Mô tả")

**Đề xuất**: 

**Phương án A** (đề xuất - đơn giản hóa):
```markdown
### Thành phần

- Sử dụng table để mô tả các trường thông tin
- Table phải có các cột: Trường thông tin, Control, Field, Max length, Bắt buộc (Y/N), Giá trị mặc định, Cho phép sửa (Y/N), Mô tả
- Trong cột "Mô tả":
  - Mô tả rõ ràng, ngắn gọn
  - Có reference đến Business Rules khi cần: **BR9.7**
  - Có placeholder cho input fields: "Nhập/Chọn [tên trường]"
```

**Loại bỏ** section "Mô tả trường" riêng biệt vì đã có trong table.

**Phương án B** (giữ nguyên guideline - thêm section):
```markdown
### Mô tả trường

[Mô tả chung về các quy tắc nhập liệu cho màn hình này]

Ví dụ:
- Trường "Tên tổ chức": Nhập tên đầy đủ của tổ chức, không quá 250 ký tự (**BR9.1**)
- Trường "Email": Phải đúng định dạng email (**BR9.9**)
- Trường "Số điện thoại": Phải là số, 10 ký tự (**BR9.4**)
```

---

## Phần 2: Danh sách files cần sửa chữa ưu tiên cao

### 2.1. Files có `## Chức năng` cần đổi thành `### Chức năng`

**Tổng số: 22 files**

| STT | File | Thao tác |
|-----|------|----------|
| 1 | `ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/6.screens/SCR_Org_History.md` | Đổi `## Chức năng` → `### Chức năng` |
| 2 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Create.md` | Đổi `## Chức năng` → `### Chức năng` |
| 3 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Detail.md` | Đổi `## Chức năng` → `### Chức năng` |
| 4 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Delete.md` | Đổi `## Chức năng` → `### Chức năng` |
| 5 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_History.md` | Đổi `## Chức năng` → `### Chức năng` |
| 6 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_CCV_Update.md` | Đổi `## Chức năng` → `### Chức năng` |
| 7 | `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/6.screens/CongChungVien/SCR_ChungChi_History.md` | Đổi `## Chức năng` → `### Chức năng` |
| 8-22 | ... (xem báo cáo chi tiết) | Đổi `## Chức năng` → `### Chức năng` |

### 2.2. Lỗi chính tả trong Activity Diagrams

**File**: `ba/[NDS-E-00016] Quản lý tổ chức hành nghề công chứng/4.usecases/[NDS-U-00020] ThemMoi/AD_Org_Create.puml`

**Dòng 19 và 23**:
- Hiện tại: `:Ở lại màn hình màn hình\n(**SCR_Org_create**);`
- Sửa thành: `:Ở lại màn hình\n(**SCR_Org_Create**);`

**Lưu ý**: Còn sai tên file reference `SCR_Org_create` → `SCR_Org_Create` (chữ C viết hoa)

### 2.3. Tiêu đề Use Case không đúng format

**File**: `ba/[NDS-E-00046] Quản lý thông tin công chứng viên/4.usecases/[NDS-U-00590] TraCuu/UC_CCV_Lookup.md`

**Dòng 1**:
- Hiện tại: `# Use Case: tra cứu công chứng viên`
- Sửa thành: `# Use Case: Tra cứu công chứng viên` (viết hoa chữ cái đầu)

---

## Phần 3: Đề xuất cập nhật Guideline

### 3.1. Cập nhật file `ba/docs/nguyen-tac-review-tai-lieu.md`

**Section cần cập nhật**: "## Quy tắc cho Screen (.md)"

**Nội dung đề xuất**:

```markdown
## Quy tắc cho Screen (.md)

### Cấu trúc file

- Bắt đầu với `# Màn hình: [Tên màn hình]`
- Có thể có mô tả ngắn gọn về màn hình (1-2 dòng)
- Phải có các section theo thứ tự:
  1. **Điều kiện tiên quyết**
  2. **Nguyên mẫu**
  3. **Thành phần**

**Lưu ý về cấp độ heading**:
- "Điều kiện tiên quyết", "Nguyên mẫu", "Thành phần" là section cấp 2 (`##`)
- "Chức năng" là subsection cấp 3 (`###`) của "Thành phần" nếu có

### Điều kiện tiên quyết

- Phải mô tả rõ quyền truy cập và các điều kiện cần thiết
- Định dạng:
  ```markdown
  ## Điều kiện tiên quyết
  - Người dùng đã đăng nhập hệ thống.
  - Người dùng có quyền [tên quyền].
  ```

### Nguyên mẫu

- Gắn các link figma (có thể có hoặc chưa)
- Nếu chưa có, để `[]`

### Thành phần

- Sử dụng table để mô tả các trường thông tin
- Đặt tên subsection theo loại thành phần: "Form nhập liệu", "Bảng kết quả", "Popup xác nhận", v.v.
- Table phải có các cột:
  - **Bắt buộc**: Trường thông tin, Control, Field, Mô tả
  - **Tùy chọn** (theo từng loại màn hình):
    - Max length (với form nhập/sửa)
    - Bắt buộc (Y/N) (với form nhập/sửa)
    - Giá trị mặc định (với form nhập/sửa)
    - Cho phép sửa (Y/N) (với form sửa)

**Quy tắc cho cột "Mô tả"**:
- Rõ ràng, ngắn gọn
- Có reference đến Business Rules khi cần: **BR9.7**
- Có placeholder cho input fields: Mặc định "Nhập/Chọn [tên label]", nếu khác ghi rõ

### Chức năng

- Là subsection (`###`) của "Thành phần"
- Sử dụng table để mô tả các nút/chức năng
- Table phải có các cột: Tên, Loại, Mô tả
- Trong cột "Mô tả":
  - Khi reference đến Màn hình khác, phải có format `(**SCR_TenChucNang**)`
  - Khi reference đến Use Case, phải có format `(**UC_TenChucNang**)`
```

### 3.2. Thêm section "Ví dụ mẫu" vào guideline

```markdown
## Ví dụ mẫu Screen file

### Màn hình danh sách

[Xem file mẫu: SCR_Template_List.md]

### Màn hình form nhập/sửa

[Xem file mẫu: SCR_Template_Form.md]

### Màn hình tra cứu

[Xem file mẫu: SCR_Template_Lookup.md]

### Popup

[Xem file mẫu: SCR_Template_Popup.md]
```

---

## Phần 4: Kế hoạch thực hiện

### Giai đoạn 1: Cập nhật guideline (ưu tiên cao)

1. Cập nhật file `ba/docs/nguyen-tac-review-tai-lieu.md` theo đề xuất trên
2. Tạo các file template mẫu
3. Review và hoàn thiện guideline

### Giai đoạn 2: Sửa lỗi nghiêm trọng (ưu tiên cao)

1. Sửa 22 files có `## Chức năng` thành `### Chức năng`
2. Sửa lỗi chính tả trong Activity Diagrams
3. Sửa tiêu đề Use Case files

### Giai đoạn 3: Chuẩn hóa (ưu tiên trung bình)

1. Chuẩn hóa table columns theo từng loại màn hình
2. Chuẩn hóa format reference UC/SCR
3. Chuẩn hóa tên subsection trong "Thành phần"

### Giai đoạn 4: Hoàn thiện (ưu tiên thấp)

1. Kiểm tra và sửa placeholder theo BR9.11
2. Review toàn bộ tài liệu một lần nữa
3. Tạo checklist review cho tương lai

---

## Phần 5: Quyết định cần làm rõ

### Câu hỏi cho team:

1. **Thứ tự section trong Screen files**:
   - [ ] Phương án A: Điều kiện tiên quyết → Nguyên mẫu → Thành phần → Chức năng
   - [ ] Phương án B: Nguyên mẫu → Thành phần → Chức năng → Điều kiện tiên quyết

2. **Section "Mô tả trường"**:
   - [ ] Phương án A: Bỏ section riêng, tích hợp vào cột "Mô tả" trong table "Thành phần"
   - [ ] Phương án B: Giữ section riêng để mô tả quy tắc chung

3. **Table columns**:
   - [ ] Yêu cầu đủ 8 cột cho TẤT CẢ màn hình
   - [ ] Linh hoạt theo từng loại màn hình (danh sách, form, popup)

**Khuyến nghị**: 
- Câu hỏi 1: Chọn Phương án A (đang được áp dụng thực tế)
- Câu hỏi 2: Chọn Phương án A (đơn giản, tránh trùng lặp)
- Câu hỏi 3: Chọn linh hoạt theo loại màn hình

