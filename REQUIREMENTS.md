# Requirements

Tài liệu đặc tả yêu cầu cho dự án **E-Pack — Nền tảng Thương mại điện tử B2B cho Sản phẩm Bao bì và In ấn theo yêu cầu**, được tổng hợp và đối chiếu thống nhất với các tài liệu hiện có của nhóm:
- Tổng quan & mô hình kinh doanh: `readme.md.md`
- Vai trò người dùng & mã chức năng (`F01`–`F10`): `user-roles.md`
- Quy trình nghiệp vụ 9 bước: `business-workflow.md`
- Phân tích đối thủ & chốt phạm vi MVP: `competitor_analysis_e_pack.md`
- Kế hoạch dự án & quản lý rủi ro: `Project Plan — Nền tảng Thương mại Điện tử B2B E-Pack.md`
- Tiêu chí công việc nhóm: `Github_Issue.md`

---

## 1. Mục tiêu dự án

- **Mục tiêu kinh doanh:** Xây dựng nền tảng thương mại điện tử B2B theo mô hình web-to-pack, kết nối các doanh nghiệp có nhu cầu đặt bao bì và in ấn theo yêu cầu (SMEs, startup, shop online, agency) với mạng lưới xưởng in và nhà sản xuất tại Việt Nam.
- **Vấn đề cần giải quyết và giá trị mang lại cho khách hàng:**
  - Số hóa quy trình trao đổi thông số, tải thiết kế và gửi yêu cầu báo giá (RFQ) tập trung trên một hệ thống, thay thế cách liên hệ thủ công qua Zalo, email hoặc điện thoại vốn mất 3–5 ngày chờ báo giá.
  - Chuẩn hóa đầu vào thông số kỹ thuật và cung cấp công cụ xem trước trực quan để khách hàng phát hiện sớm lỗi bố cục hoặc vị trí logo trước khi sản xuất.
  - Minh bạch hóa chi phí bằng bảng tính giá dự kiến tham khảo theo thời gian thực, đồng thời hỗ trợ doanh nghiệp vừa và nhỏ đặt hàng với số lượng tối thiểu hợp lý (`MOQ >= 100`).
  - Lưu trữ lịch sử cấu hình, tệp thiết kế và đơn hàng để phục vụ theo dõi tiến độ và đặt lại nhanh (Re-order).

---

## 2. Phạm vi

### Trong phạm vi

Các chức năng thống nhất triển khai trong phạm vi đồ án (phiên bản MVP / Prototype):

- **Danh mục và tìm kiếm/lọc sản phẩm (`F01`):** Trưng bày 4 nhóm sản phẩm cốt lõi (**Hộp giấy / Paper Box**, **Túi giấy / Paper Bag**, **Tube giấy / Ống giấy / Paper Tube**, **Nhãn in / Label**); hỗ trợ tìm kiếm và lọc theo loại bao bì, chất liệu, kích thước.
- **Quản lý tài khoản và phân quyền (`F02`):** Đăng ký, đăng nhập và phân tách giao diện theo 3 nhóm tài khoản đã đăng nhập (Khách hàng, Nhà cung cấp, Quản trị viên); bắt buộc đăng nhập mới được gửi yêu cầu báo giá (RFQ).
- **Cấu hình sản phẩm (`F03`):** Chọn loại sản phẩm, thiết lập kích thước (đơn vị `mm`), kiểu dáng, chất liệu giấy, định lượng (`gsm`), số lượng (`MOQ >= 100`), phương pháp/số màu in và gia công hoàn thiện hợp lệ. Theo chốt phạm vi MVP và tiêu chí kỹ thuật nhóm, ưu tiên hoàn thiện form cấu hình đầy đủ cho **Hộp giấy** và **Túi giấy** (kèm thông số cơ bản cho **Tube giấy** và **Nhãn in**).
- **Tải lên và kiểm tra tệp thiết kế (`F04`):** Tải tệp thiết kế và kiểm tra tự động cơ bản (Preflight: định dạng, dung lượng, độ phân giải dpi, tỷ lệ khung). Theo rà soát bảo mật MVP, ưu tiên chỉ nhận định dạng an toàn (`.png`, `.jpg`, `.pdf`, `.zip` dưới 20 MB), kiểm tra MIME-type ở Backend và lưu ở chế độ riêng tư (Signed URL).
- **Xem trước sản phẩm (`F05`):** Hiển thị bản thiết kế ghép lên mô hình bao bì (hỗ trợ xem trước 2D động cơ bản thể hiện vùng an toàn và kích thước Dài x Rộng x Cao, hoặc mockup mẫu cố định minh họa góc nhìn 3D ở mức cơ bản).
- **Tính giá dự kiến và gửi RFQ (`F06`):** Tự động tính giá ước tính tham khảo tại Backend dựa trên bảng giá hệ thống (cơ chế báo giá lai Hybrid); lưu vết cấu hình, tệp thiết kế, địa chỉ nhận hàng và gửi RFQ đến nhà cung cấp (che thông tin liên hệ trực tiếp trước khi xác nhận đơn).
- **Quản lý yêu cầu và báo giá chính thức (`F07`):** Nhà cung cấp tiếp nhận RFQ, thẩm định tệp thiết kế và gửi báo giá chính thức (hiệu lực 7 ngày; cảnh báo nếu chênh quá 10% so với giá dự kiến); hỗ trợ khách hàng yêu cầu điều chỉnh báo giá (tạo phiên bản v2, v3).
- **Xác nhận, đặt cọc, duyệt bản in, theo dõi và đặt lại đơn hàng (`F08`):** Khách hàng xác nhận báo giá (lưu snapshot đơn giá), chuyển khoản đặt cọc qua mã QR và tải biên lai chờ Admin duyệt; duyệt bản in hoàn chỉnh (Maket/Proofing) trước khi sản xuất; cho phép yêu cầu hủy đơn khi chưa chuyển trạng thái *Đang sản xuất*; cập nhật và theo dõi trạng thái đơn thủ công trên hệ thống; hỗ trợ đặt lại đơn cũ (Re-order).
- **Quản trị danh mục, bảng giá và đối tác (`F09`):** Quản trị viên quản lý danh mục, thông số sản phẩm, bảng giá tính toán, hồ sơ xưởng in đối tác, duyệt biên lai đặt cọc và tạo đơn hỗ trợ khách hàng (có ghi log).

### Ngoài phạm vi

Các chức năng chưa triển khai trong đồ án (thuộc giai đoạn mở rộng `F10` hoặc đã loại bỏ sau rà soát MVP):

- Dựng mô hình 3D tương tác chuyên sâu theo thời gian thực.
- Thuật toán tự động tạo khuôn bế kỹ thuật (CAD/Dieline) và AI gợi ý/sinh thiết kế bao bì.
- Tích hợp cổng thanh toán trực tuyến tự động, ví điện tử và cơ chế giữ tiền trung gian (Escrow).
- Kết nối API tự động với phần mềm nhà máy (ERP), hệ thống CRM, phần mềm kế toán và API đơn vị vận chuyển bên thứ ba.
- Cập nhật tiến độ sản xuất tự động trực tiếp từ máy móc nhà xưởng (trạng thái đơn được cập nhật thủ công trên hệ thống).

---

## 3. Người dùng

Thống nhất 4 vai trò theo `user-roles.md` (trong giai đoạn MVP, nghiệp vụ hỗ trợ bán hàng/Sales được gộp vào quyền của Quản trị viên để phù hợp với quy mô nhóm 7 thành viên):

| Vai trò | Mô tả | Quyền hạn chính (khớp `user-roles.md`) |
| :--- | :--- | :--- |
| **Khách chưa đăng nhập** | Người truy cập chưa có tài khoản hoặc chưa đăng nhập. | Xem danh sách/chi tiết 4 nhóm sản phẩm, tài liệu hướng dẫn (`F01`) và dùng thử cấu hình để xem giá dự kiến (`F03`). Bị khóa quyền gửi RFQ. |
| **Khách hàng** | Doanh nghiệp B2B, startup, shop online hoặc cá nhân đã đăng ký tài khoản. | Quản lý tài khoản và địa chỉ nhận hàng (`F02`), xem và cấu hình sản phẩm (`F01`, `F03`), tải file thiết kế (`F04`), xem trước (`F05`), gửi RFQ và yêu cầu điều chỉnh báo giá (`F06`), xác nhận đơn/đặt cọc/duyệt bản in/theo dõi và đặt lại đơn (`F08`). |
| **Nhà cung cấp** | Xưởng in hoặc đối tác sản xuất đã được thẩm định hồ sơ. | Đăng nhập vào giao diện đối tác (`F02`), tiếp nhận RFQ, xem/tải file thiết kế của đơn được điều phối, gửi báo giá chính thức và tải bản vẽ Proofing (`F07`), cập nhật tiến độ xử lý đơn hàng (`F08`). |
| **Quản trị viên (Admin)** | Quản trị viên nền tảng (kiêm điều phối bán hàng trong MVP). | Đăng nhập giao diện quản trị (`F02`), quản lý danh mục, thông số kỹ thuật, bảng giá, hồ sơ xưởng in đối tác, xác nhận biên lai đặt cọc và tạo đơn hộ khách hàng có ghi log (`F09`). |

---

## 4. Yêu cầu chức năng

Bảng yêu cầu chức năng giữ nguyên mã `F01`–`F10`, tên chức năng, nhóm người sử dụng và mức độ ưu tiên trong `user-roles.md`, đồng thời ánh xạ tương ứng với 9 bước quy trình trong `business-workflow.md`:

| Mã | Tên chức năng | Mô tả | Người sử dụng | Mức độ ưu tiên | Tiêu chí nghiệm thu |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **F01** | Xem danh sách và chi tiết sản phẩm | Hiển thị thông tin 4 nhóm sản phẩm cốt lõi (hộp giấy, túi giấy, tube giấy, nhãn in), tìm kiếm/lọc theo danh mục, chất liệu, kích thước và xem nội dung hướng dẫn (Bước 1 quy trình). | Khách chưa đăng nhập, Khách hàng | Bắt buộc | Hiển thị đầy đủ 4 nhóm sản phẩm; bộ lọc trả về đúng sản phẩm theo danh mục/chất liệu/kích thước; trang chi tiết hiển thị đầy đủ ảnh, thông số và tùy chọn in. |
| **F02** | Đăng ký, đăng nhập và phân quyền tài khoản | Xác thực người dùng và phân tách giao diện, quyền truy cập theo 3 nhóm đã đăng nhập: Khách hàng, Nhà cung cấp, Quản trị viên (Bước 1 quy trình). | Khách hàng, Nhà cung cấp, Quản trị viên | Bắt buộc | Mật khẩu được mã hóa; khách chưa đăng nhập không thể gửi RFQ; người dùng không có quyền không truy cập được màn hình hoặc dữ liệu của vai trò khác. |
| **F03** | Cấu hình sản phẩm (Product Configurator) | Cho phép chọn kích thước (`mm`), kiểu dáng, chất liệu, định lượng giấy, số lượng (`MOQ >= 100`), phương pháp in và gia công hoàn thiện hợp lệ (Bước 2 quy trình). | Khách chưa đăng nhập, Khách hàng | Bắt buộc hoặc theo phạm vi | Form nhập đầy đủ thông số cho Hộp giấy và Túi giấy (cùng thông số cơ bản cho Tube giấy); hệ thống chặn gửi nếu thiếu trường bắt buộc, nhập sai đơn vị hoặc số lượng nhỏ hơn `MOQ`. |
| **F04** | Tải lên và kiểm tra file thiết kế (Preflight cơ bản) | Cho phép tải file thiết kế (ưu tiên định dạng an toàn `.png`, `.jpg`, `.pdf`, `.zip` dưới 20 MB; kiểm soát bảo mật ở Backend) và tự động kiểm tra định dạng, dung lượng, độ phân giải (dpi), tỷ lệ khung (Bước 3–4 quy trình). | Khách hàng | Bắt buộc | File hợp lệ được lưu riêng tư (Signed URL); file sai định dạng, vượt dung lượng hoặc không đạt tiêu chí cơ bản hiển thị thông báo lỗi cụ thể để khách tải lại. |
| **F05** | Xem trước sản phẩm 2D/3D (Preview 2D/3D) | Hiển thị bản thiết kế được ghép lên mô hình bao bì ở chế độ xem trước 2D (vùng an toàn, kích thước Dài x Rộng x Cao) và mô phỏng góc nhìn trên mẫu dựng sẵn (Bước 5 quy trình). | Khách hàng | Bắt buộc | Sau khi tải thiết kế hợp lệ, người dùng quan sát được bản ghép logo/thiết kế trên mẫu kèm kích thước và có thể quay lại Bước 2 để chỉnh sửa nếu chưa đạt. |
| **F06** | Tính giá dự kiến và Gửi yêu cầu báo giá (RFQ) | Tự động ước tính chi phí tham khảo theo cấu hình tại Backend; cho phép điền thông tin liên hệ/địa chỉ nhận hàng, gửi RFQ tới nhà cung cấp và yêu cầu điều chỉnh báo giá (Bước 6–7 quy trình). | Khách hàng | Bắt buộc | Đơn giá và tổng chi phí dự kiến tự cập nhật theo cấu hình và số lượng; hiển thị rõ nhãn giá tham khảo; RFQ gửi thành công được lưu vào CSDL và che thông tin liên hệ trực tiếp trước khi chốt đơn. |
| **F07** | Quản lý yêu cầu và Báo giá chính thức | Tiếp nhận thông tin cấu hình, thẩm định file thiết kế và gửi báo giá chính thức (hiệu lực 7 ngày, hỗ trợ phiên bản v2/v3 khi thương lượng và cảnh báo nếu lệch trên 10% so với giá dự kiến) (Bước 8 quy trình). | Nhà cung cấp | Bắt buộc | Nhà cung cấp xem được đầy đủ thông số cấu hình và tải được file thiết kế của RFQ được giao; báo giá gửi đi lưu được lịch sử phiên bản và thời hạn hiệu lực. |
| **F08** | Xác nhận, theo dõi đơn hàng và Đặt lại (Re-order) | Xác nhận báo giá để tạo đơn (snapshot đơn giá), đặt cọc qua QR/upload biên lai, duyệt bản in Proofing trước sản xuất, hủy đơn khi chưa sản xuất, cập nhật/theo dõi trạng thái và đặt lại từ cấu hình cũ (Bước 9 quy trình). | Khách hàng, Nhà cung cấp | Nâng cao | Tạo được đơn hàng thành công với snapshot đơn giá; khóa chức năng hủy khi đơn ở trạng thái *Đang sản xuất*; trạng thái đơn cập nhật chính xác và tạo lại được cấu hình từ đơn cũ. |
| **F09** | Quản lý danh mục, bảng giá và đối tác | Thêm/sửa danh mục và thông số sản phẩm, cập nhật bảng giá tính toán tự động, quản lý hồ sơ xưởng in, duyệt biên lai đặt cọc và tạo đơn hộ khách hàng có ghi log (Bước 6 và quản trị hệ thống). | Quản trị viên | Bắt buộc | Cập nhật bảng giá/thông số có hiệu lực ngay với lần tính giá dự kiến tiếp theo; mọi thao tác xác nhận đặt cọc hoặc tạo đơn hộ đều yêu cầu quyền Admin và được lưu log. |
| **F10** | Thanh toán trực tuyến (Escrow), vận chuyển và Dieline tự động | Kết nối cổng thanh toán/ví điện tử, giữ tiền trung gian, theo dõi vận đơn bên thứ ba và xuất khuôn bế tự động. | Khách hàng, Nhà cung cấp, Quản trị viên | Nâng cao (giai đoạn mở rộng) | Thuộc giai đoạn mở rộng sau môn học; không nằm trong phạm vi nghiệm thu MVP. |

---

## 5. Yêu cầu phi chức năng

1. **Hiệu suất:** Thời gian tải trang mục tiêu dưới 3 giây khi kiểm thử với 50 người dùng đồng thời (đo bằng Lighthouse hoặc JMeter).
2. **Tương thích và Responsive:** Giao diện hiển thị tốt trên máy tính, tablet và điện thoại; hoạt động ổn định trên Chrome, Edge và các trình duyệt phổ biến.
3. **Khả năng sử dụng và kiểm tra dữ liệu:** Biểu mẫu rõ ràng, có hướng dẫn đơn vị và thông báo lỗi cụ thể; không cho phép gửi biểu mẫu khi thiếu thông tin bắt buộc hoặc sai định dạng.
4. **Bảo mật và phân quyền:**
   - Mã hóa mật khẩu người dùng; phân quyền chặt chẽ theo vai trò (Khách hàng chỉ xem được báo giá và đơn hàng của chính mình; người không có quyền không truy cập được trang quản trị/xưởng in).
   - Kiểm tra MIME-type và giới hạn dung lượng tệp tải lên tại Backend; lưu file thiết kế của khách hàng ở chế độ riêng tư (Signed URL).
   - Không đưa mật khẩu, API key, token hoặc dữ liệu cá nhân thật vào mã nguồn công khai (tuân thủ `AGENTS.md`).
5. **Tuân thủ pháp lý:** Minh bạch thông tin hàng hóa và phân định rõ giá dự kiến với giá chính thức (Luật TMĐT 122/2025/QH15, Nghị định 248/2026/NĐ-CP), bảo vệ dữ liệu cá nhân (Nghị định 13/2023/NĐ-CP) và bảo hộ quyền sở hữu trí tuệ đối với file thiết kế (Luật SHTT sửa đổi 131/2025/QH15).
6. **Độ tin cậy, bảo trì và sao lưu:** Mã nguồn tổ chức rõ ràng, dễ bảo trì; dữ liệu báo giá và đơn hàng lưu trữ chính xác (snapshot đơn giá tại thời điểm xác nhận); cấu hình sao lưu cơ sở dữ liệu định kỳ mỗi 24 giờ và có khả năng khôi phục.

---

## 6. Giới hạn và giả định

### Giới hạn

- **Thời gian và nhân lực:** Dự án thực hiện trong phạm vi một học phần với nhóm 7 thành viên (phân công theo `Project Plan` và `Github_Issue.md`: Trưởng nhóm/BA, UI/UX, Frontend, Backend/Database, QA/Integration), do đó tập trung hoàn thiện 3 nghiệp vụ cốt lõi: cấu hình sản phẩm, gửi/xử lý RFQ và quản lý đơn hàng.
- **Công nghệ xem trước và khuôn bế:** Nhóm chưa có đủ điều kiện xây dựng công cụ dựng mô hình 3D động chuyên sâu hay thuật toán CAD/Dieline tự động; phiên bản MVP sử dụng xem trước 2D động hoặc mockup mẫu cố định và ưu tiên cấu hình sâu cho Hộp giấy và Túi giấy.
- **Tích hợp ngoài:** Chưa tích hợp cổng thanh toán tự động (Escrow), phần mềm quản lý nhà xưởng (ERP/CRM) hay API vận chuyển thực tế; hệ thống dừng ở quy mô Prototype/MVP phục vụ kiểm chứng nghiệp vụ.

### Giả định

- Giá hiển thị ngay khi người dùng cấu hình chỉ là **giá dự kiến tham khảo**; giá chính thức do Nhà cung cấp thẩm định và gửi báo giá (có hiệu lực 7 ngày).
- Khách hàng bắt buộc đăng nhập mới được gửi yêu cầu báo giá; phải đặt cọc qua QR/biên lai và duyệt bản vẽ Proofing trước khi đơn hàng chuyển sang sản xuất.
- Trạng thái đơn hàng và tiến độ sản xuất được Nhà cung cấp hoặc Quản trị viên cập nhật thủ công trên hệ thống trong giai đoạn đầu.
- Hình ảnh mockup và dữ liệu bảng giá dùng trong đồ án là dữ liệu mẫu phục vụ mục đích thử nghiệm.
