# Phân công nhóm, Quy trình Git, Trello & Video OBS

## 1. Phân công 3 sinh viên

| Thành viên | Phạm vi màn hình chính | Trách nhiệm chéo bắt buộc |
| :--- | :--- | :--- |
| **SV1** | **Khách** (`visitor-*`) + **Sinh viên** (bài giảng, thực hành phần mềm, bảng điều khiển) + một phần màn hình dùng chung (`login`, `register`, `forgot-password`) | Mô phỏng menu phần mềm, giao diện dùng chung, responsive |
| **SV2** | **Quản trị viên** (`admin-*`) + **Sinh viên** (trắc nghiệm, nộp bài & kết quả) + `profile`, `notifications` | JavaScript / dữ liệu / Mock API (`db.json`, `api.js`); review PR |
| **SV3** | **Giảng viên** (`teacher-*`) + `index`, `settings`, `403`, `404` | Hệ thống thiết kế / điều hướng / accessibility / tích hợp nhất quán & phát hành |

> **Yêu cầu lát cắt dọc bắt buộc:** Mỗi sinh viên đều phải có đủ: `Mockup → HTML → CSS → JavaScript → Dữ liệu → Responsive → Nhánh Git → Commit → PR → Video OBS giảng giải → Làm lại được`.

---

## 2. Quy trình Git / GitHub
- **Tên repo gợi ý:** `cse122-tinhocportal-teamXX`
- **Cấu trúc nhánh:**
  - `main`: Bản ổn định đã kiểm thử
  - `dev`: Nhánh tích hợp chính
  - `feature/<ten-man-hinh>`: Nhánh tính năng (VD: `feature/student-practice-do`, `feature/teacher-practice-manage`, `feature/admin-curriculum-config`)
- **Luồng làm việc:** `Task → Branch → Code → Commit → Push → PR → Review → Merge dev → Test → Merge main`
- **Quy chuẩn Commit (Conventional Commits):**
  - Hợp lệ: `feat:`, `fix:`, `style:`, `refactor:`, `docs:`
  - **Cấm:** `update`, `done`, `final`, `fix code`, spam commit.

---

## 3. Bảng công việc (Trello / Jira / Notion)
- **Các cột bắt buộc:** `TỒN ĐỌNG` → `CẦN LÀM` → `ĐANG LÀM` → `CHỜ DUYỆT` → `HOÀN THÀNH`
- **Thông tin trên mỗi thẻ (card):** Mã task, tên tệp/giao diện, người phụ trách, deadline, tên nhánh, link PR/commit, link video OBS.
- **Task mẫu:**
  - `TASK-01`: Mockup màn hình thực hành (Figma/Canva)
  - `TASK-02`: HTML vai trò Sinh viên
  - `TASK-03`: Responsive CSS
  - `TASK-04`: JS mô phỏng thao tác phần mềm
  - `TASK-05`: Mock API (`db.json` + `api.js`)
  - `TASK-06`: *(Tùy chọn)* Tính năng AI
  - `TASK-07`: Kiểm thử đa trình duyệt & responsive
  - `TASK-08`: Quay video OBS + cập nhật README/Docs

---

## 4. Thiết kế Figma / Canva trước khi code
Cần chuẩn bị và lưu link vào `design/figma-link.txt`, ảnh xuất vào `design/mockups/`:
- Sơ đồ trang (Sitemap) & Luồng người dùng (User flow)
- Bảng kiểm kê màn hình
- Wireframe & Mockup Desktop + bản Responsive
- Hướng dẫn thành phần tối thiểu (Design system / Component kit)
- Trạng thái tải / rỗng / lỗi
- Mockup tương tác cho màn hình thực hành phần mềm

---

## 5. Quy định Video OBS giảng giải (30% điểm)
**Mỗi giao diện đã duyệt = 1 video OBS.**

### Quy tắc đặt tên file
- `SV1-01-student-practice-do.mp4`
- `SV2-01-admin-user-management.mp4`
- `SV3-01-teacher-practice-manage.mp4`

### Checklist nội dung bắt buộc trong mỗi video
1. Có **khuôn mặt + giọng nói** của sinh viên giải thích.
2. Mở **mockup Figma/Canva** và giải thích vì sao thiết kế bố cục như vậy.
3. Mở đúng tệp **HTML / CSS / JS** tương ứng.
4. Giải thích **layout + logic nghiệp vụ + ý nghĩa từng phần UI** (mock-up giao diện phần mềm, nút tick bước, nút nộp bài...).
5. **Thực hiện một thay đổi nhỏ tại chỗ** (VD: thêm bước thao tác, đổi vị trí menu, thêm câu hỏi, thêm filter...) rồi chạy lại để chứng minh.
6. **Commit thay đổi lên GitHub**, nêu rõ mã task / nhánh / commit message.
7. Làm lại một thao tác theo yêu cầu của giảng viên hoặc nhóm để chứng minh **"hiểu và làm lại được"**.
