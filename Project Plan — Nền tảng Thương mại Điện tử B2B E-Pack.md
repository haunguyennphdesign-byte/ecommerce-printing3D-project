# Project Plan — Nền tảng Thương mại Điện tử B2B E-Pack

## 1. Thành viên và vai trò

Dựa trên cơ cấu phân công nhiệm vụ của nhóm phát triển:

| Vai trò | Trách nhiệm |
| :--- | :--- |
| **Nguyễn Phúc Hậu** <br>– Trưởng nhóm/BA[cite: 2] | Quản lý tiến độ, yêu cầu, GitHub Issues và điều phối nhóm[cite: 2]. |
| **Trần Thị Yến Như, Hoàng Nguyễn Lan Hà** <br>– UI/UX[cite: 2] | Khảo sát giao diện, đề xuất thiết kế và chuẩn bị tài nguyên[cite: 2]. |
| **Lê Võ Thiện Nhân** <br>– Frontend[cite: 2] | Xây dựng giao diện HTML/CSS/JavaScript[cite: 2]. |
| **Nguyễn Phúc Hậu, Nguyễn Huy Cường** <br>– Backend/Database[cite: 2] | Thiết kế dữ liệu, nghiệp vụ và API[cite: 2]. |
| **Trần Thị Kim Thanh, Nguyễn Thị Thu Thảo** <br>– QA/Integration[cite: 2] | Lập kế hoạch kiểm thử, kiểm tra tích hợp và tài liệu[cite: 2]. |

---

## 2. Các giai đoạn

Dự án phát triển nền tảng **E-Pack** xuyên suốt học phần được chia thành các giai đoạn chính[cite: 1]:

- **Giai đoạn 1: Khảo sát và xác định yêu cầu.** Nghiên cứu thực trạng thị trường bao bì/in ấn B2B, phân tích đối thủ, xác định 4 nhóm sản phẩm cốt lõi (hộp giấy, túi giấy, tube giấy, nhãn in) và quy trình đặt hàng[cite: 1].
- **Giai đoạn 2: Thiết kế giao diện.** Xây dựng sơ đồ chức năng hệ thống, thiết kế wireframe và layout UI/UX trên Figma cho các màn hình chính của nền tảng[cite: 1].
- **Giai đoạn 3: Xây dựng các chức năng frontend.** Phát triển giao diện web tương tác, form nhập thông số kỹ thuật, khu vực hiển thị Preview 2D/3D và bảng tính giá dự kiến tức thì[cite: 1].
- **Giai đoạn 4: Phát triển backend và cơ sở dữ liệu.** Thiết kế cơ sở dữ liệu dùng chung (người dùng, cấu hình sản phẩm, bảng giá xưởng, đơn hàng), xây dựng API xử lý và kiểm tra file thiết kế[cite: 1].
- **Giai đoạn 5: Tích hợp và kiểm thử.** Kết nối Frontend với Backend, kiểm thử luồng đặt hàng từ khách hàng sang nhà cung cấp và rà soát bảo mật[cite: 1].
- **Giai đoạn 6: Triển khai và hoàn thiện.** Đưa phiên bản minh họa/thử nghiệm lên môi trường trực tuyến, chạy thử nghiệm kịch bản thực tế (Pilot) và hoàn thiện tài liệu đồ án[cite: 1].

---

## 3. Công việc

| Mã CV | Tên công việc | Giai đoạn | Người phụ trách | Kết quả cần đạt | Trạng thái |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **W01** | Khảo sát thị trường, phân tích đối thủ & chốt đề tài E-Pack | Giai đoạn 1 | Nguyễn Phúc Hậu, Nhóm BA | Tài liệu đặc tả vấn đề kinh doanh, bảng so sánh đối thủ và phạm vi sản phẩm[cite: 1, 2]. | Hoàn thành |
| **W02** | Xây dựng mô hình doanh thu, logic tính giá & quy chế pháp lý | Giai đoạn 1 | Nguyễn Thị Thu Thảo, Nhóm QA/Integration | Công thức tính giá dự kiến, quy định bảo mật file thiết kế & tuân thủ Luật TMĐT[cite: 1, 2]. | Hoàn thành |
| **W03** | Thiết kế sơ đồ hệ thống & Layout giao diện trên Figma | Giai đoạn 2 | Trần Thị Yến Như, Hoàng Nguyễn Lan Hà | Sơ đồ chức năng các vai trò và bộ layout hoàn chỉnh cho luồng cấu hình sản phẩm[cite: 1, 2]. | Hoàn thành |
| **W04** | Xây dựng giao diện Trang chủ, Danh mục & Trang Cấu hình sản phẩm | Giai đoạn 3 | Lê Võ Thiện Nhân | Giao diện web hiển thị đầy đủ form nhập thông số kỹ thuật[cite: 1, 2]. | Đang thực hiện |
| **W05** | Phát triển tính năng Preview 2D/3D & Tải file thiết kế | Giai đoạn 3 | Lê Võ Thiện Nhân, Nguyễn Huy Cường | Cho phép tải file thiết kế và hiển thị mô phỏng 2D/3D trên khung nhìn[cite: 1, 2]. | Đang thực hiện |
| **W06** | Thiết kế CSDL & API báo giá dự kiến, lưu trữ yêu cầu | Giai đoạn 4 | Nguyễn Phúc Hậu, Nguyễn Huy Cường | Cơ sở dữ liệu lưu cấu hình/đơn hàng và logic cập nhật giá dự kiến theo thông số[cite: 1, 2]. | Đang thực hiện |
| **W07** | Tích hợp luồng đặt hàng, kiểm thử (QA) & rà soát bảo mật | Giai đoạn 5 | Trần Thị Kim Thanh, Nguyễn Thị Thu Thảo | Báo cáo kiểm thử chức năng, luồng gửi yêu cầu và phân quyền truy cập[cite: 1, 2]. | Chưa bắt đầu |
| **W08** | Triển khai website minh họa & hoàn thiện báo cáo tổng kết | Giai đoạn 6 | Toàn bộ thành viên nhóm | Website hoạt động ổn định, hoàn tất tài liệu `PROJECT_PLAN.md` và báo cáo đồ án[cite: 1, 2]. | Chưa bắt đầu |

---

## 4. Rủi ro

| STT | Rủi ro nhận diện | Mức độ ảnh hưởng | Phương án xử lý & Giảm thiểu |
| :--- | :--- | :--- | :--- |
| 1 | **Hạn chế năng lực công nghệ lõi (3D thực & thuật toán khuôn bế):** Dựng mô hình 3D động và tự động tạo khuôn bế phức tạp vượt quá thời gian phát triển[cite: 1]. | Cao | Giới hạn phạm vi phiên bản đầu: sử dụng bộ khuôn dựng sẵn cho các nhóm sản phẩm cơ bản, hiển thị 3D ở mức ghép thiết kế minh họa lên mẫu cố định[cite: 1]. |
| 2 | **Sai lệch giữa giá dự kiến và báo giá chính thức của xưởng:** Giá bao bì thực tế phụ thuộc nhiều biến số (độ phủ mực, bản kẽm, biến động giá giấy) dễ gây mất niềm tin[cite: 1]. | Cao | Ghi chú rõ mức giá hiển thị trên hệ thống là *giá dự kiến tham khảo*; quy định ngưỡng cảnh báo nếu giá chính thức từ xưởng lệch quá 10% để khách hàng cân đối[cite: 1]. |
| 3 | **Rủi ro bảo mật file thiết kế & quyền sở hữu trí tuệ:** File thiết kế chứa logo, mẫu mã sản phẩm mới chưa ra mắt dễ bị rò rỉ nếu không kiểm soát chặt[cite: 1]. | Trung bình | Áp dụng cơ chế xác thực tài khoản, phân quyền truy cập (chỉ chủ đơn, quản trị viên xử lý và xưởng được chỉ định mới được xem/tải file)[cite: 1]. |
| 4 | **Giao dịch ngoài nền tảng để né phí (Disintermediation):** Khách hàng và xưởng in tự liên hệ trực tiếp cho các đơn đặt lại sau lần giao dịch đầu tiên[cite: 1]. | Trung bình | Che thông tin liên hệ trực tiếp trước khi xác nhận đơn; tích hợp tính năng *Đặt lại một chạm* (lưu sẵn cấu hình và file) cùng ưu đãi tích điểm[cite: 1]. |
| 5 | **Tiến độ triển khai gấp rút và phân bổ công việc:** Khối lượng công việc lập trình và kiểm thử lớn chia đều cho các nhóm chức năng[cite: 1]. | Trung bình | Phân chia rõ ràng trách nhiệm cho từng vị trí (UI/UX, Frontend, Backend, QA) và họp nhóm định kỳ để kiểm soát tiến độ qua GitHub Issues[cite: 1, 2]. |