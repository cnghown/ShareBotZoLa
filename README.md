# 🤖 Zalo ChatBot

**Zalo ChatBot** được phát triển bằng **JavaScript** 
Tác giả: **BCH**
Mod lại bởi **BCH** – [GitHub](https://github.com/BCHoan)

```
                  .----.
      .---------. | == |
      |.-"""""-.| |----|
      ||       || | == |
      ||       || |----|
      |'-.....-'| |::::|
      `"")---(""` |___.|
     /:::::::::::\" _  "
    /:::=======:::\`\`\
    `"""""""""""""`  '-'
```

---

## 📌 Tính năng (v1.5.5)

### 🛠 Quản lý nhóm Zalo tự động
- Tự động bảo vệ nhóm
  - **Chống Spam**
  - **Chặn Liên kết**
  - **Chặn Nội Dung Tiêu Cực**
  - **Chống Gửi Ảnh Nhạy Cảm**
  - **Chống Thu Hồi Tin Nhắn**
  - **Chỉ Được Phép Gửi Tin Nhắn Văn Bản**
  - **Kick Thành Viên**
  - **Chặn Thành Viên**
  - **Tự Động Duyệt Thành Viên**
  - **Tin Nhắn Tag All**

### 🎯 Social Bot
- Hơn **50 lệnh** giải trí:
  - 📺 YouTube
  - 🎵 TikTok
  - 🎶 ZingMP3, NhacCuaTui
  - ...và nhiều hơn nữa.

### 🎮 Tiện ích game

- **Tài xỉu**
- **Chẵn lẻ**
- **Bầu cua**
- **Kéo búa bao**
- **Nông trại**
---

## 🚀 Hướng dẫn sử dụng

**Yêu Cầu Bắt Buộc: Có Bản Nodejs V20**

### 1️⃣ Cấu hình
Mở tệp `config.json` trong thư mục `assets` và thiết lập:

- **Cookie**, **Imei**
 - Sử dụng tiện ích get-imei-cookie [tại đây](https://www.mediafire.com/file/u65t0y95nw0oujy/get-imei-cookie-js.zip/file)

 - Giải nén file ra sau đó đưa lên tiện ích chrome để sử dụng

- **UserAgent**  
  - Giữ mặc định hoặc lấy UserAgent mới tại [whatmyuseragent.com](https://whatmyuseragent.com/)

---

### 2️⃣ Chạy Bot
Chạy file:
```bash
run.bat
```

---

### 3️⃣ Thiết lập quyền Admin
- Lấy **UID** tài khoản cần cấp quyền qua terminal.
- Thêm vào file:
```
assets/data/list_admin.json
```

---

### 4️⃣ Khởi động lại bot
Sau khi cấu hình, hãy **khởi động lại** bot để áp dụng thay đổi.

---
---


## Hướng dẫn khởi chạy trên termux(Android)
**Lưu ý**: Khi chạy trên termux cần thay lại code file **bot.js**, lấy file code đã sửa [tại đây](https://www.mediafire.com/file/aadre72xnkd1r76/bot.js/file)

**Video cách cài chi tiết [Tại Đây](https://youtu.be/PcLnqET1Ivs?si=7yT8UGuu5VkXUrLc)**

**B1: tải root debian**
```
pkg update && pkg upgrade -y
pkg install proot-distro -y
proot-distro install debian
proot-distro login debian
```

**Sau khi hiện root@localhost** thì vào B2

**B2: tải node phù hợp**
```
apt-get update

apt-get install -y curl python3 make g++ gcc

curl -L https://raw.githubusercontent.com/tj/n/master/bin/n -o n

bash n 20.10.0

export PATH="/usr/local/bin:$PATH"

if [ -f /root/.bashrc ]; then
    grep -qxF 'export PATH="/usr/local/bin:$PATH"' /root/.bashrc || echo 'export PATH="/usr/local/bin:$PATH"' >> /root/.bashrc

fi
```
echo "Phiên bản NodeJS:"
```
node -v
```
echo "Phiên bản npm:"
```
npm -v
```

**B3: git clone file bot**
```
apt install git ffmpeg  -y
link mình sẽ up sau
```

**B4: build canvas**
```
apt update && apt install -y \
  build-essential \
  libcairo2-dev \
  libpango1.0-dev \
  libjpeg-dev \
  libgif-dev \
  librsvg2-dev \
  pkg-config
npm install canvas
npm install dotenv
```

**B5 tải mariaDB**
```
apt update && apt upgrade -y
apt install mariadb-server mariadb-client -y
```

**Khởi động sql**
```
service mariadb start
```

**Đặt mật khẩu cho sql**
```
mysql -u root -p
```
**Bạn sẽ thấy enter password, nhập**
*bước này chưa cần làm gì,ấn enter*

**Sau đó sẽ thấy dòng có chữ none**
*copy lệnh này*
```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'nhap_matkhau_moi';
FLUSH PRIVILEGES;
```
**Xong gõ**
```
EXIT
```
*để thoát*

**B6: thêm sql vào bashrc**
```
nano ~/.bashrc

```
**thêm Auto start MariaDB khi vào Debian**
*kéo xuống dòng cuối thêm*
```
if ! pgrep -x mysqld > /dev/null; then
    service mariadb start
fi
```
**dán vào cuối file và thoát rồi chạy**
```
source ~/.bashrc
```

**B7: chỉnh sửa database và tạo .env**
*Truy cập vô* 
```
nano /root/BCH_share_V1.5.5/assets/json-data/database-config.json
```

**Sẽ thấy**
```
{
  "nameServer": "BCH x Hoan DZ",
  "host": "localhost",
  "user": "root",
  "password": "",
  "database": "bot-zalo",
  "port": 3300,
  "tablePlayerZalo": "players_zalo",
  "tableAccount": "account",
  "dailyReward": 100000000000
}
```
**Nhập mật khẩu ở dòng "password": "", nhập mật khẩu nãy tạo ở trên, xong rồi thì thoát ra**

**Truy cập vô**
```
nano .env
```

**Dán**
```
DB_HOST=127.0.0.1
DB_PORT=3300
DB_USER=root
DB_PASSWORD=
DB_NAME=nqd_db
```
**"password": ""** dòng này mk phải để đúng với **DB_PASSWORD**, *nếu không sẽ không sử dụng được các tác vụ game*

**B8: build lại node_modules**
```
rm -rf node_modules package-lock.json && npm i
```

**B9: Chỉnh sửa file**

*chạy lệnh*
```
nano /root/BCH_share_V1.5.5/node_modules/nsfwjs/dist/esm/index.js
```
*kéo xuống tìm dòng chứa buffer/ và sửa thành buffer/index.js, xong hãy thoát ra*

**Phần còn lại**
```
node bot.js
```
## ❤️ Lời cảm ơn

**BuiCongHoan** chúc bạn sử dụng bot vui vẻ

Cảm ơn bạn đã sử dụng mã nguồn của tôi.  
Hy vọng bạn sẽ thích những tính năng mà **Zalo ChatBot** mang lại!

**Tham gia group của tôi** [tại đây](https://zalo.me/0395134812)

**Liên hệ với BuiCongHoan** [tại đây]([https://zaloapp.com/qr/p/gocjf95sb529?src=qr](https://zalo.me/0395134812))
