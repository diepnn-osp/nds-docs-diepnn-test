# Use Case: Thêm mới giao dịch công chứng

## User Story
- Với vai trò là **Nhân viên/Công chứng viên TCHNCC**, tôi muốn thêm mới giao dịch công chứng để thực hiện lưu trữ thông tin và đảm bảo giao dịch được tạo mới đầy đủ, chính xác.

## Acceptance Criteria
- Hệ thống kiểm tra quyền truy cập trước khi hiển thị form, nếu không có quyền thì hiển thị thông báo lỗi và không cho phép thao tác.
- Khi người dùng chọn tên giao dịch là "ủy quyền", hệ thống yêu cầu điền thông tin thời hạn ủy quyền.
- Khi người dùng chọn tên giao dịch là "thế chấp", hệ thống yêu cầu điền thông tin giải chấp (thời hạn giải chấp, ngày giải chấp, trạng thái giải chấp, ghi chú giải chấp).
- Người dùng có thể thêm/xóa bên liên quan (**UC_BLQ_Create**/**UC_BLQ_Delete**).
- Người dùng có thể thêm/sửa/xóa người tham gia giao dịch vào bên liên quan (**UC_NTGGD_Create**/**UC_NTGGD_Update**/**UC_NTGGD_Delete**).
- Người dùng có thể thêm/sửa/xóa tài sản giao dịch (**UC_TSGD_Create**/**UC_TSGD_Update**/**UC_TSGD_Delete**).
- Nếu là công chứng điện tử: người dùng tải lên văn bản công chứng điện tử, văn bản sửa lỗi kỹ thuật (nếu có) và các giấy tờ khác.
- Nếu là công chứng giấy: người dùng tải lên văn bản công chứng điện tử (nếu có) và hồ sơ lưu trữ điện tử.
- Khi chọn "Lưu nháp": hệ thống kiểm tra logic các trường đã nhập, không yêu cầu đầy đủ, lưu giao dịch với trạng thái "Lưu nháp" và hiển thị thông báo thành công.
- Khi chọn "Lưu chính thức": hệ thống kiểm tra đầy đủ và logic, nếu hợp lệ thì lưu thông tin, đổi trạng thái thành "Lưu chính thức", hiển thị thông báo thành công và chuyển đến màn hình chi tiết (**SCR_GDCC_Detail**).
- Khi dữ liệu không hợp lệ: hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.
- Khi chọn "Hủy": hệ thống hiển thị xác nhận, nếu đồng ý thì quay về danh sách giao dịch (**SCR_GDCC_List**), nếu không thì giữ nguyên form.
- Văn bản hủy và tạo phụ lục được mô tả trong **UC_GDCC_Revoke** và **UC_GDCC_Appendix**.
- Khi hệ thống phát sinh lỗi: hiển thị thông báo "Dữ liệu không hợp lệ, vui lòng kiểm tra lại" hoặc "Hệ thống phát sinh lỗi, vui lòng thử lại".

## Tác nhân chính
- Nhân viên/Công chứng viên TCHNCC

## Tiền điều kiện
- Người dùng đã đăng nhập hệ thống.
- Có quyền "Thêm mới giao dịch công chứng".

## Luồng chính
1. Người dùng chọn chức năng **Thêm mới** giao dịch công chứng từ màn hình danh sách giao dịch **SCR_GDCC_List**.
2. Hệ thống kiểm tra quyền truy cập, nếu có quyền: hiển thị form thêm mới giao dịch (**SCR_GDCC_Create**).
3. Người dùng nhập thông tin chung của giao dịch.
4. Hệ thống hiển thị các trường bổ sung theo tên giao dịch:
   - Nếu là **ủy quyền**: hiển thị trường thời hạn ủy quyền.
   - Nếu là **thế chấp**: hiển thị trường thông tin giải chấp.
     - Nếu trạng thái là "Đã giải chấp": yêu cầu nhập thông tin giải chấp chi tiết.
   - Nếu là **văn bản hủy** hoặc **phụ lục**: tham chiếu (**AD_GDCC_Revoke**, **AD_GDCC_Appendix**).
5. Người dùng thêm/xóa bên liên quan (**UC_BLQ_Create / UC_BLQ_Delete**).
6. Người dùng thêm/sửa/xóa người tham gia giao dịch vào bên liên quan (**UC_NTGGD_Create** / **UC_NTGGD_Update** / **UC_NTGGD_Delete**).
7. Người dùng thêm/sửa/xóa tài sản giao dịch (**UC_TSGD_Create** / **UC_TSGD_Update** / **UC_TSGD_Delete**).
8. Người dùng tải lên tài liệu:
   - Nếu là công chứng điện tử: văn bản công chứng điện tử, văn bản sửa lỗi kỹ thuật (nếu có) và giấy tờ khác.
   - Nếu là công chứng giấy: văn bản công chứng điện tử (nếu có), hồ sơ lưu trữ điện tử (nếu có) và các file thành phần hồ sơ khác (nếu có).
9. Người dùng chọn **Lưu chính thức**
   - Hệ thống kiểm tra các trường thông tin bắt buộc, logic dữ liệu và nghiệp vụ.
   - Nếu hợp lệ:
      - Đổi trạng thái giao dịch thành "Lưu chính thức".
      - Cập nhật thông tin tổ chức lưu trữ = Tổ chức công chứng đang tạo lập hồ sơ.
      - Lưu toàn bộ thông tin giao dịch vào các entity liên quan (**ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_TaiSan**, **ENT_ToChuc**).
      - Cập nhật lịch sử giao dịch (**ENT_LichSuCapNhat**).
      - Hiển thị thông báo "Thêm mới giao dịch công chứng thành công".
      - Chuyển đến màn hình chi tiết giao dịch (**SCR_GDCC_Detail**).   

## Luồng phụ 
- Người dùng chọn **Lưu nháp**:
     - Hệ thống kiểm tra logic các trường đã nhập, không kiểm tra thông tin bắt buộc.
     - Nếu hợp lệ: 
        - Lưu giao dịch với trạng thái "Lưu nháp" (**ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_TaiSan**, **ENT_ToChuc**).
        - Cập nhật lịch sử giao dịch (**ENT_LichSuCapNhat**). 
        - Hiển thị thông báo "Đã lưu nháp giao dịch công chứng".
        - Mở màn hình chi tiết giao dịch công chứng (**SCR_GDCC_Detail**).
- Người dùng chọn **Hủy**:
   - Hiển thị xác nhận hủy thao tác.
   - Nếu đồng ý: hủy thao tác và quay về danh sách giao dịch công chứng điện tử/giấy (**SCR_GDCC_List**).
   - Nếu không đồng ý: giữ nguyên form thêm mới (**SCR_GDCC_Create**).

## Ngoại lệ
- Lưu chính thức: 
    - Nếu chưa điền đầy đủ thông tin bắt buộc, hiển thị thông báo lỗi và giữ nguyên form.
    - Nếu không có thông tin người tham gia giao dịch, thông báo lỗi "Chưa có thông tin người tham gia giao dịch, vui lòng kiểm tra lại"
    - Nếu không có thông tin tài sản giao dịch, thông báo lỗi "Chưa có thông tin tài sản giao dịch, vui lòng kiểm tra lại"
    - Công chứng điện tử: Nếu chưa tải lên văn bản công chứng điện tử: thông báo lỗi "Chưa có file văn bản công chứng điện tử, vui lòng kiểm tra lại"
    - Nếu số công chứng đã tồn tại trong danh sách giao dịch của tổ chức công chứng, thông báo "Số công chứng đã tồn tại, vui lòng kiểm tra lại"
- Lỗi dữ liệu không hợp lệ: Hiển thị thông báo "Dữ liệu không hợp lệ, vui lòng kiểm tra lại".
- Lỗi hệ thống: Hiển thị thông báo "Hệ thống phát sinh lỗi, vui lòng thử lại".
- Nếu lưu thất bại: hiển thị thông báo "Thêm mới giao dịch công chứng thất bại" và giữ nguyên form.
   
## Hậu điều kiện
- Nếu thành công: giao dịch công chứng được lưu vào hệ thống với trạng thái phù hợp.
- Nếu thất bại hoặc hủy thao tác: không có dữ liệu giao dịch nào được ghi nhận.
- Nếu không có quyền: hiển thị thông báo lỗi "Bạn không có quyền thực hiện chức năng này" và kết thúc use case.

## Liên kết
- Activity Diagram: [AD_GDCC_Create.puml]
- Form liên quan: [SCR_GDCC_Create.md], [SCR_GDCC_Detail.md], [SCR_NTGGD_Create.md], [SCR_NTGGD_Delete.md], [SCR_NTGGD_Update.md], [SCR_TSGD_Create.md], [SCR_TSGD_Delete.md], [SCR_TSGD_Update.md]
- Entity liên quan: **ENT_HoSoCongChung**, **ENT_CaNhan**, **ENT_ToChuc**, **ENT_TaiSan**, **ENT_TaiLieu**, **ENT_LichSuCapNhat**, **ENT_YeuCauChuyenQuyenSoHuuHoSo**