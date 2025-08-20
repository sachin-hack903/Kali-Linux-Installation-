# Kali-Linux-Installation-
# 🐧 Kali Linux Installation on Android via [Termux](https://f-droid.org/en/packages/com.termux) (2025)

---

## 📋 **Requirements**

✅ **15GB Storage**  
✅ [**Termux app**](https://f-droid.org/repo/com.termux_1002.apk)  
✅ [**Nethunter VNC**](https://github.com/xiv3r/Kali-Linux-Termux/releases/download/Apps/offsec.nethunter.kex.apk) 

---

## ⚡ **Auto Full Install**

```
pkg update && pkg install wget -y && clear && wget -O install-nethunter-termux https://offs.ec/2MceZWr && chmod +x install-nethunter-termux && bash install-nethunter-termux && kali
````

---

## 🛠️ **Manual Installation (Step by Step)**

### 1️⃣ Setup storage access

```
termux-setup-storage
```

### 2️⃣ Update & upgrade packages

```
apt update && apt upgrade -y
```

### 3️⃣ Install wget

```
pkg install wget -y
```

### 4️⃣ Download Nethunter Installer

```
wget -O install-nethunter-termux https://offs.ec/2MceZWr
```

### 5️⃣ Make it executable

```
chmod +x install-nethunter-termux
```

### 6️⃣ Run the installer

```
./install-nethunter-termux
```

---

## 🛠️ **Fix GUI Issues**

🔴 Quit existing panel:

```
xfce4-panel --quit
```

🟡 Delete corrupted configs:

```
rm -rf ~/.config/xfce4/panel
```

🟢 Remove broken XML file:

```
rm -rf ~/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-panel.xml
```

🔵 Restart panel:

```
xfce4-panel &
```

---

## 🖥️ **VNC Setup**

### 🔑 Set VNC password

```
kali vnc passwd
```

### ▶️ Run VNC server

```
kali vnc &
```

* Address: `127.0.0.1:5901`
* Username: **kali**
* Password: *(your set password)*

<img src="https://github.com/xiv3r/Kali-Linux-Termux/blob/main/kali_nethunter/vncsetup.png">

---

## 🔑 **Usage Commands**

👤 Login as User:

```
kali
```

👑 Login as Root:

```
kali -r
```

🚪 Logout:

```
exit
```

❌ Kill VNC service:

```
kali kill vnc
```

🗑️ Uninstall:

```
kali-uninstall
```

---

## 📟 **Terminal Password**

* Default password: **kali**

<p align="center">
  <a href="https://store.nethunter.com/repo/com.offsec.nethunter.kex_11525001.apk">
    <img src="https://github.com/xiv3r/Kali-Linux-Termux/blob/main/kali_nethunter/nhterm.png" alt="NetHunter KeX Icon">
  </a>
</p>
---

## ❌ **Disable VNC Phantom Process Killer**

If you get error:
`Process completed (signal 9) - press Enter`

👉 Fix it:

1. Download:

   * [**Shizuku**](https://github.com/RikkaApps/Shizuku/releases)
   * [**Ashell**](https://github.com/DP-Hridayan/aShellYou/releases)

2. Enable **Developer Options → Wireless Debugging** & connect with Shizuku.

3. Permit **Ashell** in Shizuku settings.

4. Run these commands inside Ashell:

```
adb shell /system/bin/device_config set_sync_disabled_for_tests persistent
adb shell /system/bin/device_config put activity_manager max_phantom_processes 2147483647
adb shell settings put global settings_enable_monitor_phantom_procs false
```

5. Verify:

```
adb shell /system/bin/dumpsys activity settings | grep max_phantom_processes
adb shell /system/bin/device_config get activity_manager max_phantom_processes
```

---

## 📱 **Follow & Support 🔔**

🔥 Credited by **@Cyber_Sachin_903**

<p align="center">
<a href="https://youtube.com/@zerodarknexus">
  <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
</a>
<a href="https://t.me/ZeroHackNexus">
  <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
</a>
<a href="https://chat.whatsapp.com/II35pNaN25rHqnUmqXK6ag">
  <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
</a>
</p>

---

## 🧑‍💻 **License**

📖 Based on [Kali Linux Official Docs](https://www.kali.org/docs/nethunter/nethunter-rootless/)
✅ Released under **MIT License** – Free to use, share & improve with credits.
