# Use Case: DM_Donvi_List (Xem danh sách danh mục đơn vị)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn xem danh sách danh mục đơn vị để quản lý thông tin.
- Với vai trò là **Chuyên viên cục BTTP**, tôi muốn xem danh sách danh mục đơn vị theo phân quyền để thực hiện công việc.
- Với vai trò là **Chuyên viên tại Sở Tư pháp**, tôi muốn xem danh sách danh mục đơn vị theo phân quyền để thực hiện công việc.


## Acceptance Criteria
- Hệ thống hiển thị danh sách danh mục đơn vị với các trường: STT, Mã danh mục, Loại danh mục, Tên danh mục, Trạng thái danh mục.
- Nếu số lượng bản ghi vượt quá giới hạn hiển thị, hệ thống phải cung cấp phân trang (10 bản ghi 1 trang).
- Từ danh sách, người dùng có thể thực hiện các thao tác tùy theo phân quyền:
  + Sửa (nếu có quyền)
  + Xóa (nếu có quyền)
  + Xem lịch sử (nếu có quyền)
  + Tải về file mẫu import
  + Import dữ liệu đơn vị (nếu có quyền)
  + Xuất danh sách đơn vị (nếu có quyền)
- Hiển thị thông báo lỗi nếu không tải được dữ liệu.
- Danh sách danh mục đơn vị hiển thị theo thứ tự thời gian cập nhật từ mới tới cũ nhất.
- Nếu có lỗi tải dữ liệu, hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Hệ thống cho phép tìm kiếm danh mục đơn vị (**SCR_DM_Donvi_Search**)
- Nếu không có danh mục đơn vị nào trong hệ thống, hiển thị thông báo "Không có dữ liệu danh mục đơn vị".

## Tác nhân chính
- Quản trị viên
- Chuyên viên cục BTTP
- Chuyên viên tại Sở Tư pháp

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập chức năng.

## Luồng chính
1. Người dùng mở menu chọn "Danh mục đơn vị".
2. Hệ thống kiểm tra quyền truy cập theo vai trò (Quản trị viên, Chuyên viên cục BTTP, Chuyên viên tại Sở Tư pháp).
3. Nếu có quyền truy cập
   - Hệ thống tải danh sách đơn vị.
   - Nếu tải dữ liệu thành công:
     + Nếu có dữ liệu:
       * Sắp xếp theo thời gian cập nhật (mới → cũ).
       * Nếu số lượng bản ghi lớn hơn 10, hệ thống thực hiện phân trang, 10 bản ghi mỗi trang.
       * Hiển thị danh sách với các trường: STT, Mã danh mục, Loại danh mục, Tên danh mục, Trạng thái danh mục.
     + Nếu không có dữ liệu:
       * Hiển thị thông báo "Không có dữ liệu danh mục đơn vị".
   - Nếu không tải được dữ liệu:
     + Hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
4. Nếu không có quyền truy cập
   - Hệ thống hiển thị thông báo "Không có quyền truy cập".
   - Ẩn menu "Quản lý danh mục đơn vị" khi người dùng đăng nhập.
5. Kết thúc.

## Luồng phụ/ Ngoại lệ
- Nếu có lỗi tải danh sách: hiển thị thông báo "Không tải được danh sách, vui lòng thử lại".
- Nếu không có dữ liệu: hiển thị "Không có dữ liệu danh mục đơn vị".
- Nếu không quyền truy cập: hiển thị "Không có quyền truy cập" và ẩn đi menu "Quản lý danh mục đơn vị".

## Hậu điều kiện
- Nếu thành công: Người dùng xem được danh sách danh mục đơn vị.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_DM_Donvi_List.puml]
- Form liên quan: [SCR_DM_Donvi_List.md]
- Entity liên quan: **ENT_DM_Donvi**
