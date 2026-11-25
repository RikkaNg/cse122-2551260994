# Bảng kiểm kê màn hình – TinHocPortal (CSE122)

> **Nguyên tắc:** ĐỘ ĐẦY ĐỦ CỦA NGHIỆP VỤ > SỐ LƯỢNG GIAO DIỆN. Mỗi màn hình được duyệt = 1 video OBS giảng giải.

## 1. Màn hình nền tảng theo 4 vai trò (16 màn hình)

### Khách (3 màn hình)
| # | Tệp | Giao diện | CRUD / Trạng thái | Chức năng chính | Phụ trách | Trạng thái |
| :-: | :--- | :--- | :--- | :--- | :-: | :-: |
| 1 | `visitor-course-overview.html` | Tổng quan khóa | R | Xem tổng quan chương trình Tin học đại cương | SV1 | [ ] |
| 2 | `visitor-practice-preview.html` | Bài thực hành mẫu | R | Xem một bài thực hành phần mềm mẫu | SV1 | [ ] |
| 3 | `visitor-topic-feedback.html` | Góp ý chủ đề | C/R | Góp ý chủ đề cần bổ sung học liệu | SV1 | [ ] |

### Sinh viên (5 màn hình)
| # | Tệp | Giao diện | CRUD / Trạng thái | Chức năng chính & Truyền đạt trực quan | Phụ trách | Trạng thái |
| :-: | :--- | :--- | :--- | :--- | :-: | :-: |
| 4 | `student-dashboard.html` | Bảng điều khiển | R | Theo dõi tiến độ, điểm theo chương + **Sơ đồ tư duy chương trình học (Cách 4)** | SV1 / SV3 | [ ] |
| 5 | `student-lesson-view.html` | Xem bài giảng | R, Đang tải/Rỗng | Học lý thuyết theo chương + **Hoạt ảnh hướng dẫn menu/phím tắt (Cách 2)** | SV1 | [ ] |
| 6 | `student-practice-do.html` | Thực hành phần mềm | C/R/U, Thành công/Lỗi | Làm bài thực hành từng bước + **Mô phỏng thao tác phần mềm (Cách 1)** | SV1 | [ ] |
| 7 | `student-quiz.html` | Trắc nghiệm | C/R, Hoàn thành | Làm trắc nghiệm theo chủ đề + **Giải thích đáp án sai (Cách 3)** | SV2 | [ ] |
| 8 | `student-submission-result.html` | Kết quả nộp bài | R, Đang chờ/Bị từ chối | Nộp bài thực hành, xem kết quả và nhận xét | SV2 | [ ] |

### Giảng viên (5 màn hình)
| # | Tệp | Giao diện | CRUD / Trạng thái | Chức năng chính | Phụ trách | Trạng thái |
| :-: | :--- | :--- | :--- | :--- | :-: | :-: |
| 9 | `teacher-dashboard.html` | Bảng điều khiển | R | Tổng quan lớp, chương, bài thực hành | SV3 | [ ] |
| 10 | `teacher-practice-manage.html` | Quản lý thực hành | C/R/U/D (Lưu trữ) | Xây dựng bài thực hành phần mềm và bước thao tác | SV3 | [ ] |
| 11 | `teacher-lesson-manage.html` | Soạn bài giảng | C/R/U, Đang chờ | Soạn bài giảng, hướng dẫn thao tác | SV3 | [ ] |
| 12 | `teacher-grading.html` | Chấm bài | C/R/U, Bị từ chối | Chấm bài thực hành, phản hồi sinh viên | SV3 | [ ] |
| 13 | `teacher-analysis.html` | Phân tích năng lực | R | Xem báo cáo năng lực lớp theo chủ đề | SV3 | [ ] |

### Quản trị viên (3 màn hình)
| # | Tệp | Giao diện | CRUD / Trạng thái | Chức năng chính | Phụ trách | Trạng thái |
| :-: | :--- | :--- | :--- | :--- | :-: | :-: |
| 14 | `admin-dashboard.html` | Bảng điều khiển | R | Quản trị hệ thống TinHocPortal | SV2 | [ ] |
| 15 | `admin-user-management.html` | Quản lý người dùng | C/R/U/D (Vô hiệu hóa) | Thêm/sửa/vô hiệu hóa tài khoản, phân quyền | SV2 | [ ] |
| 16 | `admin-curriculum-config.html` | Cấu hình khóa học | C/R/U, Đã hủy/Lưu trữ | Cấu hình chương trình, danh mục phần mềm | SV2 | [ ] |

---

## 2. Màn hình dùng chung (9 màn hình)
| # | Tệp | Giao diện | Ghi chú | Phụ trách | Trạng thái |
| :-: | :--- | :--- | :--- | :-: | :-: |
| 17 | `index.html` | Trang chủ / Điều hướng | Cổng vào hệ thống, chọn vai trò / giới thiệu nhanh | SV3 | [ ] |
| 18 | `login.html` | Đăng nhập | Xác thực mock theo vai trò | SV1 | [ ] |
| 19 | `register.html` | Đăng ký | Form validation + lưu `users` | SV1 | [ ] |
| 20 | `forgot-password.html` | Quên mật khẩu | Luồng khôi phục mô phỏng | SV1 | [ ] |
| 21 | `profile.html` | Hồ sơ cá nhân | Xem / cập nhật thông tin tài khoản | SV2 | [ ] |
| 22 | `settings.html` | Cài đặt | Giao diện sáng/tối, tùy chọn hiển thị | SV3 | [ ] |
| 23 | `notifications.html` | Thông báo | Danh sách thông báo, trạng thái đã đọc/chưa đọc | SV2 | [ ] |
| 24 | `403.html` | Không có quyền truy cập | Chặn truy cập sai vai trò | SV3 | [ ] |
| 25 | `404.html` | Không tìm thấy trang | Trang báo lỗi đường dẫn | SV3 | [ ] |

---

## 3. Định nghĩa hoàn thành (Definition of Done) cho MỖI màn hình
- [ ] Bản mô phỏng Figma / Canva
- [ ] HTML ngữ nghĩa (semantic HTML)
- [ ] CSS hoàn chỉnh + Responsive (Desktop / Tablet / Mobile)
- [ ] Tương tác JavaScript có ý nghĩa
- [ ] Kiểm tra hợp lệ biểu mẫu (Form validation)
- [ ] Kết nối dữ liệu Mock API / `db.json` / LocalStorage
- [ ] Bao phủ trạng thái: Đang tải / Rỗng / Thành công / Lỗi / Vô hiệu hóa / Đang chờ / Bị từ chối / Hoàn thành / Lưu trữ (khi phù hợp)
- [ ] Khả năng tiếp cận cơ bản (Accessibility)
- [ ] Pull Request đã được review và merge vào nhánh `dev`
- [ ] Video OBS giảng giải + chứng minh "làm lại được"
- [ ] Cập nhật `README.md` và bảng kiểm kê này
