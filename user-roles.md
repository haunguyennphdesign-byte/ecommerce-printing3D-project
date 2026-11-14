# Vai trò người dùng và danh sách chức năng – E-Pack

Tài liệu mô tả các nhóm người dùng và danh sách chức năng của nền tảng bao bì B2B E-Pack.

## 1. Vai trò người dùng

| Vai trò | Mô tả |
|---------|-------|
| Khách chưa đăng nhập | Người truy cập chưa có tài khoản hoặc chưa đăng nhập. Xem sản phẩm, nội dung hướng dẫn và dùng thử cấu hình sản phẩm. |
| Khách hàng | Doanh nghiệp/cá nhân có tài khoản, thực hiện cấu hình, tải thiết kế, xem trước, yêu cầu báo giá, đặt và theo dõi đơn hàng. |
| Nhà cung cấp | Xưởng in/đối tác sản xuất, tiếp nhận yêu cầu, thẩm định file thiết kế, gửi báo giá chính thức và xử lý đơn hàng. |
| Quản trị viên (Admin) | Quản lý danh mục, thông số sản phẩm, bảng giá, hồ sơ đối tác và toàn bộ hệ thống. |

> **Lưu ý:** Tùy đề tài, nhóm có thể bổ sung nhân viên bán hàng, nhân viên xử lý đơn hoặc các vai trò khác.

## 2. Danh sách chức năng

| Mã | Chức năng | Người sử dụng | Mức độ ưu tiên |
|----|-----------|---------------|----------------|
| F01 | **Xem danh sách và chi tiết sản phẩm:** Hiển thị thông tin 4 nhóm sản phẩm cốt lõi (hộp giấy, túi giấy, tube giấy, nhãn in) và nội dung hướng dẫn. | Khách chưa đăng nhập, Khách hàng | Bắt buộc |
| F02 | **Đăng ký, đăng nhập & phân quyền tài khoản:** Xác thực người dùng và phân tách giao diện theo 3 nhóm (Khách hàng, Nhà cung cấp, Admin). | Khách hàng, Nhà cung cấp, Quản trị viên | Bắt buộc |
| F03 | **Cấu hình sản phẩm (Product Configurator):** Cho phép lựa chọn kích thước, kiểu dáng, chất liệu, định lượng giấy, số lượng, phương pháp in và gia công hoàn thiện. | Khách chưa đăng nhập, Khách hàng đã đăng nhập | Bắt buộc hoặc theo phạm vi |
| F04 | **Tải lên và kiểm tra file thiết kế (Preflight cơ bản):** Cho phép tải file (PNG, JPG, SVG, PDF, AI) và tự động kiểm tra định dạng, dung lượng, độ phân giải (dpi), tỷ lệ khung. | Khách hàng | Bắt buộc |
| F05 | **Xem trước sản phẩm 2D/3D (Preview 2D/3D):** Hiển thị bản thiết kế được ghép lên mô hình bao bì ở chế độ 2D (vùng an toàn) và 3D (xoay, phóng to/thu nhỏ). | Khách hàng | Bắt buộc |
| F06 | **Tính giá dự kiến & Gửi yêu cầu báo giá (RFQ):** Tự động ước tính chi phí theo cấu hình đã chọn và cho phép gửi yêu cầu báo giá đến nhà cung cấp. | Khách hàng | Bắt buộc |
| F07 | **Quản lý yêu cầu & Báo giá chính thức:** Tiếp nhận thông tin cấu hình, thẩm định file thiết kế và gửi báo giá chính thức lại cho khách hàng. | Nhà cung cấp | Bắt buộc |
| F08 | **Xác nhận, theo dõi đơn hàng & Đặt lại (Re-order):** Xác nhận báo giá để tạo đơn, theo dõi trạng thái đơn và lưu lịch sử cấu hình để đặt lại nhanh. | Khách hàng, Nhà cung cấp | Nâng cao |
| F09 | **Quản lý danh mục, bảng giá & đối tác:** Thêm/sửa thông số sản phẩm, cập nhật bảng giá tính toán tự động và quản lý hồ sơ xưởng in. | Quản trị viên | Bắt buộc |
| F10 | **Tích hợp thanh toán trực tuyến (Escrow), vận chuyển & Tạo khuôn bế (Dieline) tự động:** Kết nối cổng thanh toán/ví điện tử, giữ tiền trung gian, theo dõi vận đơn bên thứ ba và xuất khuôn bế tự động. | Khách hàng, Nhà cung cấp, Quản trị viên | Nâng cao (triển khai ở giai đoạn mở rộng) |

## 3. Ma trận phân quyền theo vai trò

| Mã | Khách chưa đăng nhập | Khách hàng | Nhà cung cấp | Quản trị viên |
|----|:---:|:---:|:---:|:---:|
| F01 | ✓ | ✓ | | |
| F02 | | ✓ | ✓ | ✓ |
| F03 | ✓ | ✓ | | |
| F04 | | ✓ | | |
| F05 | | ✓ | | |
| F06 | | ✓ | | |
| F07 | | | ✓ | |
| F08 | | ✓ | ✓ | |
| F09 | | | | ✓ |
| F10 | | ✓ | ✓ | ✓ |

## 4. Phân nhóm theo mức độ ưu tiên

- **Bắt buộc:** F01, F02, F04, F05, F06, F07, F09
- **Bắt buộc hoặc theo phạm vi:** F03
- **Nâng cao:** F08
- **Nâng cao (giai đoạn mở rộng):** F10
