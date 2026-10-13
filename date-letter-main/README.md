# 💌 Date Invitation Web App

Một trang web thư mời hẹn hò tương tác được thiết kế đẹp mắt, lãng mạn và tinh tế dành riêng cho **Mỹ Anh** từ **Phương**.

Trang web mô phỏng trải nghiệm mở phong bì thư, xé cuống vé nghe tin nhắn âm thanh, câu hỏi tương tác "né nút Không", cho phép chọn ngày giờ và gửi thông báo trực tiếp qua Email.

---

## ✨ Tính năng nổi bật

- ✉️ **Mở phong bì tương tác**: Hiệu ứng chuyển động mở nắp thư, hiện vé hẹn hò (*Admit Two*).
- 🎟️ **Xé cuống vé & Nghe lời nhắn**: Kéo/xé cuống vé để phát lời nhắn thoại cùng nhạc nền nhẹ nhàng.
- 💬 **Câu hỏi tương tác**: Nút *"Không"* tự động di chuyển né chuột/chạm cùng các câu thoại hài hước, dễ thương.
- 📅 **Chọn lịch hẹn thông minh**:
  - Tự động gợi ý 14 ngày tới.
  - Chọn các khung giờ linh hoạt (Sáng, Trưa, Chiều, Tối hoặc giờ khác) kèm ghi chú dặn dò.
- 📧 **Gửi mail tự động**: Tích hợp FormSubmit API để gửi thông tin chốt lịch trực tiếp về email cá nhân ngay khi hoàn tất.
- 🗓️ **Google Calendar**: Tạo sẵn đường link thêm sự kiện vào Google Calendar.
- 📱 **Responsive**: Tối ưu hoàn hảo cho cả thiết bị di động (Mobile) lẫn máy tính (Desktop).

---

## 📂 Cấu trúc thư mục

```text
├── index.html          # Mã nguồn giao diện & logic chính của trang web
├── vercel.json         # Cấu hình headers bảo vệ (noindex cho SEO)
├── .gitignore          # Cấu hình bỏ qua thư mục build (.vercel)
├── .vercelignore       # Cấu hình file không cần upload khi deploy
├── audio/
│   ├── bgm.m4a         # Nhạc nền
│   └── i-love-you_1.mp3# File âm thanh lời nhắn
└── images/
    └── ...jpg          # Ảnh kỷ niệm hiển thị ở màn hình hoàn tất
```

---

## 🚀 Hướng dẫn chạy và Deploy

### 1. Chạy thử trên máy cục bộ (Local)
Dự án được viết hoàn toàn bằng HTML/CSS/JS thuần, không cần cài đặt thư viện hay build tool phức tạp.

- Bạn chỉ cần mở file `index.html` bằng trình duyệt hoặc sử dụng extension **Live Server** trong VS Code.
- Hoặc dùng Python mở nhanh một local server:
  ```bash
  python -m http.server 8000
  ```
  Sau đó truy cập: `http://localhost:8000`

### 2. Deploy lên Vercel (Miễn phí & Cực nhanh)
1. Cài đặt Vercel CLI (nếu chưa có):
   ```bash
   npm i -g vercel
   ```
2. Đứng tại thư mục dự án và chạy:
   ```bash
   vercel
   ```
3. Làm theo hướng dẫn trên màn hình terminal để nhận link web chính thức (`https://<ten-du-an>.vercel.app`).

Hoặc bạn có thể push code lên **GitHub** và import repo vào dashboard của [Vercel](https://vercel.com) chỉ với 1 click.

---

## ⚙️ Tùy biến (Customization)

Tất cả các thông số cấu hình nằm trong thẻ `<script>` ở cuối file `index.html`:

```javascript
const C = {
  music: true,
  bgmSrc: 'audio/bgm.m4a',
  musicVolume: 0.45,
  audioSrc: 'audio/i-love-you_1.mp3',
  photoSrc: 'images/...jpg',
  email: 'phamdinhanhphuong@gmail.com', // Email nhận thông báo kết quả
};
```

---

*Made with ❤️ by Phuong*
