# Ghi chú HTML & CSS — Bài 05

## 1. CSS bố cục 2 cột (`.bo-cuc-2-cot`)

```css
.bo-cuc-2-cot {
    display: grid;
    grid-template-columns: 220px 1fr;
    gap: 24px;
    align-items: start;
}
```

| Thuộc tính | Giá trị | Công dụng |
| :--- | :--- | :--- |
| `display` | `grid` | Bật chế độ **CSS Grid** (bố cục dạng lưới gồm hàng và cột) cho thẻ `.bo-cuc-2-cot`. Nhờ đó các thẻ con trực tiếp bên trong (`.cot-trai` và `.cot-phai`) sẽ tự động xếp thành các ô lưới thay vì xếp chồng dọc như mặc định. |
| `grid-template-columns` | `220px 1fr` | Quy định **số cột và độ rộng từng cột**:<br>- Cột 1 rộng cố định **`220px`** (để chứa ảnh hoa hồng).<br>- Cột 2 rộng **`1fr`** (*1 fraction* = 1 phần không gian còn lại), tức là tự động chiếm hết phần chiều rộng còn dư của khung chứa. |
| `gap` | `24px` | Tạo **khoảng cách (khe hở) 24px** giữa các cột (và giữa các hàng nếu có nhiều hàng), giúp cột ảnh và cột chữ không bị dính sát vào nhau mà không cần dùng `margin` thủ công. |
| `align-items` | `start` | Căn chỉnh các phần tử con **theo chiều dọc** bên trong hàng lưới về **mép trên cùng** (`start`). Mặc định Grid dùng `stretch` (kéo giãn cao bằng nhau), đặt `start` giúp cột ảnh chỉ cao đúng bằng kích thước thật của ảnh và thẳng hàng từ trên xuống với tiêu đề `1. Giới thiệu`. |

### Ghi nhớ nhanh
- Muốn chia bố cục dạng lưới: luôn bắt đầu bằng `display: grid;`.
- `1fr` hiểu đơn giản là **"phần còn lại"** (nếu viết `1fr 1fr` thì chia đều 2 cột 50% - 50%; viết `1fr 2fr` thì cột 2 rộng gấp đôi cột 1).
- `gap` gọn hơn `margin` vì chỉ tạo khoảng trống **ở giữa** các cột, không tạo khoảng trống thừa ở 2 mép ngoài.
