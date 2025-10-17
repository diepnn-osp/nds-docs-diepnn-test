# Use Case: UC_Noti_Search (Tìm kiếm thông báo)

## User Story
- Với vai trò là **người dùng hệ thống**, tôi muốn tìm kiếm thông báo theo các tiêu chí nhanh và nâng cao để nhanh chóng lọc ra những thông báo cần xem hoặc xử lý.

## Acceptance Criteria
- Hỗ trợ tìm kiếm Mặc định: theo Tiêu đề và Người gửi.
- Hỗ trợ Tìm kiếm Nâng cao: bổ sung các tiêu chí Phạm vi gửi, Khoảng thời gian gửi (From - To), Trạng thái.
- Kết quả chỉ bao gồm các thông báo mà người dùng có quyền xem theo phân quyền.
- Nếu không tìm thấy bản ghi: hiển thị "Không có dữ liệu phù hợp".

## Tác nhân
- Công chứng viên
- Nhân viên TCHNCC
- Chuyên viên STP
- Lãnh đạo STP
- Lãnh đạo phòng HCBTTP tại STP
- hiennd-test
- Lãnh đạo Bộ Tư pháp
- Lãnh đạo Cục BTTP
- Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đã đăng nhập và có quyền truy cập danh sách thông báo **UC_Noti_List**.

## Luồng chính
1. Người dùng truy cập màn hình danh sách thông báo **UC_Noti_List**.
2. Người dùng nhập từ khóa vào ô tìm kiếm nhanh (theo **Tiêu đề** hoặc **Người gửi**) và nhấn Tìm kiếm.
3. Hệ thống thực hiện truy vấn theo tiêu chí người dùng nhập + phân quyền, trả về kết quả phân trang.
4. Nếu người dùng mở Tìm kiếm Nâng cao, họ có thể chọn thêm các tiêu chí: **Phạm vi gửi**, **Từ ngày - Đến ngày**, **Trạng thái**; sau đó bấm "Tìm kiếm" để thực hiện truy vấn nâng cao.
5. Hệ thống hiển thị danh sách kết quả, người dùng có thể xem chi tiết thông báo **UC_Noti_Detail**, chỉnh sửa **UC_Noti_Update** hoặc xóa **UC_Noti_Delete** theo phân quyền.
6. Kết thúc use case

## Luồng phụ / Ngoại lệ
- Người dùng mở Tìm kiếm Nâng cao, họ có thể chọn thêm các tiêu chí: **Phạm vi gửi**, **Từ ngày - Đến ngày**, **Trạng thái**; sau đó bấm "Tìm kiếm" để thực hiện truy vấn nâng cao


## Hậu điều kiện
- Nếu thành công: kết quả tìm kiếm hiển thị theo phân trang; người dùng có thể thao tác tiếp.
- Nếu thất bại: không trả về kết quả và hiển thị lỗi phù hợp.

## Related
- Use cases: **UC_Noti_List**, **UC_Noti_Detail**, **UC_Noti_Update**, **UC_Noti_Delete**
- Activity Diagram: **AD_Noti_Search.puml** 
- Screen/Form: **SCR_Noti_List.md**
- Entity: **ENT_Thongbao**


