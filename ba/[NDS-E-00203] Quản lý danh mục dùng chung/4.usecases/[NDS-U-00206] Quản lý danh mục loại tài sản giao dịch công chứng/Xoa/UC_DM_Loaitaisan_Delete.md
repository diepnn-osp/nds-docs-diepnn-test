# Use Case: DM_Loaitaisan_Delete (Xóa danh mục loại tài sản)

## User Story
- Với vai trò là Quản trị viên, tôi muốn xóa danh mục loại tài sản để có thể loại bỏ những bản ghi đã bị tạo nhầm.

## Acceptance Criteria
- Khi người dùng chọn Xóa danh mục loại tài sản, hệ thống phải hiển thị hộp thoại xác nhận với nội dung: “Bạn có chắc chắn muốn xóa danh mục loại tài sản này không?”.
- Hệ thống phải cung cấp hai lựa chọn: Xác nhận và Hủy.
- Nếu người dùng chọn Hủy, hệ thống đóng hộp thoại và danh mục loại tài sản không bị xóa.
- Nếu người dùng chọn Xác nhận, hệ thống phải kiểm tra điều kiện trước khi xóa.
- Nếu không còn ràng buộc dữ liệu, hệ thống xóa thành công và hiển thị thông báo "Xóa thành công danh mục loại tài sản".
- Hệ thống phải ghi nhận thông tin xóa danh mục loại tài sản vào nhật ký hệ thống. 
- Hệ thống phải cập nhật danh sách danh mục loại tài sản hiển thị trên **DM_Loaitaisan_List** sau khi xóa thành công.
- Chỉ có tài khoản Quản trị viên mới được xóa danh mục loại tài sản.

## Tác nhân chính
- Quản trị viên

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xóa danh mục loại tài sản.

## Luồng chính
1. Người dùng truy cập màn hình danh sách danh mục loại tài sản **DM_Loaitaisan_List**.  
2. Nếu người dùng có quyền xóa danh mục loại tài sản, hệ thống hiển thị nút xóa danh mục loại tài sản trên mỗi bản ghi
3. Người dùng nhấn nút "Xóa" trên bản ghi danh mục loại tài sản.  
4. Hệ thống hiển thị popup xác nhận xóa.  
5. Người dùng nhấn nút "Xác nhận".  
6. Hệ thống kiểm tra:  
   - Nếu Thông tin danh mục loại tài sản đang được sử dụng → Hệ thống đóng popup → Hiển thị cảnh báo lỗi "Không thể xóa danh mục loại tài sản. Danh mục đang được sử dụng" và không thực hiện xóa.  
   - Nếu không có ràng buộc → Xóa dữ liệu danh mục loại tài sản trong **DM_Loaitaisan**.  
7. Hệ thống đóng popup, hiển thị thông báo kết quả "Xóa thành công danh mục loại tài sản".
8. Hệ thống ghi nhận thông tin xóa danh mục loại tài sản vào nhật ký hệ thống.
9. Use case kết thúc. 

## Luồng phụ / ngoại lệ
- Người dùng nhấn **Hủy** hoặc biểu tượng đóng popup xác nhận xóa → Hệ thống đóng popup, use case kết thúc, không có thay đổi.  
- Nếu có lỗi hệ thống → Hiển thị thông báo lỗi chung, không xóa dữ liệu.  

## Hậu điều kiện
- Nếu thành công: Thông tin danh mục loại tài sản bị xóa và không còn trong danh sách.  
- Nếu thất bại hoặc hủy: Không có thay đổi nào trong hệ thống.

## Liên kết
- Activity Diagram: [AD_DM_Loaitaisan_Delete.puml]
- Form/Screen: [SCR_DM_Loaitaisan_Delete.md]
- Entity liên quan: **ENT_DM_Loaitaisan**
