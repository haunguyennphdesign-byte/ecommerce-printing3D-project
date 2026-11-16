# AI Usage Log

**Dự án:** E-Pack — Nền tảng thương mại điện tử B2B cho bao bì và in ấn theo yêu cầu  
**Môn học:** Phát triển ứng dụng thương mại điện tử · **Nhóm:** 01

Các mục ghi theo đầu việc. Prompt gốc được chép từ ảnh hoặc bản ghi. Prompt dựng lại dựa trên bài nhóm và cần người phụ trách xác nhận. Tên công cụ chưa có trong tài liệu được ghi là “Chưa xác nhận”. Tên ở mục Người kiểm tra là người phụ trách được đề xuất đối chiếu.

## Lần sử dụng 1 — Soạn bản nháp `REQUIREMENTS.md`

### Công cụ

Gemini 
### Mục đích

Tổng hợp tài liệu của các thành viên thành bản đặc tả yêu cầu thống nhất cho E-Pack, có phạm vi MVP và tiêu chí nghiệm thu để nhóm triển khai và kiểm thử.

### Prompt



> Tôi đang tổng hợp tài liệu đặc tả yêu cầu cho dự án website thương mại điện tử B2B E-Pack (bao bì và in ấn theo yêu cầu). Dựa trên các tài liệu hiện có của nhóm gồm: readme.md.md (tổng quan và mô hình kinh doanh), user-roles.md (4 vai trò và 10 chức năng F01–F10), business-workflow.md (quy trình 9 bước), competitor_analysis_e_pack.md (bảng chốt phạm vi MVP), Project Plan (7 thành viên và 5 rủi ro) và Github_Issue.md (tiêu chí hoàn thành), hãy lập bản nháp REQUIREMENTS.md theo đúng 6 phần: 1. Mục tiêu dự án, 2. Phạm vi (Trong phạm vi / Ngoài phạm vi), 3. Người dùng, 4. Yêu cầu chức năng (đủ 6 cột: Mã, Tên chức năng, Mô tả, Người sử dụng, Mức độ ưu tiên, Tiêu chí nghiệm thu), 5. Yêu cầu phi chức năng, 6. Giới hạn và giả định.

### Kết quả đề xuất

AI soạn bản nháp gồm sáu phần. Mục tiêu là số hóa quy trình đặt bao bì theo yêu cầu, từ chọn thông số, tải thiết kế đến gửi yêu cầu báo giá (RFQ). MVP có bốn nhóm sản phẩm gồm hộp giấy, túi giấy, ống giấy và nhãn in. Luồng chính gồm cấu hình sản phẩm, kiểm tra tệp thiết kế, xem trước, tính giá dự kiến, gửi và xử lý RFQ, đặt cọc qua QR, duyệt bản in thử và theo dõi đơn hàng.

Bản nháp xác định bốn vai trò gồm khách chưa đăng nhập, khách hàng, nhà cung cấp và quản trị viên. Bảng F01–F10 gồm mã, tên chức năng, mô tả, người sử dụng, mức độ ưu tiên và tiêu chí nghiệm thu. Các yêu cầu phi chức năng bao gồm mục tiêu tải trang dưới 3 giây với 50 người dùng đồng thời, giao diện thích ứng, phân quyền, kiểm tra tệp tại backend và sao lưu cơ sở dữ liệu mỗi 24 giờ.

### Phản biện

Bản nháp cần đối chiếu quyền thực hiện F07–F08 với ma trận phân quyền, gắn mã chức năng với từng bước trong quy trình nghiệp vụ 9 bước và kiểm tra độ khớp giữa phạm vi MVP với tiêu chí hoàn thành trên GitHub Issue. Các yêu cầu liên quan đến rủi ro cần có điều kiện kiểm tra cụ thể.

### Quyết định của nhóm

Dùng cấu trúc sáu phần và bảng F01–F10 làm khung đặc tả. Với MVP của nhóm 7 thành viên, ưu tiên cấu hình sản phẩm, gửi và xử lý RFQ, quản lý đơn hàng. Dựng 3D tương tác chuyên sâu, tạo khuôn bế tự động, thanh toán tự động và tích hợp hệ thống nhà xưởng thuộc phạm vi mở rộng.

### Người kiểm tra

Đề xuất Trần Thị Yến Như, phụ trách `REQUIREMENTS.md`, kiểm tra phạm vi và tiêu chí nghiệm thu của từng chức năng.

## Lần sử dụng 2 — Kiểm tra chéo và hoàn thiện `REQUIREMENTS.md`

### Công cụ

Gemini
### Mục đích

Đối chiếu bản nháp với ma trận phân quyền, quy trình nghiệp vụ 9 bước, phạm vi MVP, tiêu chí hoàn thành trên GitHub Issue và biện pháp giảm thiểu rủi ro trong Project Plan.

### Prompt


> Hãy kiểm tra chéo lại bản nháp trên với toàn bộ tài liệu của các thành viên khác để bảo đảm khớp hoàn toàn: đối chiếu từng dòng ma trận phân quyền trong user-roles.md, ánh xạ đủ 9 bước quy trình trong business-workflow.md, thống nhất giữa phạm vi sản phẩm ở competitor_analysis_e_pack.md với tiêu chí hoàn thành ở Github_Issue.md và các giải pháp giảm thiểu rủi ro trong Project Plan, sau đó xuất bản REQUIREMENTS.md hoàn chỉnh.

### Kết quả đề xuất

Theo bản phản hồi, AI ánh xạ 9 bước nghiệp vụ vào F01–F09 và đưa F10 vào giai đoạn mở rộng. F07 giao cho nhà cung cấp tiếp nhận RFQ, thẩm định tệp và gửi báo giá chính thức. F08 giao cho khách hàng và nhà cung cấp thực hiện các bước xử lý, theo dõi đơn theo quyền của từng bên. Quản trị viên duyệt biên lai đặt cọc và tạo đơn hộ có ghi nhật ký tại F09.

AI ưu tiên cấu hình chi tiết hộp giấy và túi giấy ở F03, đồng thời nêu thông số cơ bản cho ống giấy. F05 dùng bản xem trước 2D động cơ bản hoặc mockup 3D cố định. F06 che thông tin liên hệ trực tiếp trước khi xác nhận đơn. F07 quy định báo giá chính thức có hiệu lực 7 ngày, lưu lịch sử các phiên bản báo giá và cảnh báo khi chênh trên 10% so với giá dự kiến.

### Phản biện

Cần phân biệt tác vụ gửi báo giá chính thức của nhà cung cấp (F07), thao tác xử lý đơn của khách hàng và nhà cung cấp (F08), và quyền duyệt cọc của quản trị viên (F09). Trong bản v2, mô tả phạm vi F03 có nhắc thông số cơ bản của cả ống giấy và nhãn in, còn tiêu chí nghiệm thu F03 chỉ nêu ống giấy. Cần đối chiếu lại với GitHub Issue để chốt tiêu chí cho nhãn in.

### Quyết định của nhóm

Bản đặc tả v2 yêu cầu khách đăng nhập trước khi gửi RFQ, hiển thị giá dự kiến dưới dạng giá tham khảo và lưu đơn giá tại thời điểm khách xác nhận báo giá chính thức. Khách chuyển khoản đặt cọc qua QR, tải biên lai để quản trị viên duyệt, rồi duyệt bản in thử trước khi sản xuất. Tiến độ đơn được cập nhật thủ công trong MVP.

### Người kiểm tra

Đề xuất Trần Thị Yến Như đối chiếu lại F03, phân quyền F07–F09 và tiêu chí nghiệm thu với các tài liệu tương ứng.

## Lần sử dụng 3 — Chuẩn bị `AGENTS.md`

### Công cụ

Gemini, theo bản ghi trong `Kế Hoạch R&D Web TMĐT.docx`.

### Mục đích

Xin bản nháp về kế hoạch R&D và các nguyên tắc phối hợp với AI để tham khảo khi soạn `AGENTS.md`.

### Prompt

*Chép từ bản ghi Gemini, giữ nguyên cách gõ.*

> Hãy lập kế hoạchR$D cho thương hiệumin 3D tôi đã đề cập truóc đó, để tôi hoàn thành bài tập nghiên cứu phát triển web thương mại điện tử.

### Kết quả đề xuất

Gemini đề xuất nguyên tắc viết mã dễ bảo trì, thực hiện thay đổi nhỏ, đọc tài liệu và đề xuất phương án trước khi sửa code. Sau khi sửa, cần nêu tệp đã chỉnh, cách chạy và cách kiểm thử. Kết quả cũng có gợi ý dùng dữ liệu mẫu, bảo vệ thông tin đăng nhập và chia công việc thành các giai đoạn R&D.

### Phản biện

Đối chiếu với `REQUIREMENTS.md`, bản trả lời của Gemini dùng ví dụ giỏ hàng và thanh toán giả lập theo luồng TMĐT thông thường. E-Pack tập trung vào cấu hình bao bì, gửi RFQ và báo giá. Đây là điểm cần chỉnh khi áp dụng bản nháp vào dự án.

### Quyết định của nhóm

Phần hướng dẫn trong bài nhóm bám phạm vi `REQUIREMENTS.md` và giữ các quy tắc về đọc tài liệu, đề xuất phương án, xác nhận trước khi sửa, báo cáo thay đổi và hướng dẫn kiểm thử. Các ví dụ nghiệp vụ trong bản nháp Gemini cần được đối chiếu với luồng E-Pack trước khi đưa vào `AGENTS.md`.

### Người kiểm tra

Đề xuất Lê Võ Thiện Nhân, phụ trách `AGENTS.md`, đối chiếu nội dung với phạm vi và quy trình của nhóm.

## Lần sử dụng 4 — Chuẩn bị `README.md`

### Công cụ

Chưa xác nhận tên công cụ từ ảnh prompt.

### Mục đích

Soạn trang giới thiệu repository để người đọc hiểu đề tài, khách hàng mục tiêu, chức năng, thành viên, công nghệ dự kiến và hướng triển khai.

### Prompt

*Chép từ ảnh prompt README.*

> # Tên dự án
>
> ## 1. Giới thiệu
> Mô tả website và vấn đề kinh doanh cần giải quyết.
>
> ## 2. Khách hàng mục tiêu
> Mô tả nhóm người dùng chính.
> ## 3. Chức năng chính
> Liệt kê các chức năng dự kiến.
>
> ## 4. Thành viên
> - Thành viên 1 – Vai trò
> - Thành viên 2 – Vai trò
> - Thành viên 3 – Vai trò
> - Thành viên 4 – Vai trò
> - Thành viên 5 – Vai trò
>
> ## 5. Công nghệ dự kiến
> Ghi rõ công nghệ đã thống nhất.
>
> ## 6. Kế hoạch thực hiện
> Tóm tắt các giai đoạn của dự án.
>
> ## 7. Liên kết
> - Bảng yêu cầu: REQUIREMENTS.md
> - Kế hoạch: PROJECT_PLAN.md

### Kết quả đề xuất

Bài nhóm và đặc tả cung cấp nội dung để điền vào khung README gồm mô hình E-Pack B2B, khách hàng là doanh nghiệp vừa và nhỏ, startup, shop online và agency, cùng luồng chọn bao bì, cấu hình, tải thiết kế, xem trước và gửi RFQ. Phản hồi AI gốc cho prompt này chưa được xác nhận.

### Phản biện

Khi đối chiếu, khung prompt minh họa năm thành viên, còn bảng vai trò trong bài Nhóm 01 có bảy thành viên. Tên các công nghệ ngoài phần frontend và liên kết trong repository cần đối chiếu với nhóm trước khi ghi là đã chốt.

### Quyết định của nhóm

Bài nhóm dùng E-Pack làm đề tài và ghi bảy thành viên theo phân công thực tế. Nội dung dùng cho README bám chức năng đã thống nhất trong `REQUIREMENTS.md`. Các liên kết dự kiến theo bài nhóm gồm `REQUIREMENTS.md`, `PROJECT_PLAN.md` và `docs/competitor-analysis.md`.

### Người kiểm tra

Đề xuất Nguyễn Thị Thu Thảo, phụ trách `README.md`, kiểm tra tên thành viên, vai trò, công nghệ và các liên kết.

## Lần sử dụng 5 — Chuẩn bị `PROJECT_PLAN.md`

### Công cụ

Chưa xác nhận tên công cụ riêng cho `PROJECT_PLAN.md`. Bản ghi Gemini của phần R&D được dùng làm nguồn tham khảo chung.

### Mục đích

Chia công việc E-Pack theo giai đoạn, xác định người phụ trách, đầu ra và cách theo dõi tiến độ.

### Prompt

*Dựng lại theo nội dung kế hoạch và bảng phân công trong bài nhóm.*

> Hãy lập `PROJECT_PLAN.md` cho dự án E-Pack của Nhóm 01. Dựa trên `REQUIREMENTS.md` và bảng phân vai, hãy chia kế hoạch thành khảo sát, thiết kế UI/UX, frontend, backend và cơ sở dữ liệu, tích hợp và kiểm thử, rồi triển khai và hoàn thiện. Với mỗi đầu việc, ghi mã, người phụ trách, kết quả cần đạt, thời hạn và trạng thái. Ưu tiên luồng cấu hình bao bì, tải file thiết kế, gửi RFQ, xử lý báo giá và theo dõi đơn. Liệt kê rủi ro và cách xử lý. Ghi các mốc chưa thống nhất là chờ xác nhận.

### Kết quả đề xuất

Tài liệu nhóm nêu các giai đoạn từ khảo sát đến triển khai và các đầu việc về đặc tả, thiết kế giao diện, dữ liệu, frontend và kiểm thử. Bản ghi R&D có đề xuất lộ trình chung. Chưa có phản hồi AI gốc riêng cho `PROJECT_PLAN.md` để xác nhận các mốc và đầu việc.

### Phản biện

Đối chiếu với phạm vi MVP, dựng 3D tương tác, thanh toán tự động và tích hợp phần mềm nhà xưởng sẽ kéo dài tiến độ. Với chức năng phụ thuộc nhiều phần như gửi RFQ, nhóm cần có tiêu chí nghiệm thu từ lúc nhập cấu hình đến lúc lưu yêu cầu để frontend, backend và QA cùng kiểm tra.

### Quyết định của nhóm

Theo bài nhóm, Hậu điều phối kế hoạch và tiến độ. Công việc bám phạm vi MVP đã nêu trong đặc tả, trong đó ưu tiên cấu hình sản phẩm, xử lý RFQ và quản lý đơn hàng. Các mốc thời hạn và trạng thái của từng đầu việc cần đối chiếu với `PROJECT_PLAN.md` hoặc GitHub Issues trước khi xác nhận.

### Người kiểm tra

Đề xuất Nguyễn Phúc Hậu, phụ trách `PROJECT_PLAN.md`, đối chiếu người phụ trách, thời hạn và tiêu chí hoàn thành của từng đầu việc.
