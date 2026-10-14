# 🤖 Mino — Web bán hàng + Bot trả lời khách 24/7

Bộ web bán hàng nhỏ gọn gồm **4 file HTML** — mở lên là chạy, **không cần cài đặt gì cả**.

- 🛒 Khách vào web → chat với **bot Mino** → bot tự báo giá theo tên món, nhận đơn COD
- 💬 Chủ shop mở **Kênh Chat** → xem hội thoại, đơn hàng, trả lời khách, quản lý cơ hội
- ⚙️ Đổi thông tin shop bằng **trang Cài đặt dạng form** — không cần sửa code
- 🔗 Kèm hướng dẫn nối **Facebook Messenger** & **Zalo OA** (cả đường không cần code lẫn đường API)

---

## 📥 Tải về (chọn 1 trong 2 cách)

### Cách 1 — Tải ZIP (ai không biết git, dễ nhất)
1. Bấm nút xanh **`< > Code`** ở đầu trang này
2. Chọn **Download ZIP**
3. Giải nén file vừa tải — xong, đủ cả 4 trang bên trong

### Cách 2 — Dùng git
```bash
git clone https://github.com/binance9/bot-ban-hang-mino.git
```

## ▶️ Chạy (5 giây)

Mở file **`index.html`** bằng trình duyệt (Chrome hoặc Edge). Hết — không cần cài Python, Node, hay gì cả.

> 💡 Muốn có đường link gửi cho khách: vào **netlify.com/drop**, kéo cả thư mục vào, nhận link miễn phí ngay lập tức.

## ⚙️ Cài đặt thông tin shop (2 phút, không cần biết code)

1. Mở file **`caidat.html`** (hoặc bấm "⚙️ Cài đặt" trên menu)
2. Điền tên shop, số điện thoại → bấm **＋ Thêm món** nhập món bán (tên + giá)
3. Thêm kịch bản: khách hỏi *"giá"* → bot trả câu gì; khách hỏi *"ship"* → trả câu gì
4. Bấm **💾 Lưu cài đặt** → mở lại `index.html` (F5) — bot nói theo shop mình liền

Sửa hỏng? Bấm **↺ Khôi phục mặc định** — về như cũ trong 1 giây.

## 📋 Các file trong bộ

| File | Dành cho | Làm gì |
|---|---|---|
| `index.html` | 🛒 Khách hàng | Trang bán hàng + bot Mino chat tư vấn, nhận đơn |
| `admin.html` | 💬 Chủ shop | Kênh Chat: hội thoại, đơn hàng, cơ hội kinh doanh |
| `caidat.html` | ⚙️ Chủ shop | Cài đặt bằng form: thông tin, món bán, kịch bản bot |
| `huong-dan.html` | 📘 Mọi người | Hướng dẫn 3 bước + nối Facebook/Zalo chi tiết |

## 🔗 Kết nối Facebook Messenger / Zalo

Mở **`huong-dan.html`** — mục 4 và 5, có 2 đường:

- **Không cần code (khuyên dùng):** AhaChat — miễn phí, kéo thả, 10 phút chạy cả Messenger lẫn Zalo
- **API chính chủ:** code webhook Meta + Zalo Open API chép được ngay, từng bước có ảnh cảnh báo lỗi hay gặp

## ❓ Vài điều nên biết

- Dữ liệu demo (hội thoại, đơn, cài đặt) lưu **trên trình duyệt của máy mình** — muốn nhiều máy chung dữ liệu thì cần thêm server nhỏ (hướng dẫn trong `huong-dan.html` mục 6)
- Xóa dữ liệu demo: nhấn `F12` → Application → Local Storage → xóa các khoá `donhang`, `mino_*`
- Bot trả lời theo **từ khóa + dò tên sản phẩm**; muốn thông minh hơn (hiểu câu tự do) chỉ cần cắm API AI vào hàm `botTraLoi()` trong `index.html` — thay đúng 1 hàm

## 📄 Giấy phép

MIT — thoải mái lấy về dùng, sửa, bán. Không cần xin ai.
