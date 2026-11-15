# Phân Tích Đối Thủ Cạnh Tranh & Chốt Phạm Vi MVP — Dự Án E-Pack

## 1. Bảng So Sánh Các Website Tương Tự

| Tiêu chí | Pacdora (`www.pacdora.com`) | Packhelp (`packhelp.com`) | Packlane (`packlane.com`) | Đề xuất cho dự án E-Pack |
| :--- | :--- | :--- | :--- | :--- |
| **Trang chủ** | Tập trung thiết kế và mockup bao bì | Tập trung sản phẩm và giải pháp bao bì | Tập trung bao bì tùy chỉnh | Giao diện trực quan, giới thiệu 4 nhóm sản phẩm chính |
| **Danh mục sản phẩm** | Box, Bag, Tube, Bottle | Box, Tube, Bag, Label | Mailer Box, Product Box, Shipping Box | Phân loại: Paper Box, Paper Bag, Paper Tube, Label |
| **Tìm kiếm và lọc** | Tìm mẫu theo danh mục | Tìm kiếm và duyệt sản phẩm | Chọn sản phẩm theo loại và thông số | Lọc theo loại bao bì, chất liệu và kích thước |
| **Chi tiết sản phẩm** | Mẫu thiết kế, mockup, khuôn bế | Kích thước, chất liệu, số lượng, giá | Quy cách, vật liệu, thiết kế, giá | Hiển thị hình ảnh, thông số và tùy chọn in |
| **Giỏ hàng và đặt hàng** | Thiết kế và xuất file | Cấu hình, báo giá và đặt hàng | Cấu hình, thiết kế và thanh toán | Tải file thiết kế và gửi yêu cầu báo giá |
| **Điểm có thể cải thiện** | Chưa tập trung vào quy trình đặt bao bì hoàn chỉnh | Nhiều danh mục, cần thời gian lựa chọn | Nhiều thông số kỹ thuật | Tối giản quy trình, hỗ trợ tiếng Việt và dễ sử dụng |

---

## 2. Nhận Xét Chi Tiết Các Nền Tảng Tham Khảo

Qua khảo sát ba website **Pacdora**, **Packhelp** và **Packlane**, nhóm nhận thấy mỗi nền tảng có những chức năng nổi bật có thể vận dụng vào quá trình phát triển **E-Pack**:

* **Pacdora** ([https://www.pacdora.com/](https://www.pacdora.com/)):
  * **Điểm mạnh:** Nổi bật với thư viện mẫu bao bì, công cụ thiết kế và mô phỏng sản phẩm 3D trực quan.
  * **Áp dụng cho E-Pack:** Học hỏi cách trình bày hình ảnh trực quan, hỗ trợ khách hàng tải file thiết kế và xem trước sản phẩm. Tuy nhiên, công cụ thiết kế 3D chuyên sâu chưa phù hợp để triển khai ngay do yêu cầu kỹ thuật cao.

* **Packhelp** ([https://packhelp.com/](https://packhelp.com/)):
  * **Điểm mạnh:** Nổi bật với hệ thống phân loại sản phẩm, tùy chỉnh kích thước, chất liệu, số lượng và quy trình báo giá.
  * **Áp dụng cho E-Pack:** Áp dụng cách tổ chức danh mục sản phẩm, bộ lọc tìm kiếm và chức năng lựa chọn thông số bao bì để khách hàng dễ dàng tìm được sản phẩm phù hợp.

* **Packlane** ([https://packlane.com/](https://packlane.com/)):
  * **Điểm mạnh:** Nổi bật với quy trình cấu hình sản phẩm, thiết kế trực tuyến, tính giá và đặt hàng.
  * **Áp dụng cho E-Pack:** Học hỏi cách xây dựng quy trình lựa chọn quy cách, tải file thiết kế và gửi yêu cầu đặt hàng. Tuy nhiên, hệ thống thiết kế và tính giá tự động phức tạp chưa cần thiết trong phiên bản đầu tiên.

---

## 3. Định Hướng Phát Triển E-Pack (MVP)

Từ những ưu điểm trên, nhóm định hướng xây dựng **E-Pack** thành nền tảng thương mại điện tử B2B chuyên về bao bì và in ấn, trưng bày bốn nhóm sản phẩm chính: **Paper Box**, **Paper Bag**, **Paper Tube** và **Label**.

Các chức năng ưu tiên triển khai gồm:
1. Hiển thị và phân loại sản phẩm theo từng nhóm bao bì.
2. Tìm kiếm, lọc theo danh mục, chất liệu và xem thông tin chi tiết sản phẩm.
3. Cho phép khách hàng tùy chỉnh kích thước (đơn vị mm), chất liệu, số lượng ($MOQ \ge 100$) và gia công hợp lệ (tập trung cấu hình sâu cho 2 nhóm chính là **Hộp giấy** và **Túi giấy**).
4. Hỗ trợ tải lên file thiết kế bao bì an toàn (`.png`, `.jpg`, `.pdf`, `.zip` dưới 20MB, lưu trữ riêng tư) và xem trước 2D động cơ bản (chèn logo đè lên ảnh mẫu kèm kích thước).
5. Bắt buộc đăng nhập để gửi yêu cầu báo giá theo cơ chế lai (Hybrid), hỗ trợ thương lượng phiên bản báo giá (hiệu lực 7 ngày), đặt cọc qua chuyển khoản QR và duyệt bản in (Proofing) trước khi sản xuất.

Đối với các chức năng nâng cao như thiết kế 3D chuyên sâu, tự động tạo khuôn bế (Dieline), tích hợp cổng thanh toán tự động, kết nối ERP/CRM/Kế toán và tự động cập nhật tiến độ sản xuất từ nhà máy, nhóm chưa ưu tiên triển khai do hạn chế về thời gian, kỹ thuật và nguồn lực.

---

## 4. Bảng Rà Soát Phản Biện & Quyết Định Chốt Phạm Vi Chức Năng

| Nội dung | Đề xuất ban đầu | Phản biện kỹ thuật & nghiệp vụ | Quyết định chốt phạm vi của nhóm |
| :--- | :--- | :--- | :--- |
| **Quản lý tài khoản & Xác thực** | Có (Đăng ký, đăng nhập, quản lý thông tin doanh nghiệp, khôi phục mật khẩu) | Cần khóa quyền gửi yêu cầu báo giá của Guest để tránh dữ liệu rác tách rời khỏi hệ thống | **Giữ lại và sửa đổi:** Giữ các chức năng tài khoản; bắt buộc khách hàng đăng nhập mới được gửi yêu cầu báo giá để quản lý tập trung lịch sử giao dịch. |
| **Phân quyền người dùng** | Có 4 vai trò (Guest, Customer, Sales, Admin; quyền Sales/Admin ở mục đặt hàng ghi là "Hỗ trợ") | Tách riêng Sales và Admin gây trùng lặp giao diện quản trị cho nhóm 7 người; từ "Hỗ trợ" mơ hồ, không lập trình được | **Sửa đổi:** Gộp quyền xử lý của Sales và Admin trong giai đoạn MVP để tối ưu nguồn lực; đổi từ "Hỗ trợ" thành chức năng *"Tạo đơn hộ khách hàng"* có ghi log. |
| **Danh mục sản phẩm & Tìm kiếm, lọc** | Có (4 nhóm: Hộp giấy, Túi giấy, Ống giấy, Nhãn in; lọc theo danh mục và chất liệu) | Đáp ứng tốt nhu cầu cơ bản | **Giữ lại:** Đáp ứng đúng nhu cầu tra cứu sản phẩm B2B cơ bản và hoàn toàn nằm trong khả năng triển khai của nhóm. |
| **Tùy chỉnh thông số kỹ thuật sản phẩm** | Có (Nhập kích thước, chất liệu, định lượng, kỹ thuật in, gia công, số lượng cho cả 4 nhóm) | Vượt phạm vi MVP vì công thức tính phôi 4 loại khác nhau hoàn toàn; thiếu đơn vị đo (`mm`/`cm`), MOQ và ràng buộc gia công | **Sửa đổi:** Trưng bày đủ 4 danh mục nhưng chỉ làm công cụ tùy chỉnh sâu cho 2 nhóm chính (Hộp giấy, Túi giấy); bổ sung ràng buộc đơn vị `mm`, $MOQ \ge 100$ và ma trận gia công hợp lệ. |
| **Xem trước sản phẩm (Mockup / 2D / 3D)** | Có (Mục tiêu trực quan như Pacdora, nhưng MVP lại hạ xuống chỉ dùng ảnh mockup tĩnh có sẵn) | Ảnh mockup tĩnh không hiển thị được logo và kích thước thực tế của khách, chưa giải quyết được bài toán khó hình dung sản phẩm | **Sửa đổi:** Loại bỏ 3D khỏi MVP để tránh quá tải; nâng cấp mockup tĩnh thành *Xem trước 2D động cơ bản* (cho phép chèn logo đè lên ảnh mẫu và hiển thị kích thước Dài $\times$ Rộng $\times$ Cao). |
| **Upload logo và file thiết kế** | Có (Tải lên logo/file thiết kế, giới hạn định dạng và dung lượng) | Thiếu tiêu chuẩn bảo mật: file `.svg`/`.pdf` dễ bị chèn mã độc XSS; lưu file ở thư mục công khai dễ bị lộ thiết kế độc quyền của khách | **Giữ lại và siết chặt bảo mật:** Chỉ nhận định dạng an toàn (`.png`, `.jpg`, `.pdf`, `.zip` dưới 20MB), kiểm tra MIME-type ở Backend và lưu file ở chế độ riêng tư (Signed URL). |
| **Cơ chế báo giá (Tự động & Thủ công)** | Có (Vừa yêu cầu tự động tính giá trên giao diện, vừa giả định Sales lập báo giá thủ công 100%) | Mâu thuẫn quy trình; nếu tính giá ở Frontend dễ bị sửa giá, còn báo giá thủ công 100% thì không rút ngắn thời gian chờ | **Sửa đổi sang Báo giá lai (Hybrid):** Tự động tính giá ước tính tại Backend với các thông số tiêu chuẩn; chỉ chuyển sang luồng Sales báo giá thủ công khi đơn có yêu cầu đặc biệt. |
| **Đàm phán & Hiệu lực báo giá** | Có ở mức cơ bản (Khách chỉ có 2 lựa chọn: Xác nhận hoặc Từ chối báo giá; không có hạn sử dụng) | Thiếu thực tế B2B: khách từ chối vì giá cao cần kênh thương lượng; giá giấy biến động nên báo giá không thể có hiệu lực vô thời hạn | **Bổ sung:** Thêm nút *"Yêu cầu điều chỉnh báo giá"* (tạo phiên bản v2, v3), quy định thời hạn hiệu lực (7 ngày) và lưu cứng đơn giá tại thời điểm chốt (Snapshot). |
| **Quy trình đặt cọc & Thanh toán** | Chưa rõ ràng (Xác nhận báo giá xong tạo đơn sản xuất luôn; thanh toán trực tuyến đưa vào phần nâng cao) | Thiếu mắt xích sống còn: bao bì in theo yêu cầu không thể bán lại cho khách khác nếu người đặt hủy ngang khi chưa đặt cọc | **Triển khai theo giai đoạn:** MVP chưa tích hợp cổng thanh toán tự động nhưng bổ sung trạng thái *"Chờ đặt cọc"* (hiển thị mã QR chuyển khoản và upload biên lai để Admin duyệt trước khi sản xuất). |
| **Duyệt bản in trước sản xuất (Proofing)** | Không có | Thiếu nghiệp vụ cốt lõi ngành in: file khách gửi thường sai hệ màu CMYK/tràn lề, cần nhà in dàn trang gửi lại khách ký duyệt trước khi chạy máy | **Bổ sung:** Thêm bước Admin/Sales upload bản vẽ hoàn chỉnh (Maket) lên đơn hàng để khách kiểm tra và bấm *"Duyệt bản in"* hoặc *"Yêu cầu chỉnh sửa"* trước khi đưa vào sản xuất. |
| **Quản lý đơn hàng & Tiến độ sản xuất** | Có (Mô tả hệ thống tự động cập nhật trạng thái đơn hàng theo từng giai đoạn sản xuất và giao hàng) | Bất khả thi trong phạm vi đồ án vì website không kết nối phần mềm nhà máy (ERP) hay API đơn vị vận chuyển | **Loại bỏ** (Chỉ cập nhật trạng thái đơn hàng thủ công trên hệ thống). |
| **Địa chỉ giao hàng & Chính sách hủy đơn** | Có nhắc tới "Hỗ trợ yêu cầu hủy đơn theo chính sách" nhưng chưa mô tả điều kiện và luồng thực hiện | Thiếu bước chọn địa chỉ nhận hàng B2B và thiếu điều kiện khóa nút hủy khi xưởng đã tiến hành in ấn | **Giữ lại và làm rõ:** Bổ sung bước chọn địa chỉ nhận hàng khi đặt đơn; chỉ cho phép khách gửi yêu cầu hủy khi đơn chưa chuyển sang trạng thái *"Đang sản xuất"*. |
| **Tạo Dieline tự động & AI gợi ý thiết kế** | Có (Đưa vào danh mục chức năng nâng cao) | Vượt phạm vi môn học và năng lực kỹ thuật của nhóm (thuật toán dựng khuôn bế CAD/Dieline và huấn luyện AI rất phức tạp) | **Loại bỏ** |
| **Tích hợp CRM, ERP và Kế toán** | Có (Đưa vào danh mục chức năng nâng cao) | Vượt phạm vi đề tài website thương mại điện tử và không có hạ tầng doanh nghiệp thực tế để tích hợp API | **Loại bỏ** |
| **Yêu cầu phi chức năng & Kiểm thử** | Có (Tốc độ tải dưới 3s, giao diện dễ hiểu, có cơ chế sao lưu và phục hồi dữ liệu) | Viết cảm tính, thiếu thông số định lượng (số lượng người dùng đồng thời, chu kỳ backup) nên không thể viết Test Case nghiệm thu | **Giữ lại và định lượng hóa:** Chốt mục tiêu tải trang dưới 3 giây với 50 người dùng đồng thời (đo bằng JMeter/Lighthouse) và cấu hình script tự động sao lưu database mỗi 24 giờ. |