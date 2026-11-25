# Đặc tả đầy đủ BTL: TinHocPortal (CSE122)

- **Học phần:** PHÁT TRIỂN ỨNG DỤNG WEB CƠ BẢN – CSE122
- **Nhóm thực hiện:** 3 sinh viên
- **Loại sản phẩm:** Sản phẩm Web Frontend (nguyên mẫu) có nhiều vai trò, CRUD, responsive, tương tác JavaScript; AI là tùy chọn nâng cao
- **CSDL:** Xây dựng qua mock API (JSON Server / MockAPI / LocalStorage)
- **Nguyên tắc minh chứng:** Mỗi giao diện thực tế đã được duyệt trong bảng kiểm kê màn hình = 1 video OBS giảng giải, trong đó sinh viên phải giải mã và làm lại được những gì đã dựng.

---

## 01. Lĩnh vực
Giáo dục đại học / Tin học đại cương (tin văn phòng Word/Excel/PowerPoint, hệ điều hành, mạng, an toàn thông tin, tư duy thuật toán, ứng dụng phổ thông).

## 02. Tóm tắt sản phẩm
**TinHocPortal** – Hệ thống hỗ trợ giảng dạy và học tập môn Tin học đại cương giúp giảng viên dựng bài giảng, bài thực hành phần mềm, đề kiểm tra và hướng dẫn thao tác, đồng thời giúp sinh viên tiếp thu dễ hiểu qua bài thực hành phần mềm mô phỏng thao tác từng bước, hướng dẫn trực quan, trắc nghiệm và bài tập nộp. Sản phẩm tập trung phát triển frontend nhiều trang, nhiều vai trò, dữ liệu qua mock API.

## 03. Ngữ cảnh
Tin học đại cương là môn bổ trợ bắt buộc cho hầu hết sinh viên các ngành, nội dung gồm tin văn phòng, hệ điều hành, mạng, an toàn thông tin và tư duy thuật toán. Sinh viên đến từ nhiều nền tảng khác nhau nên trình độ không đồng đều, khó bám sát một tốc độ chung. Giảng viên khó hỗ trợ từng thao tác phần mềm, còn tài liệu thực hành phân bố rời rạc, không có kênh tự luyện và đánh giá tiến độ. Vì vậy cần một hệ thống mô phỏng thao tác phần mềm theo từng bước để người học tự luyện mọi nơi.

## 04. Phát biểu vấn đề
- **P1.** Trình độ tin học của sinh viên không đồng đều, gây khó khăn khi phải học theo một tốc độ chung.
- **P2.** Sinh viên khó nhớ thứ tự thao tác trong các phần mềm văn phòng nếu chỉ xem slide tĩnh.
- **P3.** Giảng viên khó thiết kế bài thực hành phần mềm và khó đánh giá mức thao tác của từng sinh viên.
- **P4.** Sinh viên thiếu kênh tra cứu thao tác và tự kiểm tra năng lực theo từng chủ đề.

## 05. Mục tiêu
- **O1.** Biến bài toán dạy–học Tin học đại cương thành sản phẩm Frontend có hành trình người dùng rõ ràng.
- **O2.** Thiết kế đầy đủ giao diện cho từng vai trò: Khách, Sinh viên, Giảng viên, Quản trị viên.
- **O3.** Thể hiện CRUD/trạng thái nghiệp vụ: chương, bài giảng, bài thực hành, đề kiểm tra, nộp bài.
- **O4.** Dùng JavaScript/DOM cho mô phỏng thao tác phần mềm, gợi ý menu, tìm kiếm, lọc, kiểm tra hợp lệ.
- **O5.** Xây dựng dữ liệu qua mock API / LocalStorage / MockAPI (entity + `db.json`).
- **O6.** Thiết kế ít nhất 3 cách truyền đạt kiến thức trực quan (mô phỏng thao tác từng bước, hoạt ảnh giao diện phần mềm, trắc nghiệm/đố nhanh).
- **O7.** Tổ chức làm việc nhóm bằng Trello và Git/GitHub theo nhánh + yêu cầu hợp nhất, kèm video OBS.

## 06. Các vai trò
| Vai trò | Trách nhiệm chính |
| :--- | :--- |
| **Khách** | Xem công khai: giới thiệu khóa, bài thực hành phần mềm mẫu, góp ý chủ đề |
| **Sinh viên** | Học lý thuyết, làm bài thực hành phần mềm mô phỏng, trắc nghiệm, nộp bài, theo dõi tiến độ |
| **Giảng viên** | Xây dựng bài giảng/bài thực hành, soạn đề, chấm bài, quản lý lớp, theo dõi tiến độ |
| **Quản trị viên** | Quản lý tài khoản, chương trình học, danh mục phần mềm, cấu hình hệ thống |

## 07. Hành trình người dùng tổng quát
1. Khám phá / đăng nhập
2. Thực hiện nghiệp vụ chính theo vai trò
3. Xem trạng thái / dữ liệu / phản hồi
4. *(Tùy chọn)* AI hỗ trợ phân tích, gợi ý hoặc tạo nội dung
5. Người dùng Chấp nhận / Sửa / Từ chối / Lưu
6. Vai trò vận hành duyệt / xử lý
7. Bảng điều khiển / báo cáo / hoàn tất

### Nguyên tắc phạm vi – Bắt buộc áp dụng
> **"3 giao diện/vai trò" là ngưỡng tối thiểu chống làm ít, KHÔNG phải mục tiêu.** Phải xây dựng toàn bộ màn hình cần thiết để nghiệp vụ chạy từ đầu đến cuối. Tiêu chí: **ĐỘ ĐẦY ĐỦ CỦA NGHIỆP VỤ > SỐ LƯỢNG GIAO DIỆN.**

- **Bao phủ trạng thái bắt buộc:** Đang tải; Rỗng; Thành công; Lỗi; Vô hiệu hóa; Đang chờ; Bị từ chối; Hoàn thành; Đã hủy/Lưu trữ khi phù hợp.
- **Màn hình dùng chung:** `index.html`, `login.html`, `register.html`, `forgot-password.html`, `profile.html`, `settings.html`, `notifications.html`, `403.html`, `404.html` (xét trong bảng kiểm kê).
- **Lát cắt dọc bắt buộc cho từng sinh viên:** Bản mô phỏng → HTML → CSS → JavaScript → Dữ liệu → Responsive → Nhánh Git → Commit → PR → Video OBS giảng giải. Mỗi sinh viên phải tự hoàn thành ít nhất một luồng end-to-end và giảng giải được nó.
- **(Tùy chọn) Trải nghiệm khi AI thất bại:** Mỗi AI feature cần có trạng thái không đủ dữ liệu / không chắc chắn / lỗi, kèm thao tác Chỉnh sửa / Thử lại / Bỏ qua / Báo cáo / Dùng thủ công.
- **Bảo vệ / Chỉnh sửa ngẫu nhiên:** Giảng viên có thể yêu cầu thay đổi nhỏ 5–10 phút (thêm filter theo phần mềm, đổi table thành card bài thực hành, thêm field + validation, xử lý API rỗng, đổi responsive, thêm trạng thái).

## 08. Danh sách giao diện nền tảng bắt buộc
Chi tiết đầy đủ và bảng theo dõi tiến độ xem tại [screen-list.md](screen-list.md).

- **Khách (3 màn hình):** `visitor-course-overview.html`, `visitor-practice-preview.html`, `visitor-topic-feedback.html`
- **Sinh viên (5 màn hình):** `student-dashboard.html`, `student-lesson-view.html`, `student-practice-do.html`, `student-quiz.html`, `student-submission-result.html`
- **Giảng viên (5 màn hình):** `teacher-dashboard.html`, `teacher-practice-manage.html`, `teacher-lesson-manage.html`, `teacher-grading.html`, `teacher-analysis.html`
- **Quản trị viên (3 màn hình):** `admin-dashboard.html`, `admin-user-management.html`, `admin-curriculum-config.html`

## 09. Chuẩn chi tiết cho TỪNG giao diện đã duyệt
Mỗi màn hình phải có:
- Tệp HTML đúng tên, ngữ nghĩa chuẩn
- Điều hướng nhất quán
- Nội dung chính (card bài thực hành, list chương, mock-up giao diện phần mềm, form hướng dẫn thao tác, dashboard)
- Trạng thái tải / rỗng / lỗi
- Responsive
- Tương tác JS có ý nghĩa (tick bước thực hành, mô phỏng menu phần mềm, kiểm tra kết quả)
- Kiểm tra hợp lệ biểu mẫu (form validation)
- Dữ liệu mock API
- *(Nếu có)* Giao diện AI: Nhập → Xử lý → Kết quả → Giải thích → Người dùng kiểm soát

**Quy tắc CRUD:** `C` = Tạo, `R` = Đọc, `U` = Sửa, `D` = Xóa; với dữ liệu nghiệp vụ thay Xóa bằng **Hủy / Lưu trữ / Vô hiệu hóa / Đóng** khi hợp lý.

## 10. Ma trận thực thể & CRUD gợi ý
| Thực thể | Tạo | Đọc | Sửa | Xóa/Lưu trữ | Ghi chú |
| :--- | :---: | :---: | :---: | :---: | :--- |
| `users` | ✓ | ✓ | ✓ | ✓ / Vô hiệu hóa | Tài khoản theo vai trò (mock data) |
| `chapters` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Chương lý thuyết của môn |
| `lessons` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Bài giảng lý thuyết |
| `practices` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Bài thực hành phần mềm + danh sách bước |
| `submissions` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Kết quả nộp bài thực hành |
| `quizzes` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Câu hỏi trắc nghiệm theo chủ đề |
| `softwareTitles` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Danh mục phần mềm (Word/Excel/PowerPoint…) |
| `quizAttempts` | ✓ | ✓ | ✓ | ✓ / Lưu trữ | Lần làm trắc nghiệm và điểm |

## 11. Kĩ năng truyền đạt kiến thức (Điểm nhấn sáng tạo – 25% điểm)
Tối thiểu **3 cách** truyền đạt trực quan, mỗi cách gắn với một màn hình cụ thể:

1. **Cách 1 – Mô phỏng thao tác phần mềm từng bước (`student-practice-do.html`):** Dựng mock-up giao diện Word/Excel/PowerPoint bằng HTML/CSS, hướng dẫn bấm menu từng bước, tick hoàn thành và kiểm tra kết quả. *Lý do:* sinh viên "tay làm mắt thấy" đúng vị trí nút bấm thay vì nhớ chữ, phù hợp người học đa trình độ.
2. **Cách 2 – Hoạt ảnh hướng dẫn menu/tổ hợp phím (`student-lesson-view.html`):** Mỗi thao tác có hoạt ảnh vòng phóng to vùng menu, hiển thị phím tắt tương ứng. *Lý do:* rút ngắn thời gian tìm nút, tăng tốc độ làm bài thực hành.
3. **Cách 3 – Trắc nghiệm nhanh kèm giải thích (`student-quiz.html`):** Câu hỏi theo chương (thuật ngữ, phím tắt, quy trình), mỗi đáp án sai hiện giải thích. *Lý do:* vừa kiểm tra vừa củng cố ngay những lỗi thường gặp của người mới.
4. **Cách 4 – Sơ đồ tư duy chương trình học (`student-dashboard.html`):** Trực quan hóa cấu trúc chương theo nhánh (tin văn phòng, hệ điều hành, mạng, an toàn, thuật toán). *Lý do:* định vị nhanh chủ đề đã và chưa học, theo dõi tiến độ.

## 12. (Tùy chọn nâng cao) Ý tưởng AI – Không bắt buộc
Nếu làm, cần luồng đầy đủ: `Input → Validation → Processing → Result → Explanation → Accept/Edit/Reject → Save`.
- **AI-1 – AI Software Step Advisor:** Gợi ý chuỗi thao tác đúng và giải thích chọn menu nào theo câu hỏi của sinh viên (JSON cây thao tác / rule-based JS / LLM API tùy chọn).
- **AI-2 – AI Practice Summarizer:** Tóm tắt nội dung và yêu cầu bài thực hành thành các nhiệm vụ ngắn.
- **AI-3 – AI Weakness Detector:** Phân tích kết quả trắc nghiệm/thực hành để nhận diện chủ đề yếu và gợi ý bài luyện tập.

## 13. Dữ liệu giả lập / API
- Triển khai qua file JSON cục bộ, LocalStorage/SessionStorage, JSON Server, MockAPI, public API hoặc LLM API tùy chọn. Không bắt buộc backend thật.
- File `db.json` đặt tại root, gồm 8 entity tối thiểu (`users`, `chapters`, `lessons`, `practices`, `submissions`, `quizzes`, `softwareTitles`, `quizAttempts`), mỗi entity **5–8 bản ghi mẫu** theo môn Tin học đại cương (có `id`, `createdAt`, `updatedAt`).
- Ví dụ `practices`: `{ id, chapterId, software: "Excel", title, steps: [{ text, action }], expectedResult, createdAt, updatedAt }`.

## 14. Gợi ý Prompt & nguyên tắc dùng AI có trách nhiệm
- Viết prompt rõ ngữ cảnh, vai trò, yêu cầu cụ thể, giới hạn phạm vi.
- Hai vòng lặp: (a) tạo bản nháp → (b) yêu cầu AI giải thích / gợi ý cải thiện.
- Không nộp kết quả AI chưa hiểu; phải khai báo đầy đủ trong `docs/ai-usage-report.md`.

## 15–19. Phân công nhóm, GitHub, Trello, Video OBS, Figma/Canva
Xem chi tiết quy trình thực thi tại [team-assignment.md](team-assignment.md).

## 20. Cấu trúc kho mã nguồn gợi ý
```text
project-root/
├── README.md
├── docs/ (project-proposal, screen-list, team-assignment, ai-usage-report)
├── design/ (figma-link.txt, mockups/)
├── pages/
├── assets/ (images, icons, data, software-mockups/)
├── css/ (style.css, responsive.css)
├── js/ (main.js, api.js, modules/)
└── db.json  (mock API – JSON Server / MockAPI)
```

## 21. Khai báo công cụ hỗ trợ (AI Usage Disclosure)
Lưu trong [ai-usage-report.md](ai-usage-report.md): công cụ, prompt chính, phần AI sinh, phần tự chỉnh sửa, lỗi gặp phải, cách kiểm chứng, điều học được, tính năng mock vs thật.

## 22. Phạm vi sản phẩm tối thiểu (MVP)
- **BẮT BUỘC PHẢI CÓ:**
  - Đủ vai trò và toàn bộ màn hình theo bảng kiểm kê.
  - Navigation xuyên suốt; Responsive; CRUD mô phỏng ý nghĩa; Search/filter/form validation (lọc theo phần mềm).
  - Dữ liệu mock API / JSON.
  - Tối thiểu 3 cách truyền đạt kiến thức trực quan (Mục 11).
  - Minh chứng Trello + Git (nhánh/PR) + video OBS giảng giải cho từng màn hình.
  - Khả năng "làm lại được" khi bị hỏi.
- **NÊN CÓ:** Biểu đồ/bảng điều khiển; thông báo nổi; trạng thái rỗng/tải/lỗi; component & token dùng lại; chế độ tối/sáng.
- **CÓ THÌ TỐT:** Ý tưởng AI nâng cao (Mục 12); LLM API thật; PWA; cá nhân hóa lộ trình; tải nguồn thực hành mẫu.

## 23. Tiêu chí duyệt đề
Chuỗi minh chứng liền mạch:
`Ngữ cảnh → Vấn đề → Mục tiêu → Vai trò → Màn hình → Bản mô phỏng → Công việc → Nhánh → Commit → PR → Video OBS giảng giải → Làm lại được → Sản phẩm`

## 24. Đánh giá – Thang điểm gợi ý
- **30%** – Tính đầy đủ nghiệp vụ + chất lượng frontend
- **25%** – Cách truyền đạt kiến thức trực quan (Mục 11)
- **30%** – Video OBS giảng giải + khả năng làm lại khi bảo vệ
- **15%** – Git/GitHub + Trello + AI usage disclosure

## 25. Chuẩn đầu ra mong đợi
Phân tích vấn đề; chia hệ thống thành vai trò/màn hình; thiết kế UI/UX bằng Figma/Canva; hiện thực HTML semantic; CSS/Bootstrap + responsive; JavaScript DOM/sự kiện/biểu mẫu; JSON/mock API; sáng tạo cách truyền đạt kiến thức; Git/GitHub; teamwork; và giảng giải, làm lại được sản phẩm.
