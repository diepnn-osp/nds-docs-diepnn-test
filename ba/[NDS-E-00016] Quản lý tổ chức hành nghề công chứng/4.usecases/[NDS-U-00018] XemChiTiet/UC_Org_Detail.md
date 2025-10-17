# Use Case: Xem chi tiết thông tin tổ chức công chứng (UC_Org_Detail)

## User Story
- Là **Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP**, tôi muốn xem được chi tiết thông tin của tổ chức công chứng thuộc Sở Tư pháp để nắm rõ hồ sơ và tình trạng hoạt động của họ
- Là **Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP**, tôi muốn xem được chi tiết thông tin của tổ chức công chứng trên toàn bộ hệ thống để nắm rõ hồ sơ và tình trạng hoạt động của họ

## Acceptance criteria
- Hệ thống hiển thị đầy đủ thông tin chi tiết của tổ chức công chứng được chọn từ danh sách.
- Các trường thông tin bao gồm: 
    - Tên tổ chức công chứng 
    - Sở Tư pháp quản lý
    - Địa chỉ
    - Tỉnh/Thành phố
    - Phường/Xã 
    - Số điện thoại
    - Mã số thuế
    - Trưởng văn phòng
    - Trạng thái hoạt động 
    - Danh sách công chứng viên: Họ và tên, số thẻ, chức vụ (Công chứng viên/trưởng văn phòng), trạng thái
- Người dùng có thể quay lại danh sách tổ chức công chứng.
- Nếu không tìm thấy dữ liệu, hệ thống hiển thị thông báo "Không tìm thấy thông tin tổ chức công chứng".
- Nếu có lỗi hệ thống, hiển thị thông báo lỗi.  

## Tác nhân chính
- Chuyên viên STP, Lãnh đạo STP, Lãnh đạo phòng HCBTTP tại STP, Lãnh đạo Bộ Tư pháp, Lãnh đạo Cục BTTP, Chuyên viên Cục BTTP

## Tiền điều kiện
- Người dùng đăng nhập hệ thống.
- Người dùng có quyền xem chi tiết thông tin tổ chức công chứng

## Luồng chính
1. Người dùng truy cập thành công màn hình danh sách tổ chức công chứng
2. Người dùng truy cập trang chi tiết thông tin tổ chức công chứng bằng cách click vào "Họ và tên" tổ chức công chứng hoặc biểu tượng xem chi tiết
3. Hệ thống truy vấn thông tin chi tiết tổ chức công chứng theo ID (**ENT_ToChucCongChung**).
4. Hệ thống hiển thị màn hình chi tiết tổ chức công chứng (**SCR_Org_Detail**) bao gồm các thông tin
    - Tên tổ chức công chứng 
    - Sở Tư pháp quản lý
    - Địa chỉ
    - Tỉnh/Thành phố
    - Phường/Xã 
    - Số điện thoại
    - Mã số thuế
    - Trưởng văn phòng: Họ và tên
    - Trạng thái hoạt động 
    - Danh sách công chứng viên: Họ và tên, số thẻ, chức vụ (Công chứng viên/trưởng văn phòng), trạng thái
5. Hệ thống hiển thị các nút chức năng.
- Biểu tượng quay lại và nút đóng => Bấm vào chuyển về màn hình danh sách tổ chức công chứng (**SCR_Org_List**)
- Chỉnh sửa => Mô tả trong use case chỉnh sửa thông tin tổ chức công chứng (**UC_Org_Update**) và màn hình (**SCR_Org_Detail**)
6. Kết thúc Use case

## Luồng phụ / ngoại lệ
- Không có dữ liệu: Hiển thị "Không tìm thấy thông tin tổ chức công chứng".
- Lỗi hệ thống: Hiển thị thông báo "Không tải được thông tin, vui lòng thử lại".

## Hậu điều kiện
- Nếu thành công: Người dùng xem được thông tin chi tiết tổ chức công chứng.
- Nếu thất bại: Không hiển thị dữ liệu, hoặc hiển thị thông báo lỗi.

## Liên kết
- Activity Diagram: [AD_Org_Detail.puml]
- Form/Screen: [SCR_Org_Detail.md]
- Entity liên quan: **ENT_ToChucCongChung**
