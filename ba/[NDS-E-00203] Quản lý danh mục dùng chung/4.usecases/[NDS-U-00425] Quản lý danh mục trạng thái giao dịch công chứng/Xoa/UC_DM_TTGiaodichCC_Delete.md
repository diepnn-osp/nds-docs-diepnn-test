# Use Case: DM_TTGiaodichCC_Delete (Xóa danh mục trạng thái giao dịch công chứng)

## User Story
- Với vai trò là **Quản trị viên**, tôi muốn xóa danh mục trạng thái giao dịch công chứng để có thể loại bỏ những bản ghi đã bị tạo nhầm hoặc không còn sử dụng.

## Acceptance Criteria
- Khi người dùng chọn Xóa danh mục trạng thái giao dịch công chứng, hệ thống phải hiển thị hộp thoại xác nhận với nội dung: “Bạn có chắc chắn muốn xóa danh mục trạng thái giao dịch công chứng này không?”.
- Hệ thống phải cung cấp hai lựa chọn: Xác nhận và Hủy.
- Nếu người dùng chọn Hủy, hệ thống đóng hộp thoại và danh mục trạng thái giao dịch công chứng không bị xóa.
- Nếu người dùng chọn Xác nhận, hệ thống phải kiểm tra điều kiện trước khi xóa.
- Nếu không còn ràng buộc dữ liệu, hệ thống xóa thành công và hiển thị thông báo "Xóa thành công danh mục trạng thái giao dịch công chứng".
- Hệ thống phải ghi nhận thông tin xóa danh mục trạng thái giao dịch công chứng vào nhật ký hệ thống. 
- Hệ thống phải cập nhật danh sách danh mục trạng thái giao dịch công chứng hiển thị trên **DM_TTGiaodichCC_List** sau khi xóa thành công.
- Chỉ có tài khoản Quản trị viên mới được xóa danh mục trạng thái giao dịch công chứng.

## Tác nhân chính
- Quản trị viên

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xóa danh mục trạng thái giao dịch công chứng.

## Luồng chính
1. Người dùng truy cập màn hình danh sách danh mục trạng thái giao dịch công chứng **DM_TTGiaodichCC_List**.  
2. Nếu người dùng có quyền xóa danh mục trạng thái giao dịch công chứng, hệ thống hiển thị nút xóa danh mục trạng thái giao dịch công chứng trên mỗi bản ghi
3. Người dùng nhấn nút "Xóa" trên bản ghi danh mục trạng thái giao dịch công chứng.  
4. Hệ thống hiển thị popup xác nhận xóa.  
5. Người dùng nhấn nút "Xác nhận".  
6. Hệ thống kiểm tra:  
   - Nếu Thông tin danh mục trạng thái giao dịch công chứng đang được sử dụng → Hệ thống đóng popup → Hiển thị cảnh báo lỗi "Không thể xóa danh mục trạng thái giao dịch công chứng. Danh mục đang được sử dụng" và không thực hiện xóa.  
   - Nếu không có ràng buộc → Xóa dữ liệu danh mục trạng thái giao dịch công chứng trong **DM_TTGiaodichCC**.  
7. Hệ thống đóng popup, hiển thị thông báo kết quả "Xóa thành công danh mục trạng thái giao dịch công chứng".
8. Hệ thống ghi nhận thông tin xóa danh mục trạng thái giao dịch công chứng vào nhật ký hệ thống.
9. Use case kết thúc. 

## Luồng phụ / ngoại lệ
- Người dùng nhấn **Hủy** hoặc biểu tượng đóng popup xác nhận xóa → Hệ thống đóng popup, use case kết thúc, không có thay đổi.  
- Nếu có lỗi hệ thống → Hiển thị thông báo lỗi chung, không xóa dữ liệu.  

## Hậu điều kiện
- Nếu thành công: Thông tin danh mục trạng thái giao dịch công chứng bị xóa và không còn trong danh sách.  
- Nếu thất bại hoặc hủy: Không có thay đổi nào trong hệ thống.

## Liên kết
- Activity Diagram: [AD_DM_TTGiaodichCC_Delete.puml]
- Form/Screen: [SCR_DM_TTGiaodichCC_Delete.md]
- Entity liên quan: **ENT_DM_TTGiaodichCC**
