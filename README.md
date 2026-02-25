# 🤖 Zalo ChatBot

![NodeJS](https://img.shields.io/badge/Node.js-v20-green)
![Status](https://img.shields.io/badge/status-active-success)
![Maintained](https://img.shields.io/badge/maintained-yes-brightgreen)

> 🚀 **Zalo Automation Bot** mạnh mẽ được xây dựng bằng **JavaScript (Node.js)**
> Tự động hóa quản lý nhóm, giải trí và hỗ trợ vận hành Zalo 24/7.

---

## 👨‍💻 Thông tin dự án

* **Tác giả:** BCH
* **Mod & phát triển:** BCH
* **GitHub:** https://github.com/cnghown/ShareBotZoLa
* **Ngôn ngữ:** JavaScript (Node.js)

---

## ✨ Tính năng nổi bật

### 🛡️ Quản lý nhóm Zalo tự động

Bot hoạt động như một **Group Guardian** giúp bảo vệ nhóm:

* 🚫 Chống spam tin nhắn
* 🔗 Tự động chặn link
* ⚠️ Lọc nội dung tiêu cực
* 🖼️ Chặn ảnh nhạy cảm
* ♻️ Chống thu hồi tin nhắn
* 💬 Chỉ cho phép gửi văn bản
* 👢 Kick thành viên vi phạm
* ⛔ Ban thành viên tự động
* ✅ Tự động duyệt thành viên
* 📢 Tag All nhanh chóng

---

### 🎯 Social Bot

Kho lệnh giải trí phong phú (**50+ Commands**):

* 📺 YouTube Downloader
* 🎵 TikTok Video
* 🎶 ZingMP3 / NhacCuaTui
* 🤖 AI Chat & tiện ích
* 🔎 Nhiều lệnh mở rộng khác

---

### 🎮 Mini Games tích hợp

Giải trí trực tiếp trong nhóm:

* 🎲 Tài Xỉu
* 🎯 Chẵn Lẻ
* 🦀 Bầu Cua
* ✊ Kéo Búa Bao
* 🌱 Nông Trại Mini Game

---

## ⚙️ Yêu cầu hệ thống

* Node.js **v20 trở lên**
* Windows / Linux / VPS

Kiểm tra phiên bản:

```bash
node -v
```

---

## 🚀 Cài đặt & sử dụng

### 1️⃣ Clone dự án

```bash
git clone https://github.com/cnghown/ShareBotZoLa.git
cd ShareBotZoLa
```

---

### 2️⃣ Cài đặt thư viện

```bash
npm install
```

---

### 3️⃣ Cấu hình Bot

Mở file:

```
assets/config.json
```

---

#### 📱 Lấy UUID

1. Mở Zalo Web
2. Nhấn **F12 → Console**
3. Chạy:

```js
localStorage.getItem('z_uuid')
```

---

#### 🌐 Lấy User-Agent

* F12 → Network
* Chọn request bất kỳ
* Copy dòng:

```
Mozilla/5.0 (...)
```

---

#### 🍪 Lấy Cookie

* Cài extension **J2Team Cookies**
* Export Cookie dạng JSON
* Dán vào `config.json`

---

### 4️⃣ Chạy Bot

```bash
run.bat
```

hoặc

```bash
npm start
```

---

### 5️⃣ Cấp quyền Admin

Lấy UID trong terminal → thêm vào:

```
assets/data/list_admin.json
```

---

### 6️⃣ Khởi động lại Bot

Restart bot để áp dụng cấu hình.

---

## 📜 Ví dụ lệnh Bot

```
.help
.tagall
.antispam on
.tiktok <link>
.youtube <từ khóa>
.baucua
.taixiu
```

---

## 📂 Cấu trúc thư mục

```
assets/
 ┣ config.json
 ┣ data/
 ┃ ┗ list_admin.json
commands/
modules/
run.bat
index.js
```

---

## ⚠️ Disclaimer

Dự án được chia sẻ nhằm mục đích **học tập và nghiên cứu**.
Tác giả không chịu trách nhiệm cho các hành vi sử dụng sai mục đích hoặc vi phạm điều khoản của nền tảng Zalo.

---

## ❤️ Credits

Cảm ơn bạn đã sử dụng **Zalo ChatBot**.

Hy vọng dự án giúp bạn:

* Quản lý nhóm hiệu quả hơn
* Tự động hóa Zalo dễ dàng
* Mang lại trải nghiệm giải trí thú vị 🎉

---

## 📞 Liên hệ

* Zalo: https://zalo.me/0395134812
* GitHub: https://github.com/cnghown

---

⭐ Nếu thấy dự án hữu ích, hãy **Star repo** để ủng hộ nhé!
