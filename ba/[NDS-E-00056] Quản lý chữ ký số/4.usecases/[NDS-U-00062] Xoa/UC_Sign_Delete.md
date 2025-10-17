# Use Case: Xóa thông tin chữ ký số

## User Story
- Là **Nhân viên TCHNCC, Công chứng viên của TCNHCC**, tôi muốn xóa được thông tin chữ ký số, để có thể loại bỏ những bản ghi đã bị tạo nhầm.

## Acceptance criteria
- Khi người dùng chọn Xóa thông tin chữ ký số, hệ thống phải hiển thị hộp thoại xác nhận với nội dung: “Bạn có chắc chắn muốn xóa thông tin chữ ký số này không?”.
- Hệ thống phải cung cấp hai lựa chọn: Xác nhận và Hủy.
- Nếu người dùng chọn Hủy, hệ thống đóng hộp thoại và thông tin chữ ký số không bị xóa.
- Nếu người dùng chọn Xác nhận, hệ thống phải kiểm tra điều kiện trước khi xóa
- Nếu không còn ràng buộc dữ liệu, hệ thống xóa thành công và hiển thị thông báo "Xóa thành công thông tin thông tin chữ ký số".
- Hệ thống phải ghi nhận thông tin xóa thông tin chữ ký số vào nhật ký hệ thống. 
- Hệ thống phải cập nhật danh sách thông tin chữ ký số hiển thị trên **SCR_Sign_List** sau khi xóa thành công
- Nhân viên TCHNCC, công chứng viên chỉ có thể xóa đăng ký chữ ký số của tổ chức mình

## Tác nhân chính
- Nhân viên TCHNCC, Công chứng viên của TCNHCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Người dùng có quyền xóa thông tin chữ ký số

## Luồng chính
1. Người dùng truy cập màn hình danh sách thông tin chữ ký số **SCR_Sign_List**.  
2. Nếu người dùng có quyền xóa thông tin chữ ký số, hệ thống hiển thị nút xóa thông tin chữ ký số trên mỗi bản ghi
3. Người dùng nhấn nút "Xóa" trên bản ghi thông tin chữ ký số.  
3. Hệ thống hiển thị popup xác nhận xóa.  
4. Người dùng nhấn nút "Xác nhận".  
5. Hệ thống kiểm tra:  
   - Nếu thông tin chữ ký số đã được phê duyệt → Hệ thống đóng popup → Hiển thị cảnh báo lỗi "Không thể xóa thông tin chữ ký số đã được phê duyệt"  và không thực hiện xóa.  
   - Nếu không có ràng buộc → Xóa dữ liệu thông tin chữ ký số trong **ENT_ChuKySo**.  
6. Hệ thống đóng popup, hiển thị thông báo kết quả "Xóa thành công thông tin thông tin chữ ký số" .  
7. Use case kết thúc. 

## Luồng phụ / ngoại lệ
- Người dùng nhấn **Hủy** hoặc biểu tượng đóng popup xác nhận xóa → Hệ thống đóng popup, use case kết thúc, không có thay đổi.  
- Nếu có lỗi hệ thống → Hiển thị thông báo lỗi chung, không xóa dữ liệu.  
- Nếu chữ ký số không thuộc tổ chức công chứng của người dùng, hệ thống thông báo lỗi "Không thể xóa chữ ký số".
- Nếu chữ ký số có trạng thái khác "Mới tạo" hoặc "Chờ duyệt", hệ thống thông báo lỗi "Không thể xóa chữ ký số".

## Hậu điều kiện
- Nếu thành công: thông tin chữ ký số bị xóa và không còn trong danh sách.  
- Nếu thất bại hoặc hủy: Không có thay đổi nào trong hệ thống.

## Liên kết
- Activity Diagram: [AD_Sign_Delete.puml]
- Form/Screen: [SCR_Sign_List.md], [SCR_Sign_Delete.md]
- Entity liên quan: ENT_ChuKySo
