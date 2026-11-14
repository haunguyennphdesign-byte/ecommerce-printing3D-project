# Project Plan — Nền tảng Thương mại Điện tử B2B E-Pack

## 1. Thành viên và vai trò

| STT | Họ và tên | Mã sinh viên | Vai trò dự án | Trách nhiệm chính |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **Nguyễn Huy Cường** | 89252020051 | Tech Lead / Fullstack Dev | Thiết kế kiến trúc hệ thống, phát triển công cụ cấu hình sản phẩm (Configurator) và tính năng Preview 2D/3D; xây dựng website[cite: 1]. |
| 2 | **Nguyễn Phúc Hậu** | 88252020074 | Frontend Developer | Phát triển giao diện người dùng (Frontend), xử lý luồng tương tác tải file thiết kế, tổng hợp và hoàn thiện nội dung kỹ thuật[cite: 1]. |
| 3 | **Nguyễn Thị Minh Hà** | 33261020071 | Project Manager / BA | Quản lý tiến độ chung, phân tích yêu cầu nghiệp vụ, xác định phạm vi hệ thống và tổng hợp, rà soát báo cáo[cite: 1]. |
| 4 | **Đỗ Đức Đạt** | 33252020208 | Market & UX Researcher | Phân tích đối thủ cạnh tranh (Printgo, Pacdora, Packlane...), nghiên cứu hành vi khách hàng B2B và đề xuất luồng trải nghiệm[cite: 1]. |
| 5 | **Nguyễn Thị Thu Thảo** | 88252020056 | Business & Pricing Analyst | Xây dựng logic mô hình doanh thu (hoa hồng, hội phí), cơ sở dữ liệu bảng giá gốc và thuật toán tính giá dự kiến[cite: 1]. |
| 6 | **Trần Thị Yến Như** | 33252020056 | Financial & Resource Planner | Hoạch định nguồn lực, dự toán chi phí hạ tầng/vận hành và phân tích tính khả thi tài chính của dự án[cite: 1]. |
| 7 | **Nguyễn Thị Khánh Vi** | 88254020199 | Legal & QA Compliance | Rà soát tuân thủ pháp lý TMĐT, bảo vệ dữ liệu cá nhân, bảo mật file thiết kế, sở hữu trí tuệ và kiểm thử quy trình[cite: 1]. |

---

## 2. Các giai đoạn

Dự án phát triển nền tảng **E-Pack** xuyên suốt học phần được chia thành 6 giai đoạn chính[cite: 1]:

- **Giai đoạn 1: Khảo sát và xác định yêu cầu.** Nghiên cứu thực trạng ngành bao bì/in ấn B2B, phân tích đối thủ, xác định 4 nhóm sản phẩm cốt lõi (hộp giấy, túi giấy, tube giấy, nhãn in), phân quyền người dùng và quy trình đặt hàng 7 bước[cite: 1].
- **Giai đoạn 2: Thiết kế giao diện.** Xây dựng sơ đồ chức năng hệ thống, thiết kế wireframe và layout UI/UX trên Figma cho các màn hình chính (Trang chủ, Trang cấu hình 2D/3D, Hộp thoại RFQ, Dashboard nhà cung cấp)[cite: 1].
- **Giai đoạn 3: Xây dựng các chức năng frontend.** Phát triển giao diện web tương tác, form nhập thông số kỹ thuật, khu vực hiển thị Preview 2D/3D và bảng tính giá dự kiến tức thì[cite: 1].
- **Giai đoạn 4: Phát triển backend và cơ sở dữ liệu.** Thiết kế cơ sở dữ liệu dùng chung (người dùng, cấu hình sản phẩm, bảng giá xưởng, đơn hàng/RFQ), xây dựng API xử lý tính giá dự kiến và kiểm tra file (Preflight cơ bản)[cite: 1].
- **Giai đoạn 5: Tích hợp và kiểm thử.** Kết nối Frontend với Backend, kiểm thử luồng đặt hàng 7 bước từ khách hàng sang nhà cung cấp, kiểm tra tính chính xác của công thức báo giá và rà soát lỗ hổng bảo mật file thiết kế[cite: 1].
- **Giai đoạn 6: Triển khai và hoàn thiện.** Đưa phiên bản minh họa/thử nghiệm lên môi trường trực tuyến (Google Sites / Web Hosting), chạy thử nghiệm kịch bản thực tế (Pilot) và hoàn thiện tài liệu đồ án[cite: 1].

---

## 3. Công việc

| Mã CV | Tên công việc | Giai đoạn | Người phụ trách | Kết quả cần đạt | Thời hạn | Trạng thái |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **W01** | Khảo sát thị trường, phân tích đối thủ & chốt đề tài E-Pack | GĐ 1 | Nguyễn Thị Minh Hà, Đỗ Đức Đạt | Tài liệu đặc tả vấn đề kinh doanh, bảng so sánh đối thủ và phạm vi 4 nhóm sản phẩm[cite: 1]. | Buổi 1 – 2 | Hoàn thành |
| **W02** | Xây dựng mô hình doanh thu, logic tính giá & pháp lý TMĐT | GĐ 1 | Nguyễn Thị Thu Thảo, Nguyễn Thị Khánh Vi, Trần Thị Yến Như | Công thức tính giá dự kiến, quy định bảo mật file thiết kế & tuân thủ Luật TMĐT[cite: 1]. | Buổi 2 – 3 | Hoàn thành |
| **W03** | Thiết kế sơ đồ hệ thống & Layout giao diện trên Figma | GĐ 2 | Nguyễn Huy Cường, Nguyễn Phúc Hậu | Sơ đồ chức năng 3 vai trò và bộ layout hoàn chỉnh cho luồng cấu hình 4 bước[cite: 1]. | Buổi 3 – 4 | Hoàn thành |
| **W04** | Xây dựng giao diện Trang chủ, Danh mục & Trang Cấu hình sản phẩm | GĐ 3 | Nguyễn Phúc Hậu | Giao diện web hiển thị đầy đủ form nhập thông số (kích thước, chất liệu, số lượng, gia công)[cite: 1]. | Buổi 5 – 6 | Hoàn thành |
| **W05** | Phát triển tính năng Preview 2D/3D & Tải file thiết kế | GĐ 3 | Nguyễn Huy Cường | Cho phép tải file (PNG, JPG, SVG, PDF, AI) và hiển thị mô phỏng 2D/3D trên khung nhìn[cite: 1]. | Buổi 6 – 7 | Đang thực hiện |
| **W06** | Thiết kế CSDL & API báo giá dự kiến, lưu trữ yêu cầu RFQ | GĐ 4 | Nguyễn Huy Cường, Nguyễn Thị Thu Thảo | Cơ sở dữ liệu lưu cấu hình/đơn hàng và logic cập nhật giá dự kiến theo thông số[cite: 1]. | Buổi 7 – 8 | Đang thực hiện |
| **W07** | Tích hợp luồng đặt hàng, kiểm thử (QA) & rà soát bảo mật | GĐ 5 | Nguyễn Thị Khánh Vi, Nguyễn Phúc Hậu | Báo cáo kiểm thử chức năng Preflight, luồng gửi RFQ và phân quyền truy cập file[cite: 1]. | Buổi 9 – 10 | Chưa bắt đầu |
| **W08** | Triển khai website minh họa & hoàn thiện báo cáo tổng kết | GĐ 6 | Toàn bộ Nhóm 04 | Website hoạt động ổn định, hoàn tất tài liệu `PROJECT_PLAN.md` và báo cáo đồ án[cite: 1]. | Buổi 11 – 12 | Chưa bắt đầu |

---

## 4. Rủi ro

| STT | Rủi ro nhận diện | Mức độ ảnh hưởng | Phương án xử lý & Giảm thiểu |
| :--- | :--- | :--- | :--- |
| 1 | **Hạn chế năng lực công nghệ lõi (3D thực & thuật toán khuôn bế):** Dựng mô hình 3D động và tự động tạo khuôn bế (dieline) phức tạp vượt quá thời gian và nguồn lực của học phần[cite: 1]. | Cao | Giới hạn phạm vi phiên bản đầu: sử dụng bộ khuôn dựng sẵn cho 4 nhóm sản phẩm cơ bản, hiển thị 3D ở mức ghép thiết kế minh họa lên mẫu cố định; đưa tính năng dựng 3D thực và tự động tạo khuôn bế vào giai đoạn mở rộng[cite: 1]. |
| 2 | **Sai lệch giữa giá dự kiến và báo giá chính thức của xưởng:** Giá bao bì thực tế phụ thuộc nhiều biến số (độ phủ mực, bản kẽm, biến động giá giấy) dễ gây mất niềm tin nếu lệch quá nhiều[cite: 1]. | Cao | Ghi chú rõ mức giá hiển thị trên hệ thống là *giá dự kiến tham khảo*; quy định ngưỡng cảnh báo nếu giá chính thức từ xưởng lệch quá 10% để khách hàng chủ động cân đối trước khi chốt đơn[cite: 1]. |
| 3 | **Rủi ro bảo mật file thiết kế & quyền sở hữu trí tuệ:** File thiết kế của doanh nghiệp chứa logo, mẫu mã sản phẩm mới chưa ra mắt dễ bị rò rỉ nếu không kiểm soát chặt[cite: 1]. | Trung bình | Áp dụng cơ chế xác thực tài khoản, phân quyền truy cập (chỉ chủ đơn, quản trị viên xử lý và xưởng được chỉ định mới được xem/tải file) và thiết lập chính sách xóa file định kỳ sau khi hoàn tất đơn[cite: 1]. |
| 4 | **Giao dịch ngoài nền tảng để né phí (Disintermediation):** Khách hàng và xưởng in tự liên hệ trực tiếp cho các đơn đặt lại sau lần giao dịch đầu tiên[cite: 1]. | Trung bình | Che thông tin liên hệ trực tiếp trước khi xác nhận đơn; tích hợp tính năng *Đặt lại một chạm* (lưu sẵn cấu hình và file thiết kế) cùng ưu đãi tích điểm để tạo sự tiện lợi khi giao dịch trên sàn[cite: 1]. |
| 5 | **Tiến độ triển khai gấp rút và phụ thuộc việc kiêm nhiệm:** Thành viên nhóm phải kiêm nhiệm nhiều vai trò (lập trình, phân tích, tài chính) trong thời gian học phần ngắn[cite: 1]. | Trung bình | Chia nhỏ công việc theo từng buổi học, ưu tiên hoàn thiện các chức năng cốt lõi (MVP) trước và kiểm tra tiến độ định kỳ hằng tuần thông qua Project Manager[cite: 1]. |