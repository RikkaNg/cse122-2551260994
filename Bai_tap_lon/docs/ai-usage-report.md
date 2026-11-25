# Báo cáo khai báo sử dụng AI (AI Usage Disclosure)

> Tài liệu bắt buộc theo Mục 14 & Mục 21 của đề tài **TinHocPortal – CSE122**.
> Nguyên tắc: Không nộp kết quả AI mà sinh viên chưa hiểu; mọi kết quả AI phải được kiểm chứng, tự chỉnh sửa và giải thích lại được.

## 1. Danh sách công cụ AI đã sử dụng
| Công cụ | Mục đích sử dụng | Thành viên sử dụng |
| :--- | :--- | :--- |
| *(VD: Gemini / ChatGPT / Copilot...)* | *(Gợi ý cấu trúc, tạo dữ liệu mẫu db.json, giải thích JS...)* | SV1 / SV2 / SV3 |

## 2. Nhật ký Prompt & Kiểm chứng

### Mục 1 – *(Tên tính năng / màn hình)*
- **Công cụ:** 
- **Prompt chính:**
  > *(Ghi lại prompt đã dùng)*
- **Phần AI sinh ra:** 
- **Phần sinh viên tự chỉnh sửa:** 
- **Lỗi gặp phải (nếu có):** 
- **Cách kiểm chứng (chạy thử, test edge-case):** 
- **Điều học được:** 

---

## 3. Phân biệt tính năng Mock vs Thật
| Tính năng | Trạng thái (Mock / Thật) | Cách triển khai hiện tại |
| :--- | :---: | :--- |
| Xác thực đăng nhập / phân quyền | Mock | Kiểm tra đối chiếu với `users` trong `db.json` / `LocalStorage` |
| Dữ liệu khóa học, bài giảng, thực hành | Mock | JSON Server / `db.json` + `LocalStorage` |
| Mô phỏng thao tác phần mềm | Thật (Frontend JS) | HTML/CSS mockup + JavaScript DOM bắt sự kiện click menu |
| Tính năng AI *(nếu có)* | Mock / API | *(Ghi rõ rule-based JSON hay gọi LLM API thật)* |
