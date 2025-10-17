# Use Case: DM_BenLQ_Delete (Xóa danh mục bên liên quan)

## User Story
- Với vai trò là Quản trị viên, tôi muốn xóa danh mục bên liên quan để có thể loại bỏ những bản ghi đã bị tạo nhầm.

## Acceptance Criteria
- Khi người dùng chọn Xóa danh mục bên liên quan, hệ thống phải hiển thị hộp thoại xác nhận với nội dung: “Bạn có chắc chắn muốn xóa danh mục bên liên quan này không?”.
- Hệ thống phải cung cấp hai lựa chọn: Xác nhận và Hủy.
- Nếu người dùng chọn Hủy, hệ thống đóng hộp thoại và danh mục bên liên quan không bị xóa.
- Nếu người dùng chọn Xác nhận, hệ thống phải kiểm tra điều kiện trước khi xóa.
- Nếu không còn ràng buộc dữ liệu, hệ thống xóa thành công và hiển thị thông báo "Xóa thành công danh mục bên liên quan".
- Hệ thống phải ghi nhận thông tin xóa danh mục bên liên quan vào nhật ký hệ thống. 
- Hệ thống phải cập nhật danh sách danh mục bên liên quan hiển thị trên **DM_BenLQ_List** sau khi xóa thành công.
- Chỉ có tài khoản Quản trị viên mới được xóa danh mục bên liên quan.

## Tác nhân chính
- Quản trị viên

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xóa danh mục bên liên quan.

## Luồng chính
1. Người dùng truy cập màn hình danh sách danh mục bên liên quan **DM_BenLQ_List**.  
2. Nếu người dùng có quyền xóa danh mục bên liên quan, hệ thống hiển thị nút xóa danh mục bên liên quan trên mỗi bản ghi
3. Người dùng nhấn nút "Xóa" trên bản ghi danh mục bên liên quan.  
4. Hệ thống hiển thị popup xác nhận xóa.  
5. Người dùng nhấn nút "Xác nhận".  
6. Hệ thống kiểm tra:  
   - Nếu Thông tin danh mục bên liên quan đang được sử dụng → Hệ thống đóng popup → Hiển thị cảnh báo lỗi "Không thể xóa danh mục bên liên quan. Danh mục đang được sử dụng" và không thực hiện xóa.  
   - Nếu không có ràng buộc → Xóa dữ liệu danh mục bên liên quan trong **DM_BenLQ**.  
7. Hệ thống đóng popup, hiển thị thông báo kết quả "Xóa thành công danh mục bên liên quan".
8. Hệ thống ghi nhận thông tin xóa danh mục bên liên quan vào nhật ký hệ thống.
9. Use case kết thúc. 

## Luồng phụ / ngoại lệ
- Người dùng nhấn **Hủy** hoặc biểu tượng đóng popup xác nhận xóa → Hệ thống đóng popup, use case kết thúc, không có thay đổi.  
- Nếu có lỗi hệ thống → Hiển thị thông báo lỗi chung, không xóa dữ liệu.  

## Hậu điều kiện
- Nếu thành công: Thông tin danh mục bên liên quan bị xóa và không còn trong danh sách.  
- Nếu thất bại hoặc hủy: Không có thay đổi nào trong hệ thống.

## Liên kết
- Activity Diagram: [AD_DM_BenLQ_Delete.puml]
- Form/Screen: [SCR_DM_BenLQ_Delete.md]
- Entity liên quan: **ENT_DM_BenLQ**
