# Use Case: DM_Donvi_Create (Thêm mới danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn thêm mới danh mục đơn vị.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn thêm mới danh mục đơn vị.
- Với vai trò là **Chuyên viên tại Sở Tư Pháp**, tôi muốn thêm mới danh mục đơn vị.

## Acceptance Criteria
- Hiển thị form thêm mới danh mục đơn vị khi người dùng chọn chức năng thêm mới.
- Người dùng nhập thông tin:
   - Mã danh mục **Tự sinh theo hệ thống, số tự nhiên tự tăng, disabel**
   - Tên danh mục
   - Loại đơn vị **Chọn loại: Sở Tư pháp/Đơn vị thuộc BTP/Đơn vị thuộc STP, Đơn vị cung cấp TTNC, TCHNCC**
- Kiểm tra dữ liệu hợp lệ (tên danh mục không được để trống, loại đơn vị được chọn).
- Lưu danh mục khi dữ liệu hợp lệ.
- Hiển thị thông báo "Thêm mới danh mục thành công".
- Chuyển hướng về trang danh sách danh mục sau khi lưu thành công.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư Pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị".
2. Người dùng chọn thêm mới danh mục.
3. Hệ thống hiển thị form nhập thông tin.
4. Người dùng nhập thông tin danh mục đơn vị, chọn loại đơn vị.
5. Người dùng chọn thao tác **Lưu thông tin**.
6. Hệ thống kiểm tra dữ liệu hợp lệ.
7. Nếu hợp lệ, hệ thống ghi nhận dữ liệu danh mục đơn vị.
8. Hệ thống kiểm tra ghi thành công:
   - Nếu thành công: Hiển thị thông báo "Thêm mới danh mục thành công".
   - Chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
9. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **Luồng hủy thao tác**:
  1. Người dùng chọn thao tác **Đóng**.
  2. Hệ thống xác nhận hủy thao tác.
  3. Nếu người dùng chọn "Đồng ý": Hủy thao tác và chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
  4. Nếu người dùng chọn "Không": Ở lại màn hình thêm mới (**SCR_DM_Donvi_Create**).
- **Kiểm tra dữ liệu không hợp lệ**:
  1. Người dùng chọn thao tác **Lưu thông tin** với dữ liệu không hợp lệ.
  2. Hệ thống hiển thị cảnh báo lỗi "Nhập thiếu thông tin bắt buộc".
  3. Người dùng ở lại màn hình thêm mới (**SCR_DM_Donvi_Create**).
- **Lỗi hệ thống khi ghi dữ liệu**:
  1. Khi ghi nhận dữ liệu xảy ra lỗi hệ thống.
  2. Hệ thống hiển thị thông báo lỗi hệ thống.
  3. Người dùng ở lại màn hình thêm mới (**SCR_DM_Donvi_Create**).

## Hậu điều kiện
- Nếu thành công: Danh mục đơn vị được lưu trong hệ thống.
- Nếu thất bại: Không có dữ liệu nào được thêm.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Create.puml]
- Form liên quan: [SCR_DM_Donvi_Create.md]
- Entity liên quan: **ENT_DM_Donvi**
