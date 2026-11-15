# AI Usage Log

**Dự án:** E-Pack — Nền tảng thương mại điện tử B2B cho bao bì và in ấn theo yêu cầu  
**Môn học:** Phát triển ứng dụng thương mại điện tử · **Nhóm:** 01

Các mục ghi theo đầu việc. Prompt gốc được chép từ ảnh hoặc bản ghi. Prompt dựng lại dựa trên bài nhóm và cần người phụ trách xác nhận. Tên công cụ chưa có trong tài liệu được ghi là “Chưa xác nhận”. Tên ở mục Người kiểm tra là người phụ trách được đề xuất đối chiếu.

## Lần sử dụng 1 — Phân tích yêu cầu cho `REQUIREMENTS.md`

### Công cụ

Công cụ AI phân tích yêu cầu Chat GPT.

### Mục đích

Chuyển bài toán đặt bao bì theo yêu cầu thành phạm vi triển khai, vai trò người dùng và danh sách yêu cầu có thể nghiệm thu.

### Prompt

*Dựng lại theo mẫu phân tích yêu cầu trong bài nhóm và bản đặc tả.*

> Bạn là chuyên gia phân tích nghiệp vụ cho dự án E-Pack, nền tảng kết nối doanh nghiệp cần đặt bao bì với xưởng in. Dựa vào bài nhóm và khảo sát Pacdora, Packhelp, Packlane, hãy trình bày mục tiêu, phạm vi MVP, vai trò và quyền hạn, chức năng, quy trình nghiệp vụ chính, yêu cầu phi chức năng và rủi ro. Lập bảng chức năng F01–F10 có người sử dụng, mức ưu tiên và tiêu chí nghiệm thu. Phân biệt các tính năng cần cho phiên bản đầu với các tính năng có thể làm sau.

### Kết quả đề xuất

Bản phân tích đưa ra danh mục bốn loại bao bì, chức năng tài khoản, cấu hình thông số, gửi yêu cầu báo giá (RFQ), quản lý báo giá, theo dõi đơn và quản trị. Bản `REQUIREMENTS.md` tổng hợp các chức năng thành F01–F10, gắn với vai trò và các bước nghiệp vụ.

### Phản biện

Bảng phản biện của nhóm chỉ ra quyền giữa Sales và Admin còn chồng lấn, cấu hình đầy đủ cả bốn loại bao bì vượt sức nhóm và luồng báo giá chưa phân định rõ giá dự kiến với báo giá chính thức.

### Quyết định của nhóm

Giữ bốn danh mục và ưu tiên cấu hình chi tiết cho hộp giấy, túi giấy. Khách có thể xem và dùng thử cấu hình, nhưng cần đăng nhập để gửi RFQ. Trong MVP, Admin kiêm nhiệm vụ hỗ trợ bán hàng. Chức năng mở rộng như cổng thanh toán trực tuyến và tạo khuôn bế tự động được đưa ra khỏi phạm vi nghiệm thu MVP.

### Người kiểm tra

Đề xuất Trần Thị Yến Như, phụ trách `REQUIREMENTS.md`, đối chiếu mã chức năng, quyền hạn và tiêu chí nghiệm thu.

## Lần sử dụng 2 — Phản biện yêu cầu và chốt phạm vi MVP

### Công cụ

Công cụ AI phản biện độc lập (chưa xác nhận tên).

### Mục đích

Kiểm tra đề xuất ban đầu về tính khả thi, các bước nghiệp vụ còn thiếu và tiêu chí nghiệm thu trước khi chốt yêu cầu.

### Prompt

*Dựng lại theo mẫu phản biện và bảng kết quả trong bài nhóm.*

> Hãy phản biện độc lập bản yêu cầu của E-Pack dựa trên bài toán đặt bao bì B2B và quy mô nhóm sinh viên. Với từng chức năng, chỉ ra yêu cầu trùng lặp, vượt phạm vi, bước nghiệp vụ còn thiếu, rủi ro về dữ liệu và điểm chưa đủ rõ để lập trình hoặc kiểm thử. Hãy nêu lý do và đề xuất giữ, sửa, bổ sung hoặc chuyển sang giai đoạn sau. Tập trung vào quyền gửi RFQ, cấu hình sản phẩm, xem trước, tải file, báo giá và quy trình trước sản xuất.

### Kết quả đề xuất

Công cụ phản biện chỉ ra bản đầu thiếu bước đặt cọc và duyệt bản in, chưa quy định hiệu lực báo giá, và giả định hệ thống có thể tự cập nhật tiến độ sản xuất dù MVP chưa tích hợp phần mềm nhà xưởng. Bảng phản biện cũng đề xuất kiểm tra tệp ở backend và lưu tệp thiết kế riêng tư.

### Phản biện

Bảng quyết định của nhóm ghi nhận phản biện theo từng chức năng. Ví dụ, ảnh mockup cố định chưa thể hiện được logo và kích thước khách đã chọn. Trình xem 3D chuyên sâu lại vượt phạm vi học phần. Phương án nhóm ghi nhận là xem trước 2D cơ bản với logo và kích thước.

### Quyết định của nhóm

Phân biệt giá tham khảo do hệ thống ước tính với báo giá chính thức. Quy định báo giá có hiệu lực 7 ngày và cho phép khách yêu cầu điều chỉnh. Bổ sung bước đặt cọc qua QR và tải biên lai để Admin duyệt, tiếp đến là duyệt bản in trước sản xuất. Tiến độ đơn được cập nhật thủ công. Tệp thiết kế được kiểm tra ở backend và lưu riêng tư.

### Người kiểm tra

Đề xuất Trần Thị Yến Như đối chiếu đặc tả với bảng phản biện và Nguyễn Phúc Hậu kiểm tra các quyết định ảnh hưởng đến tiến độ.

## Lần sử dụng 3 — Chuẩn bị `AGENTS.md`

### Công cụ

Gemini

### Mục đích

Xin bản nháp về kế hoạch R&D và các nguyên tắc phối hợp với AI để tham khảo khi soạn `AGENTS.md`.

### Prompt

> Hãy lập kế hoạchR$D cho thương hiệumin 3D tôi đã đề cập truóc đó, để tôi hoàn thành bài tập nghiên cứu phát triển web thương mại điện tử.

### Kết quả đề xuất

Gemini đề xuất nguyên tắc viết mã dễ bảo trì, thực hiện thay đổi nhỏ, đọc tài liệu và đề xuất phương án trước khi sửa code. Sau khi sửa, cần nêu tệp đã chỉnh, cách chạy và cách kiểm thử. Kết quả cũng có gợi ý dùng dữ liệu mẫu, bảo vệ thông tin đăng nhập và chia công việc thành các giai đoạn R&D.

### Phản biện

Đối chiếu với `REQUIREMENTS.md`, bản trả lời của Gemini dùng ví dụ giỏ hàng và thanh toán giả lập theo luồng TMĐT thông thường. E-Pack tập trung vào cấu hình bao bì, gửi RFQ và báo giá. Đây là điểm cần chỉnh khi áp dụng bản nháp vào dự án.

### Quyết định của nhóm

Phần hướng dẫn trong bài nhóm bám phạm vi `REQUIREMENTS.md` và giữ các quy tắc về đọc tài liệu, đề xuất phương án, xác nhận trước khi sửa, báo cáo thay đổi và hướng dẫn kiểm thử. Các ví dụ nghiệp vụ trong bản nháp Gemini cần được đối chiếu với luồng E-Pack trước khi đưa vào `AGENTS.md`.

### Người kiểm tra

Đề xuất Thiện Nhân, phụ trách `AGENTS.md`, đối chiếu nội dung với phạm vi và quy trình của nhóm.

## Lần sử dụng 4 — Chuẩn bị `README.md`

### Công cụ

Gemini
### Mục đích

Soạn trang giới thiệu repository để người đọc hiểu đề tài, khách hàng mục tiêu, chức năng, thành viên, công nghệ dự kiến và hướng triển khai.

### Prompt
# Tên dự án

## 1. Giới thiệu
Mô tả website và vấn đề kinh doanh cần giải quyết.

## 2. Khách hàng mục tiêu
Mô tả nhóm người dùng chính.
## 3. Chức năng chính
Liệt kê các chức năng dự kiến.

## 4. Thành viên
- Thành viên 1 – Vai trò
- Thành viên 2 – Vai trò
- Thành viên 3 – Vai trò
- Thành viên 4 – Vai trò
- Thành viên 5 – Vai trò

## 5. Công nghệ dự kiến
Ghi rõ công nghệ đã thống nhất.

## 6. Kế hoạch thực hiện
Tóm tắt các giai đoạn của dự án.

## 7. Liên kết
- Bảng yêu cầu: REQUIREMENTS.md
- Kế hoạch: PROJECT_PLAN.md

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

Gemini

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
