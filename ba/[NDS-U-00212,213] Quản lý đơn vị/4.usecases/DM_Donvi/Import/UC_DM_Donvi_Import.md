# Use Case: DM_Donvi_Import (Import dữ liệu danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn import dữ liệu danh mục đơn vị từ file để nhập dữ liệu hàng loạt.
- Với vai trò là **Chuyên viên Cục BTTP**, tôi muốn import dữ liệu danh mục đơn vị từ file theo phạm vi quyền của mình để nhập dữ liệu hàng loạt.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn import dữ liệu danh mục đơn vị từ file theo đơn vị của mình để nhập dữ liệu hàng loạt.

## Acceptance Criteria
- Cho phép người dùng import dữ liệu danh mục đơn vị từ file theo mẫu được quy định.
- Kiểm tra định dạng file trước khi xử lý:
  + File phải có định dạng Excel (.xlsx, .xls)
  + Dung lượng file tối đa không vượt quá 10MB
  + File phải có cấu trúc đúng theo mẫu tải về (số cột, tên cột, thứ tự cột)
- Đọc và kiểm tra dữ liệu import theo các điều kiện:
  + Kiểm tra trùng lặp tên đơn vị
  + Tự sinh mã danh mục theo STT của dòng trong file import
  + Tên danh mục không được để trống
  + Danh mục của các đơn vị thuộc BTP, STP phải có loại đơn vị
- Import dữ liệu vào hệ thống tự động khi dữ liệu hợp lệ mà không cần xác nhận.
- Điều kiện bắt buộc cho cột "Loại đơn vị":
  + Nếu giá trị cột "Loại đơn vị" = "BTP" hoặc "STP" thì cột này KHÔNG được để trống
  + Nếu giá trị = "Khác" thì cột có thể để trống hoặc có giá trị
  - **Giá trị hợp lệ**: "BTP", "STP", "Khác"
  - **Thông báo lỗi**:
  + "Loại đơn vị không hợp lệ tại dòng [STT]" - nếu giá trị không thuộc danh sách cho phép
  + "Thiếu thông tin Loại đơn vị cho đơn vị BTP/STP tại dòng [STT]" - nếu để trống khi bắt buộc
- Hiển thị thông báo thành công khi import thành công.
- Hiển thị thông báo lỗi và tự động tải về file ghi chú từng bản ghi bị lỗi khi import thất bại.

## Tác nhân chính
- Quản trị viên
- Chuyên viên Cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền quản lý danh mục đơn vị.
- Người dùng đã sử dụng theo file mẫu được tải về tại danh sách danh mục đơn vị (**UC_DM_Donvi_Download_Temp**).
- Người dùng đã chuẩn bị file dữ liệu theo mẫu.

## Luồng chính
1. Người dùng truy cập chức năng "Danh sách danh mục đơn vị" (**SCR_DM_Donvi_List**).
2. Người dùng chọn thao tác "Import dữ liệu".
3. Người dùng chọn file import từ thiết bị.
4. Hệ thống kiểm tra định dạng file.
5. Nếu file đúng định dạng:
   - Hệ thống đọc dữ liệu từ file.
     - Kiểm tra cấu trúc file (số cột, tên cột)
     - Mã danh mục không trùng lặp (tự sinh theo format: DV_[STT])
     - Tên danh mục không được để trống
     - **Loại đơn vị: kiểm tra giá trị hợp lệ và tính bắt buộc theo quy tắc trên**
     - Trạng thái mặc định = Active nếu để trống
   - Hệ thống kiểm tra dữ liệu import.
   - Nếu dữ liệu hợp lệ:
     - Hệ thống import dữ liệu vào hệ thống.
     - Hệ thống hiển thị thông báo "Import dữ liệu thành công".
     - Chuyển hướng về danh sách (**SCR_DM_Donvi_List**).
6. Kết thúc use case.

## Luồng phụ / Ngoại lệ
- **File không đúng định dạng**:
  1. Hệ thống kiểm tra định dạng file.
  2. Nếu file không đúng định dạng:
  3. Hệ thống hiển thị thông báo "File không đúng định dạng".
  4. Người dùng ở lại màn hình import (**SCR_DM_Donvi_Import**).
- **Dữ liệu không hợp lệ**:
  1. Hệ thống kiểm tra dữ liệu import.
  2. Nếu dữ liệu không hợp lệ:
  3. Hệ thống thông báo lỗi dữ liệu import.
  4. Hệ thống tự động tải về thiết bị file ghi chú từng bản ghi bị lỗi với các lỗi cụ thể:
     - Kiểm tra trùng lặp tên đơn vị
     - Tên danh mục không được để trống
     - Loại đơn vị không hợp lệ (nếu giá trị không thuộc danh sách: BTP, STP, Khác)
     - Thiếu thông tin Loại đơn vị cho đơn vị BTP/STP
     - Email không đúng định dạng
     - Số điện thoại không đúng định dạng
  5. Người dùng ở lại màn hình import (**SCR_DM_Donvi_Import**).
- **Lỗi hệ thống khi import**:
  1. Hệ thống import dữ liệu vào hệ thống.
  2. Nếu import không thành công:
  3. Hệ thống hiển thị thông báo "Import dữ liệu thất bại".
  4. Người dùng ở lại màn hình import (**SCR_DM_Donvi_Import**).

## Hậu điều kiện
- **Nếu thành công**: Dữ liệu danh mục đơn vị được import vào hệ thống theo phạm vi quyền của người dùng.
- **Nếu thất bại**: Không có dữ liệu nào được import vào hệ thống.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_Import.puml]
- Form liên quan: [SCR_DM_Donvi_Import.md]
- Entity liên quan: **ENT_DM_Donvi**