# QUY CHUẨN NGHIỆP VỤ DÙNG CHUNG HỆ THỐNG CƠ SỞ DỮ LIỆU CÔNG CHỨNG

Tài liệu này mô tả **các quy chuẩn nghiệp vụ chung** áp dụng cho toàn bộ các tính năng trong hệ thống.  

## BR1. Phân trang dữ liệu

| Nội dung          | Quy chuẩn nghiệp vụ                                                                                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cách hiển thị     | Danh sách dữ liệu được phân trang, mặc định 10 bản ghi/trang                                                                                                                  |
| Điều chỉnh        | Người dùng có thể thay đổi số bản ghi/trang: 10, 20, 50, 100, các thông tin hiển thị và điều hướng thay đổi theo số bản ghi/trang mà người dùng chọn                          |
| Điều hướng        | Có biểu tượng chuyển "Trang trước", "Trang sau". Hiển thị số trang hiện tại, mỗi số đại diện cho một trang dữ liệu. Người dùng có thể bấm vào để chuyển sang trang tương ứng. |
| Thông tin bổ sung | Luôn hiển thị tổng số bản ghi và tổng số trang. Hiển thị theo định dạng ""STT bản ghi đầu tiên của trang" - "STT bản ghi cuối cuối cùng trang" trên "tổng số lượng bản ghi""  |


## BR2. Hiển thị

| Nội dung                  | Quy chuẩn nghiệp vụ                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Thứ tự hiển thị danh sách | Mặc định thứ tự hiển thị là theo thời gian cập nhật từ mới tới cũ nhất. Nếu có thay đổi về thứ tự, sẽ mô tả trong Usecase                                                                 |
| Thông tin hiển thị        | Thông tin nào bị trống hoặc không có dữ liệu, hiện dấu "-". Thông tin nào dài quá 2 dòng, chỉ hiển thị 1 phần thông tin, hiển thị biểu tượng "...", hover vào hiển thị chi tiết           |
| Hiển thị ngày             | Hiển thị ngày theo định dạng dd/mm/yyyy HH:mm nếu là datetime hoặc dd/mm/yyyy nếu là date                                                                                                 |
| Hiển thị số tiền          | Hiển thị số tiền định sẽ dùng dấu chấm (.) để phân cách hàng nghìn, triệu, tỷ                                                                                                             |
| Hiển thị giá trị đo lường | Hiển thị giá trị đo lường sẽ dùng dấu chấm (.) để phân cách hàng nghìn, triệu, tỷ. Dùng dấu phẩy (,) phân cách thập phân. Hiển thị đơn vị đo lường sau giá trị, có khoảng trắng ngăn cách |
| Hiển thị địa chỉ gộp      | Hiển thị theo format "Địa chỉ chi tiết, phường/xã, tỉnh/thành phố"                                                                                                                        |
| Hiển thị gộp thông tin    | Hiển thị cách nhau bởi dấu "," thông tin nào không có bỏ trống, cắt dấu ","                                                                                                               |

## BR3. Tìm kiếm và lọc

| Nội dung       | Quy chuẩn nghiệp vụ                                                                                                                                                                                                              |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tìm kiếm chung | Có ô tìm kiếm theo từ khóa trên danh sách, những trường thông tin tìm kiếm sẽ quy định rõ trong usecase, tìm kiếm theo quy tắc: partial match (LIKE %keyword%), không phân biệt viết hoa viết thường, loại bỏ các ký tự đặc biệt |
| Ghi nhớ bộ lọc | Hệ thống tự động giữ lại bộ lọc sau khi người dùng chuyển trang hoặc tải lại                                                                                                                                                     |


## BR4. Xuất Excel

| Nội dung       | Quy chuẩn nghiệp vụ                                                                                |
|----------------|----------------------------------------------------------------------------------------------------|
| Định dạng file | Xuất ra file Excel (.xlsx)                                                                         |
| Tên file       | Tên theo Entity + ngày giờ xuất. Ví dụ: `DanhSachCongChungVien-20251002-0930.xlsx`                 |
| Dữ liệu xuất   | Dữ liệu xuất đúng theo điều kiện tìm kiếm, bộ lọc. Danh sách xuất ra giống với danh sách hiển thị. |
| Giới hạn       | Xuất tối đa 50.000 bản ghi trong một lần                                                           |
| Định dạng cột  | Ngày hiển thị `dd/mm/yyyy` hoặc `dd/mm/yyyy hh:mm`, số tiền có dấu phân cách hàng nghìn            |


## BR5. File đính kèm

| Nội dung           | Quy chuẩn nghiệp vụ                                                        |
|--------------------|----------------------------------------------------------------------------|
| Định dạng cho phép | Tùy từng trường hợp cụ thể sẽ mô tả trong chi tiết                         |
| Dung lượng         | Tối đa 10MB/file, nếu có thay đổi sẽ quy định rõ trong usecase hoặc screen |
| Xem file           | Đối với file PDF và file ảnh, click vào hiển thị màn hình preview          |


## BR6. Nhật ký cập nhật (Audit log)

| Nội dung           | Quy chuẩn nghiệp vụ                                                           |
|--------------------|-------------------------------------------------------------------------------|
| Lưu lại            | Tất cả thao tác thêm, sửa, xóa dữ liệu                                        |
| Thông tin bắt buộc | Người thực hiện, ngày giờ, trường thông tin thay đổi, giá trị cũ, giá trị mới |
| Truy xuất          | Người quản trị có thể xem lại lịch sử thay đổi theo từng bản ghi              |

## BR7. Phần đầu trang 
| Nội dung            | Quy chuẩn nghiệp vụ                                                                                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Thông tin tài khoản | Luôn hiển thị Họ và tên của người dùng + chức vụ. Hiển thị ảnh nếu có, nếu không sẽ hiển thị ảnh mặc định, click vào sẽ mở 2 lựa chọn: Quản lý tài khoản hoặc Đăng xuất |
| Biểu tượng menu     | Mặc định hiển thị menu chi tiết, bấm vào biểu tượng này sẽ đóng menu, thực hiện lại sẽ mở menu                                                                          |


## BR8. Menu/Danh mục chức năng hệ thống
| Nội dung                                                    | Quy chuẩn nghiệp vụ                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Trang chủ                                                   | Hiển thị khi người dùng có quyền, click vào mở trang chủ                                           |
| Quản lý giao dịch công chứng                                | Hiển thị khi người dùng có quyền, click vào hiển thị các mục con                                   |
| Quản lý giao dịch công chứng - Giao dịch công chứng giấy    | Hiển thị khi người dùng có quyền, click vào mở trang danh sách giao dịch công chứng giấy           |
| Quản lý giao dịch công chứng - Giao dịch công chứng điện tử | Hiển thị khi người dùng có quyền, click vào mở trang danh sách giao dịch công chứng điện tử        |
| Quản lý công chứng viên                                     | Hiển thị khi người dùng có quyền, click vào mở trang danh sách công chứng viên                     |
| Quản lý tổ chức công chứng                                  | Hiển thị khi người dùng có quyền, click vào mở trang danh sách tổ chức công chứng                  |
| Quản lý chữ ký số                                           | Hiển thị khi người dùng có quyền, click vào mở trang danh sách chữ ký số                           |
| Tra cứu                                                     | Hiển thị khi người dùng có quyền, click vào mở màn hình tra cứu. Mặc định chọn tab công chứng viên |

## BR9. Nhập thông tin
| STT | Nội dung                | Quy chuẩn nghiệp vụ                                                                                                                                                                                                                                     |
|-----|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Kiểm tra định dạng      | Nếu trường thông tin sai định dạng dữ liệu, hệ thống hiển thị cảnh báo ngay dưới ô là "Sai định dạng thông tin". Áp dụng cho toàn bộ form trên hệ thống                                                                                                 |
| 2   | Kiểm tra bắt buộc       | Nếu trường thông tin bắt buộc không được nhập khi bấm lưu, hệ thống hiển thị cảnh báo ngay dưới ô là "Nhập thông tin bắt buộc". Áp dụng cho toàn bộ form trên toàn hệ thống                                                                             |
| 3   | Ngày sinh, ngày cấp     | Chọn từ lịch, không cho phép chọn ngày lớn hơn ngày hiện tại                                                                                                                                                                                            |
| 4   | Số điện thoại           | Hệ thống cho phép nhập theo cả dạng `0xxxxxxxxx` hoặc `+84xxxxxxxxx`.Nếu nhập `+84` thì tự động chuyển thành `0`.Định dạng: Đủ 10 chữ số với di động, , không cho phép ký tự đặc biệt (`-`, khoảng trắng,…), với cố định 10-11 chữ số                   |
| 5   | Input lựa chọn/dropdown | Click vào, hệ thống hiển thị mặc định 5 giá trị nếu có nhiều hơn 5, có thể scroll xuống để hiển thị thêm. Hiển thị ô điền thông tin tìm kiếm, khi người dùng điền, hệ thống lọc giá trị để chọn theo từ đã điền. Áp dụng cho toàn bộ form trên hệ thống |
| 6   | Quy tắc click nút tab   | Gõ tab, hệ thống tự động chuyển từ field này sang field kế tiếp, từ trái sang phải, từ trên xuống . Nếu tab ở input lựa chọn, chọn ngay giá trị đầu tiên. áp dụng cho toàn bộ form trên hệ thống                                                        |
| 7   | Tỉnh/Thành phố          | Chọn tỉnh/thành phố từ danh mục hành chính quốc gia cũ/mới. Trường thông tin Tỉnh/Thành phố mới tự động cập nhật theo Tỉnh/thành phố cũ đã chọn                                                                                                         |
| 8   | Phường/Xã               | Chọn phường/xã từ danh mục hành chính quốc gia cũ/mới, danh sách hiển thị theo tỉnh thành đã chọn nếu là địa chỉ mới, danh sách cập nhật theo quận huyện đã chọn nếu là tỉnh thành cũ                                                                   |
| 9   | Email                   | Email luôn có cấu trúc TênNgườiDùng@TênMiền.Đuôi. Max length 255                                                                                                                                                                                        |
| 10  | Số giấy tờ cá nhân      | Cho phép điền không quá 12 ký tự, không có ký tự đặc biệt và khoảng trống                                                                                                                                                                               |
| 11  | Placeholder             | Mặc định placeholder luôn là Nhập/Chọn + tên label. Nếu có thay đổi, chi tiết trong screeen                                                                                                                                                             |
| 12  | Quận/Huyện              | Chọn quận/huyện từ danh mục hành chính quốc gia cũ, danh sách hiển thị theo tỉnh thành đã chọn                                                                                                                                                          |
| 13  | Số công chứng           | Công chứng điện tử: "Số/Năm/CCGDĐT", Công chứng giấy: "Số/Năm/CCGD"                                                                                                                                                                                     |


## BR10. Popup
| Nội dung       | Quy chuẩn nghiệp vụ                                                |
|----------------|--------------------------------------------------------------------|
| Nút "Đóng"     | Luôn hiển thị trong popup, click vào sẽ hủy thao tác và đóng popup |
| Biểu tượng "x" | Luôn hiển thị trong popup, click vào sẽ hủy thao tác và đóng popup |

## BR11. Button
| Nội dung | Quy chuẩn nghiệp vụ                                                            |
|----------|--------------------------------------------------------------------------------|
| Tooltips | Khi hover vào 1 biểu tượng/nút không có label, hệ thống hiện thị tooltip mô tả |

## BR12. Lưu thông tin

| STT | Nội dung  | Quy chuẩn nghiệp vụ                                                                                                                                           |
|-----|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | Họ và tên | Họ và tên người dùng được lưu thành 2 trường thông tin là HoDem và Ten. Tách chữ cuối cùng mà người dùng nhập để lưu vào Tên, các chữ còn lại lưu vào "HoDem" |

## BR13. Mật khẩu

| STT | Nội dung          | Quy chuẩn nghiệp vụ                                                                           |
|-----|-------------------|-----------------------------------------------------------------------------------------------|
| 1   | Mật khẩu mặc định | Khi tạo 1 tài khoản hoặc reset mật khẩu thì mật khẩu mặc định luôn là: "Csdl@btp2025"         |
| 2   | Quy tắc mật khẩu  | Độ dài tối thiểu: 8 ký tự .Phải chứa ít nhất: 1 chữ hoa, 1 chữ thường, 1 số, 1 ký tự đặc biệt |