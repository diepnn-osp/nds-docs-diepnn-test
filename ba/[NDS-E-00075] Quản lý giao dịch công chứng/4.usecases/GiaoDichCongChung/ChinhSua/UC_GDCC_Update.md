# Use Case: Chỉnh sửa giao dịch công chứng

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn chỉnh sửa giao dịch công chứng để thực hiện cập nhật các giao dịch bị sai thông tin do nhập nhầm.

## Acceptance Criteria
- Hệ thống kiểm tra quyền truy cập trước khi hiển thị form, nếu không có quyền thì hiển thị thông báo lỗi và không cho phép thao tác.
- Người dùng có thể thêm/xóa bên liên quan (**UC_BLQ_Create**/**UC_BLQ_Delete**).
- Người dùng có thể thêm/sửa/xóa người tham gia giao dịch vào bên liên quan (**UC_NTGGD_Create**/**UC_NTGGD_Update**/**UC_NTGGD_Delete**).
- Người dùng có thể thêm/sửa/xóa tài sản giao dịch (**UC_TSGD_Create**/**UC_TSGD_Update**/**UC_TSGD_Delete**).
- Người dùng có thể cập nhật các file đã tải lên
- Khi chọn "Lưu nháp": hệ thống kiểm tra logic các trường đã nhập, không yêu cầu đầy đủ, lưu giao dịch với trạng thái "Lưu nháp" và hiển thị thông báo thành công.
- Khi chọn "Lưu chính thức": hệ thống kiểm tra đầy đủ và logic, nếu hợp lệ thì lưu thông tin, đổi trạng thái thành "Lưu chính thức", hiển thị thông báo thành công và chuyển đến màn hình chi tiết (**SCR_GDCC_Detail**).
- Hệ thống ghi lại lịch sử cập nhật thông tin
- Khi dữ liệu không hợp lệ: hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.
- Khi chọn "Hủy": hệ thống hiển thị xác nhận, nếu đồng ý thì quay về màn hình chi tiết giao dịch (**SCR_GDCC_Detail**), nếu không thì giữ nguyên form.
- Văn bản hủy và phụ lục được mô tả trong **UC_HSSC_Revoke** và **UC_HSSC_Appendix**.
- Khi hệ thống phát sinh lỗi: hiển thị thông báo "Dữ liệu không hợp lệ, vui lòng kiểm tra lại" hoặc "Hệ thống phát sinh lỗi, vui lòng thử lại".
- Nếu giao dịch đã được lưu chính thức, người dùng không thể thực hiện Lưu nháp
- Nếu giao dịch đang lưu nháp, người dùng có thể chọn lưu nháp hoặc lưu chính thức

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Có quyền "Chỉnh sửa giao dịch công chứng".

## Luồng chính
1. Người dùng chọn chỉnh sửa 1 giao dịch công chứng.
2. Hệ thống kiểm tra quyền truy cập, nếu có quyền: hiển thị form chỉnh sửa giao dịch (**SCR_GDCC_Update**).
3. Người dùng cập nhật các thông tin chung của giao dịch.
4. Hệ thống hiển thị các trường bổ sung nếu người dùng chọn lại tên giao dịch (giống với khi thêm mới).
5. Người dùng thêm/xóa bên liên quan (**UC_BLQ_Create** / **UC_BLQ_Delete**).
6. Người dùng thêm/sửa/xóa người tham gia giao dịch vào bên liên quan (**UC_NTGGD_Create** / **UC_NTGGD_Update** / **UC_NTGGD_Delete**).
7. Người dùng thêm/sửa/xóa tài sản giao dịch (**UC_TSGD_Create** / **UC_TSGD_Update** / **UC_TSGD_Delete**).
8. Người dùng cập nhật tài liệu bằng cách xóa tài liệu cũ và tải lên file mới
9. Người dùng chọn **Lưu chính thức**
   - Hệ thống kiểm tra nghiệp vụ, các trường thông tin bắt buộc và logic dữ liệu.
   - Nếu hợp lệ:
      - Cập nhật toàn bộ thông tin đã chỉnh sửa vào giao dịch (**ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_TaiSan**, **ENT_ToChuc**).
      - Đổi trạng thái giao dịch thành "Lưu chính thức" nếu đang là lưu nháp.
      - Cập nhật lịch sử giao dịch (**ENT_LichSuCapNhat**).
      - Hiển thị thông báo "Cập nhật thông tin giao dịch công chứng thành công".
      - Chuyển đến màn hình chi tiết giao dịch (**SCR_GDCC_Detail**).   

## Luồng phụ 
- Người dùng chọn **Lưu nháp** (nếu trạng thái vẫn là "Lưu nháp"):
     - Hệ thống kiểm tra logic các trường đã nhập, không kiểm tra đầy đủ.
     - Nếu hợp lệ: cập nhật thông tin giao dịch, hiển thị thông báo "Đã lưu nháp giao dịch công chứng" (**ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_TaiSan**, **ENT_ToChuc**).
     - Cập nhật lịch sử giao dịch (**ENT_LichSuCapNhat**).
     - Mở màn hình chi tiết giao dịch công chứng (**SCR_GDCC_Detail**).
- Người dùng chọn **Hủy**:
   - Hiển thị xác nhận hủy thao tác.
   - Nếu đồng ý: hủy thao tác và quay về màn hình chi tiết giao dịch công chứng điện tử/giấy (**SCR_GDCC_Detail**).
   - Nếu không đồng ý: giữ nguyên form chỉnh sửa (**SCR_GDCC_Update**).

## Ngoại lệ
- Lưu chính thức: 
    - Nếu chưa điền đầy đủ thông tin bắt buộc, hiển thị thông báo lỗi và giữ nguyên form.
    - Nếu không có thông tin người tham gia giao dịch, thông báo lỗi "Chưa có thông tin người tham gia giao dịch, vui lòng kiểm tra lại"
    - Nếu không có thông tin tài sản giao dịch, thông báo lỗi "Chưa có thông tin tài sản giao dịch, vui lòng kiểm tra lại"
    - Công chứng điện tử: Nếu chưa tải lên văn bản công chứng điện tử: thông báo lỗi "Chưa có file văn bản công chứng điện tử, vui lòng kiểm tra lại"
    - Nếu số công chứng đã tồn tại trong danh sách giao dịch của tổ chức công chứng, thông báo "Số công chứng đã tồn tại, vui lòng kiểm tra lại"
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".
- Nếu lưu thất bại: hiển thị thông báo "Cập nhật giao dịch công chứng thất bại" và giữ nguyên form.
      
## Hậu điều kiện
- Nếu thành công: giao dịch công chứng được lưu vào hệ thống với trạng thái phù hợp.
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu giao dịch nào được ghi nhận.
- Nếu không có quyền: hiển thị thông báo lỗi "Bạn không có quyền thực hiện chức năng này" và kết thúc use case.

## Liên kết
- Activity Diagram: [AD_GDCC_Update.puml]
- Form liên quan: [SCR_GDCC_Create.md], [SCR_GDCC_Detail.md], [SCR_NTGGD_Create.md], [SCR_NTGGD_Delete.md], [SCR_NTGGD_Update.md], [SCR_TSGD_Create.md], [SCR_TSGD_Delete.md], [SCR_TSGD_Update.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_TaiSan**, **ENT_LichSuCapNhat**, **ENT_YeuCauChuyenQuyenSoHuuHoSo**, **ENT_TaiLieu**