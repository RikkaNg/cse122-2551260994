# Design System – TinHocPortal: Chủ đề "Khám Phá Các Tầng Đại Dương" (Ocean Depth Theme)

Tài liệu thiết kế giao diện cho **TinHocPortal (CSE122)** theo ý tưởng cá nhân hóa hành trình học Tin học đại cương thành **cuộc thám hiểm lặn qua 5 tầng đại dương** — từ vùng nước nông chan hòa ánh sáng đến rãnh đại dương sâu thẳm phát quang sinh học.

---

## 1. Bản đồ 5 Tầng Đại Dương ↔ 5 Chương Tin Học Đại Cương

5 tầng sinh thái biển thực tế (Hải dương học) ánh xạ 1–1 với 5 chủ đề cốt lõi trong đề bài:

| Chương | Tầng Đại Dương | Độ sâu | Chủ đề Tin học đại cương | Màu chủ đạo (Accent) | Màu nền tầng (Surface) | Biểu tượng / Cảm hứng |
| :-: | :--- | :---: | :--- | :--- | :--- | :--- |
| **Chương 1** | **Tầng Mặt Trời** *(Sunlight / Epipelagic)* | `0m – 200m` | **Hệ điều hành & Máy tính cơ bản** | `#0EA5E9` (Sky Cyan) | `#E0F2FE` → `#BAE6FD` | Tia nắng xuyên nước, rạn san hô, cá nhỏ |
| **Chương 2** | **Tầng Chạng Vạng** *(Twilight / Mesopelagic)* | `200m – 1.000m` | **Tin học văn phòng (Word, Excel, PowerPoint)** | `#0284C7` (Ocean Blue) | `#0C4A6E` → `#075985` | Ánh sáng lam dịu, sứa biển, đàn cá di cư |
| **Chương 3** | **Tầng Nửa Đêm** *(Midnight / Bathypelagic)* | `1.000m – 4.000m` | **Mạng máy tính & Internet** | `#38BDF8` (Electric Aqua) | `#082F49` → `#0F172A` | Dòng hải lưu, cáp quang biển, sinh vật phát sáng |
| **Chương 4** | **Tầng Vực Thẳm** *(Abyssal / Abyssopelagic)* | `4.000m – 6.000m` | **An toàn & Bảo mật thông tin** | `#2DD4BF` (Bioluminescent Teal) | `#042F2E` → `#0B1120` | Tàu ngầm chịu áp suất, lớp giáp bảo vệ, radar sonar |
| **Chương 5** | **Tầng Rãnh Đại Dương** *(Hadal / Trenches)* | `6.000m – 11.000m` | **Tư duy thuật toán & Giải quyết vấn đề** | `#A78BFA` (Abyssal Violet) | `#1E1B4B` → `#020617` | Miệng phun thủy nhiệt, phát quang sinh học tím–lục |

### Lý do UX thuyết phục khi thuyết trình / quay OBS
- **Tạo động lực học tập (Gamification tự nhiên):** Sinh viên học xong mỗi bài sẽ thấy **"Độ sâu khám phá (m)"** tăng lên thay vì chỉ là `%` khô khan.
- **Phân tầng độ khó trực quan:** Tầng càng sâu = kiến thức càng nâng cao, màu nền chuyển dần từ sáng trong trẻo (làm quen) sang xanh thẫm phát quang (tư duy sâu).
- **Cá nhân hóa giao diện theo chương:** Khi sinh viên chọn học một chương, bảng màu nhấn (accent), thanh độ sâu (depth gauge) và huy hiệu tầng tự động thay đổi theo tầng đại dương tương ứng.

---

## 2. Bảng màu chuẩn & CSS Tokens

### Màu nền & Chữ (Đảm bảo tương phản WCAG AA ≥ 4.5:1)
> **Nguyên tắc quan trọng:** Dù nền trang mang không khí đại dương (Dark Ocean / Light Seafoam), **khung nội dung bài giảng, bảng biểu và khung mô phỏng phần mềm Word/Excel/PowerPoint** phải giữ bề mặt sạch, độ tương phản cao để sinh viên đọc lâu không mỏi mắt.

```css
:root {
  /* Nền tổng thể (Deep Ocean Mode - Mặc định) */
  --bg-abyss: #020817;
  --bg-deep: #071426;
  --bg-surface: #0D2137;
  --bg-surface-elevated: #132E4A;
  --border-ocean: rgba(56, 189, 248, 0.18);

  /* Chữ */
  --text-primary: #F0F9FF;
  --text-secondary: #94B8D7;
  --text-muted: #6487A8;

  /* Màu nhấn 5 tầng đại dương */
  --zone-1-sunlight: #0EA5E9;   /* Chương 1: Hệ điều hành */
  --zone-2-twilight: #3B82F6;   /* Chương 2: Tin văn phòng */
  --zone-3-midnight: #06B6D4;   /* Chương 3: Mạng máy tính */
  --zone-4-abyssal:  #14B8A6;   /* Chương 4: An toàn thông tin */
  --zone-5-hadal:    #8B5CF6;   /* Chương 5: Tư duy thuật toán */

  /* Màu ngữ nghĩa (Trạng thái bắt buộc Mục 07) */
  --status-success:  #10B981;   /* Hoàn thành / Thành công */
  --status-warning:  #F59E0B;   /* Đang chờ / Cần chú ý */
  --status-danger:   #F43F5E;   /* Lỗi / Bị từ chối */
  --status-disabled: #475569;   /* Vô hiệu hóa / Lưu trữ */
  --status-info:     #38BDF8;   /* Gợi ý / Đang tải */

  /* Khung đọc & Mô phỏng phần mềm (Nền sáng trung tính) */
  --workspace-paper: #FFFFFF;
  --workspace-text:  #0F172A;
}
```

### Chế độ Sáng / Tối (Nên có – Mục 22)
- **Chế độ Mặc định (Deep Ocean):** Nền xanh biển sâu `#071426`, thẻ nổi hiệu ứng kính mờ (glassmorphism nhẹ), ánh sáng phát quang tinh tế.
- **Chế độ Sáng (Sunlight Surface):** Nền trắng pha xanh bọt biển `#F0F9FF`, thẻ trắng `#FFFFFF`, viền `#BAE6FD`, chữ xanh đen `#0C2D48`.

---

## 3. Typography & Khoảng cách
- **Tiêu đề (Headings):** `Be Vietnam Pro` hoặc `Plus Jakarta Sans` (hỗ trợ tiếng Việt chuẩn, nét tròn hiện đại, gọn gàng).
- **Nội dung (Body):** `Inter` hoặc `Be Vietnam Pro` (`16px`, line-height `1.6`).
- **Mã phím tắt / Độ sâu / Công thức Excel:** `JetBrains Mono` (VD: `Ctrl + B`, `=SUM(A1:A5)`, `2.450m`).
- **Bo góc:** Card `16px`, Button/Input `10px`, Badge/Pill `999px`.
- **Hệ lưới Responsive:**
  - Desktop (`≥ 1200px`): Sidebar trái (`260px`) + Nội dung chính + Thanh đo độ sâu (Depth Meter) bên phải hoặc trên header.
  - Tablet (`768px – 1199px`): Sidebar thu gọn thành icon bar (`72px`).
  - Mobile (`< 768px`): Topbar + Drawer menu trượt ngang, card xếp 1 cột.

---

## 4. Cá nhân hóa giao diện theo 4 Vai trò

| Vai trò | Biểu tượng đại dương | Bố cục & Điểm nhấn giao diện |
| :--- | :--- | :--- |
| **Khách** | 🧭 *Người quan sát trên boong tàu* | Landing page cuộn dọc xuyên qua 5 tầng đại dương (từ trời sáng xuống đáy sâu), xem thử bài thực hành mẫu, gửi góp ý chủ đề. |
| **Sinh viên** | 🤿 *Nhà thám hiểm đại dương* | Có **Thước đo độ sâu (Depth Gauge)**, **Sơ đồ lặn 5 tầng (Mindmap)**, nút đổi màu giao diện theo tầng đang học, huy hiệu sinh vật biển khi hoàn thành chương. |
| **Giảng viên** | 🚢 *Thuyền trưởng / Điều phối tàu nghiên cứu* | Giao diện bảng điều khiển tập trung dữ liệu (Sonar Dashboard): quản lý bài giảng/thực hành theo tầng, chấm bài nộp, biểu đồ năng lực lớp theo từng tầng kiến thức. |
| **Quản trị viên** | 📡 *Trạm kiểm soát Hải dương học* | Bố cục quản trị rõ ràng, bảng người dùng, phân quyền, cấu hình chương trình & danh mục phần mềm, trạng thái bật/tắt/lưu trữ. |

---

## 5. Tích hợp 4 Cách Truyền Đạt Kiến Thức (Mục 11) vào Chủ đề Đại Dương

1. **Cách 1 – Mô phỏng thao tác phần mềm (`student-practice-do.html`):**
   - Khung mô phỏng Word/Excel/PowerPoint giữ giao diện quen thuộc (nền sáng chuẩn phần mềm), bao quanh bởi **Bảng điều khiển tàu lặn** gồm danh sách bước thao tác, thanh tiến độ độ sâu và nút phát sáng gợi ý vị trí menu (`Sonar Pulse`).
2. **Cách 2 – Hoạt ảnh hướng dẫn menu / phím tắt (`student-lesson-view.html`):**
   - Hiệu ứng **vòng sóng sonar phát quang** (`sonar-ping` animation) khoanh tròn đúng nút menu cần bấm, kèm thẻ phím tắt nổi (`Ctrl + C`, `Ctrl + S`...).
3. **Cách 3 – Trắc nghiệm nhanh kèm giải thích & Đấu Trùm Cuối Tầng (`student-quiz.html`):**
   - **Trắc nghiệm ôn luyện thường:** Giao diện "Thu thập mẫu vật / Giải mã tín hiệu" — chọn đúng cộng điểm, chọn sai hiện hộp giải thích chi tiết.
   - **Bài kiểm tra tổng kết chương = Đấu Trùm Cuối Tầng Đại Dương (Boss Battle):** Sinh viên dùng kiến thức cả chương để đối đầu sinh vật biểu tượng sống **đúng độ sâu của tầng đó** nhằm mở khóa tầng sâu hơn.
4. **Cách 4 – Sơ đồ tư duy chương trình học (`student-dashboard.html`):**
   - **Bản đồ cắt dọc 5 tầng đại dương (Vertical Ocean Depth Map)**: hiển thị 5 tầng từ `0m` đến `11.000m`, mỗi tầng tỏa nhánh các bài học/thực hành và kết thúc bằng nút **Cổng Đấu Trùm (Boss Gate)** kèm trạng thái: *Đã hạ gục (xanh ngọc)*, *Sẵn sàng khiêu chiến (phát sáng)*, *Chưa mở khóa (xám mờ)*.

---

## 5.1. Hệ thống Trùm Cuối 5 Tầng Đại Dương (Boss Battle – Kiểm tra tổng kết chương)

Mỗi bài kiểm tra tổng kết chương gắn với một loài sinh vật thực tế sinh sống ở đúng tầng đại dương đó:

| Chương | Tầng Đại Dương (Độ sâu) | Trùm cuối (Sinh vật đúng tầng) | Hình tượng gắn với môn học |
| :-: | :--- | :--- | :--- |
| **1** | **Tầng Mặt Trời** (`0 – 200m`) | **Cá Mập Trắng Lớn** *(Great White Shark)* | Vua vùng nước sáng — kiểm tra nền tảng máy tính & hệ điều hành |
| **2** | **Tầng Chạng Vạng** (`200 – 1.000m`) | **Mực Khổng Lồ** *(Giant Squid)* | Nhiều xúc tu linh hoạt — kiểm tra tổng hợp thao tác Word, Excel, PowerPoint |
| **3** | **Tầng Nửa Đêm** (`1.000 – 4.000m`) | **Cá Cần Câu Vực Sâu** *(Deep-sea Anglerfish)* | Đèn phát quang dẫn dụ — kiểm tra kiến thức mạng máy tính & Internet |
| **4** | **Tầng Vực Thẳm** (`4.000 – 6.000m`) | **Cá Răng Nanh Vực Thẳm** *(Abyssal Fangtooth)* | Săn mồi trong bóng tối áp suất cao — kiểm tra an toàn & bảo mật thông tin |
| **5** | **Tầng Rãnh Đại Dương** (`6.000 – 11.000m`) | **Cá Ốc Rãnh Mariana** *(Mariana Snailfish)* | Loài cá sống sâu nhất hành tinh (~8.178m) — thử thách tối thượng về tư duy thuật toán |

### Cơ chế tương tác JS (Dễ code, dễ giải thích khi quay OBS)
- **Thanh máu Trùm (Boss HP):** Tương ứng số câu hỏi tổng kết chương (VD: 5 hoặc 10 câu).
- **Thanh Oxy Tàu Lặn (Player HP):** 3 bình Oxy (trả lời sai tối đa 3 lần).
- **Trả lời đúng:** Tàu lặn bắn sóng Sonar → Trùm mất HP (hiệu ứng rung + thanh máu tụt) → cộng điểm độ sâu.
- **Trả lời sai:** Trùm phản công → giảm 1 bình Oxy + **hiện ngay Hộp Giải Thích** (vì sao sai, đáp án đúng là gì) để củng cố kiến thức.
- **Hạ gục Trùm (`Boss HP = 0`):** Mở khóa tầng đại dương tiếp theo, nhận huy hiệu sinh vật, lưu kết quả vào `quizAttempts`.
- **Cạn Oxy (`Oxy = 0`):** Trạng thái thất bại ("Nổi lên sửa tàu") + gợi ý bài giảng cần ôn lại + nút **Thử lại**.

---

## 6. Bộ 9 Trạng thái UI bắt buộc (Mục 07)
- **Đang tải (Loading):** Skeleton nhấp nháy kiểu gợn sóng nước + spinner radar sonar.
- **Rỗng (Empty):** Minh họa vùng biển trống / tàu lặn tìm kiếm + nút hành động tạo mới hoặc xóa bộ lọc.
- **Thành công (Success):** Toast xanh ngọc `#10B981` + icon tích.
- **Lỗi (Error):** Banner/Toast đỏ san hô `#F43F5E` + nút "Thử lại".
- **Vô hiệu hóa (Disabled):** Giảm độ mờ `opacity: 0.5`, màu `#475569`, không cho click.
- **Đang chờ (Pending):** Badge hổ phách `#F59E0B` (VD: bài nộp đang chờ giảng viên chấm).
- **Bị từ chối (Rejected):** Badge đỏ `#F43F5E` + khung nhận xét lý do từ giảng viên.
- **Hoàn thành (Completed):** Badge xanh ngọc + huy hiệu tầng đại dương.
- **Đã hủy / Lưu trữ (Archived):** Badge xám viền nét đứt, đẩy xuống cuối danh sách hoặc vào tab "Lưu trữ".
