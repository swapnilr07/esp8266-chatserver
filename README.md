# 📡 ESP8266 Offline Chat Server

This project flashes a ready-made firmware (`chatserver.bin`) to your NodeMCU ESP8266, turning it into a **local Wi-Fi chat server**. Any nearby device can connect to its Wi-Fi and join a real-time chatroom via their browser — **no internet needed**.

---

## 🔧 Features

- 🌐 100% offline chat via local Wi-Fi (ESP8266 hotspot)
- ✅ Auto-login for returning users
- 🔒 Usernames shown only for others, not for yourself
- 🛡️ Admin panel with full control
- ❌ Clear all chat logs (Admin only)
- Change Wi-Fi name & password (even open network)
- Change admin password
- View connected users
- Restart device
- Logout from admin panel

---

## 📁 Files

- `chatserver.bin` – Precompiled firmware ready to flash on ESP8266

---

## 🔐 Default Settings

| Feature            | Value                  |
|--------------------|-------------------------|
| Wi-Fi Name (SSID)  | ChatServer              |
| Wi-Fi Password     | 00000000                |
| Admin Password     | admin123                |
| Chatroom URL       | http://192.168.4.1      |
| Admin Panel URL    | http://192.168.4.1/admin|

---
## 🔽 Download Firmware

Click below to download the precompiled firmware for ESP8266:

[⬇️ ChatServer.bin](https://github.com/swapnilr07/esp8266-chatserver/blob/main/ChatServer.bin?raw=true)

## 🚀 Flashing Instructions

### 🔹 Web Flasher (Recommended)

1. Go to: [https://esp.huhn.me/](https://esp.huhn.me/)
2. Connect ESP8266 via USB
3. Select your port and upload `chatserver.bin`
4. Click **Flash**
5. You're done!

### 🔹 Using esptool.py (Advanced)

```bash
esptool.py --port COM3 write_flash 0x00000 chatserver.bin
