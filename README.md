# 🤖 Mino — Web bán hàng + Bot trả lời khách 24/7

Trang web bán hàng nhỏ gọn gồm **4 file HTML**, bot chat tự động báo giá – nhận đơn COD 24/7.
**Không cần cài đặt gì cả** — không server, không database, không framework. Mở file là chạy.

> 🪪 Mã nguồn mở theo giấy phép **MIT** — thoải mái dùng, sửa, bán cho shop của mình.

---

## ✨ Tính năng

| Trang | Dành cho | Làm gì |
|---|---|---|
| `index.html` | 🛒 Khách hàng | Trang bán hàng: lưới sản phẩm + bot **Mino** chat tư vấn, dò tên món báo giá, nhận đơn COD |
| `admin.html` | 💬 Chủ shop | **Kênh Chat**: hội thoại live từ web, đơn hàng qua form, trả lời khách tay (đẩy ngược về widget), ghi chú nội bộ, cơ hội kinh doanh |
| `caidat.html` | ⚙️ Chủ shop | Cài đặt bằng **form** (không cần sửa code): thông tin shop, món bán, kịch bản hỏi–đáp của bot |
| `huong-dan.html` | 📘 Mọi người | Hướng dẫn 3 bước + nối Facebook Messenger & Zalo OA (đường AhaChat không cần code lẫn đường API chính chủ) |

Bot hoạt động theo 2 lớp: khách nhắn **có tên món** → báo giá đúng món đó; không có tên món → dò **bảng từ khóa** (giá / ship / đặt hàng / đổi trả…); không khớp → nhờ chủ shop gọi lại (kèm gợi ý để lại SĐT).

---

## 📥 Tải về

**Cách 1 — Tải ZIP (không cần biết git, dễ nhất)**
1. Bấm nút xanh **`< > Code`** ở đầu trang repo
2. Chọn **Download ZIP** → giải nén là đủ 4 trang bên trong

**Cách 2 — Dùng git**
```bash
git clone https://github.com/binance9/bot-ban-hang-mino.git
```

## ▶️ Chạy (5 giây)

Mở file **`index.html`** bằng Chrome hoặc Edge — hết.

> 💡 Muốn có **link gửi cho khách**: vào [netlify.com/drop](https://app.netlify.com/drop), kéo cả thư mục vào, nhận link miễn phí ngay lập tức.

## ⚙️ Cài đặt thông tin shop (2 phút, không cần biết code)

1. Mở **`caidat.html`** (hoặc bấm *⚙️ Cài đặt* trên menu)
2. Điền tên shop, SĐT → **＋ Thêm món** nhập món bán (tên + giá)
3. Thêm kịch bản: khách hỏi *"giá"* → bot trả câu gì; khách hỏi *"ship"* → trả câu gì
4. Bấm **💾 Lưu cài đặt** → mở lại `index.html` (F5) — bot nói theo shop mình liền

Sửa hỏng? Bấm **↺ Khôi phục mặc định** — về như cũ trong 1 giây.

## 💬 Chăm khách hằng ngày

Mở **`admin.html`** (bấm *🖥️ Kênh Chat*):
- Hội thoại khách chat với bot hiện tự động theo phiên (cột 2, nhãn *Khách online*)
- Đơn khách đặt qua form hiện sẵn kèm tên + SĐT + địa chỉ — gọi xác nhận là xuất kho
- Khách bot chưa xử lý được → gõ trả lời tay, tin đẩy ngược về widget của khách ngay
- Xem *Hướng dẫn* → mục 4 & 5 để nối bot với Facebook Messenger / Zalo OA

---

## 🧠 Nâng cấp bot

Muốn bot hiểu câu tự do (thay vì dò từ khóa): chỉ cần **thay 1 hàm `botTraLoi()`** trong `index.html` — cắm API AI vào đó, phần còn lại giữ nguyên.

## 📌 Nên biết

- Dữ liệu (hội thoại, đơn, cài đặt) lưu **trong trình duyệt của máy đang mở** (localStorage). Muốn nhiều máy chung dữ liệu → cần thêm server nhỏ (gợi ý trong `huong-dan.html` mục 6)
- Muốn **reset dữ liệu demo**: F12 → Application → Local Storage → xóa các khoá `donhang`, `mino_*`
- Công nghệ: HTML + CSS + JavaScript thuần, **0 dependency**, tổng ~100 KB

## 📄 Giấy phép

[MIT](LICENSE) — dùng, sửa, bán thoải mái. Không cần xin ai.
