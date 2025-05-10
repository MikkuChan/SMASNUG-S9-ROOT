# Samsung S9 (SDM845) Rooting Guide | Panduan Root Samsung S9 (SDM845)

<div align="center">
  <img src="https://img.shields.io/badge/Device-Samsung%20S9%20(SDM845)-blue">
  <img src="https://img.shields.io/badge/Type-Root%20Guide-orange">
  <img src="https://img.shields.io/badge/Status-Working-green">
</div>

<details open>
<summary><b>🇬🇧 English Version</b></summary>

## ⚠️ Disclaimer
- **This guide is provided for educational purposes only**
- **All risks associated with these modifications are assumed by the user**
- **Make a full backup of your data before proceeding**
- **Ensure your battery is at least 50% charged**

## 📋 Overview
This guide provides instructions for rooting your Samsung S9 (SDM845) device, including installing TWRP recovery, flashing a custom kernel with KernelSU support, and setting up additional modules.

## 🛠️ What You'll Get
- TWRP Custom Recovery
- Custom Kernel with KernelSU
- System Modules Support
- Advanced Features (ADB Debugging, Battery Management)

## 📱 Pre-requisites
- Samsung S9 with Snapdragon 845 chipset
- USB cable
- Windows PC
- Basic understanding of Android commands
- Backup of all important data

## 📥 Required Downloads

### TWRP Installation
- [Odin Tool](https://odindownload.com/mobile/)
- [TWRP Recovery](https://t.me/samsung845/25/55756)
- [Permanent TWRP](https://t.me/samsung845/12/82714)

### Custom Kernel & Root
- [Custom Kernel](https://github.com/Andrey0800770/samsung_sdm845-kernel/releases/download/V4.9.337-006-susfs4ksu/starqlte-v4.9.337-Rel6.zip)
- [KernelSU Manager](https://github.com/backslashxx/KernelSU/releases)
- [BusyBox](https://t.me/taamarin/283465/387838)

### Additional Modules
- [Box For Root (BFR) & Manager](https://github.com/taamarin/box_for_magisk)
- [WebUI for BFM](https://github.com/geeks121/webui_bfm)
- [Battery Charge Limiter](https://github.com/MuntashirAkon/BatteryChargeLimiter)

## 📲 Step-by-Step Instructions

### 1. Installing TWRP Recovery

1. Download and extract Odin tool on your PC
2. Download the TWRP recovery file
3. Boot your device into Download Mode:
   - Power off your device completely
   - Press and hold **Volume Down + Bixby + Power** buttons simultaneously
   - Press Volume Up to confirm when prompted
4. Open Odin on your PC
5. Connect your device to PC via USB cable
6. In Odin:
   - Ensure your device is detected (blue box in Odin)
   - Click on the **AP** button and select the TWRP file
   - Make sure only "F. Reset Time" and "Auto Reboot" options are checked
   - Click **Start** to begin flashing
7. When flashing completes, immediately boot to Recovery Mode:
   - Press and hold **Volume Up + Bixby + Power** buttons

> 🎬 **Visual Guide**: [TWRP Installation Tutorial](https://youtu.be/uFZhLi0LOWk)

### 2. Installing Custom Kernel

1. While in TWRP, first install the permanent TWRP file:
   - Tap **Install**
   - Navigate to and select the permanent TWRP file
   - Swipe to confirm flash
2. Next, install the custom kernel:
   - Go back to Install screen
   - Navigate to and select the custom kernel zip file
   - Swipe to confirm flash
3. When complete, select **Reboot System**

### 3. Setting Up Root & Modules

1. Install KernelSU Manager:
   - Download the KernelSU APK from the link provided
   - Install the APK on your device
   - Open the app to confirm root access
2. Install BusyBox:
   - Download the BusyBox installer
   - Install and run the app
   - Grant root permissions when prompted
   - Install BusyBox binaries
3. Install BFR & Manager:
   - Download and install from the provided link
   - Follow on-screen setup instructions
4. Install WebUI (optional):
   - Download and install the WebUI add-on
   - Configure according to your preferences

### 4. Advanced Configurations

#### Enable Auto ADB Debugging
Edit `/system/build.prop` and add the following lines:
```
service.adb.tcp.port=5555
ro.adb.secure=0
ro.debuggable=1
persist.service.adb.enable=1
persist.service.debuggable=1
persist.sys.usb.config=mtp,adb
```

#### Enable Auto Power On When Charging
Edit `/init.rc` (around line 1871):
- Find: `#class_start sec-charger`
- Replace with: `setprop sys.powerctl reboot`

#### Battery Charge Control
Install the Battery Charge Limiter app from the provided link to manage battery charging thresholds.

## 📝 Notes
- Some features may vary depending on your firmware version
- Performance improvements will depend on kernel optimization
- Always keep a backup recovery method available

## ❓ Troubleshooting
- If device boots to system instead of TWRP after flashing, try booting to recovery manually
- If KernelSU shows "unsupported" status, verify you've installed the correct kernel version
- For module-related issues, check the respective GitHub repositories for updated information

## 🔗 Credits & Resources
- Original kernel developer: [Andrey0800770](https://github.com/Andrey0800770)
- KernelSU project: [KernelSU](https://github.com/backslashxx/KernelSU)
- BFR developer: [taamarin](https://github.com/taamarin)
- Samsung SDM845 community: [Telegram](https://t.me/samsung845)
</details>

<details>
<summary><b>🇮🇩 Versi Bahasa Indonesia</b></summary>

## ⚠️ Peringatan
- **Panduan ini disediakan untuk tujuan edukasi saja**
- **Semua risiko yang terkait dengan modifikasi ini ditanggung oleh pengguna**
- **Buat cadangan penuh data Anda sebelum melanjutkan**
- **Pastikan baterai minimal terisi 50%**

## 📋 Gambaran Umum
Panduan ini memberikan petunjuk untuk melakukan root pada perangkat Samsung S9 (SDM845), termasuk instalasi TWRP recovery, flashing kernel kustom dengan dukungan KernelSU, dan pengaturan modul tambahan.

## 🛠️ Yang Akan Anda Dapatkan
- TWRP Custom Recovery
- Custom Kernel dengan KernelSU
- Dukungan Modul Sistem
- Fitur Lanjutan (ADB Debugging, Manajemen Baterai)

## 📱 Prasyarat
- Samsung S9 dengan chipset Snapdragon 845
- Kabel USB
- PC Windows
- Pemahaman dasar perintah Android
- Cadangan semua data penting

## 📥 Unduhan yang Diperlukan

### Instalasi TWRP
- [Odin Tool](https://odindownload.com/mobile/)
- [TWRP Recovery](https://t.me/samsung845/25/55756)
- [TWRP Permanen](https://t.me/samsung845/12/82714)

### Kernel Kustom & Root
- [Custom Kernel](https://github.com/Andrey0800770/samsung_sdm845-kernel/releases/download/V4.9.337-006-susfs4ksu/starqlte-v4.9.337-Rel6.zip)
- [KernelSU Manager](https://github.com/backslashxx/KernelSU/releases)
- [BusyBox](https://t.me/taamarin/283465/387838)

### Modul Tambahan
- [Box For Root (BFR) & Manager](https://github.com/taamarin/box_for_magisk)
- [WebUI untuk BFM](https://github.com/geeks121/webui_bfm)
- [Pengatur Batas Pengisian Baterai](https://github.com/MuntashirAkon/BatteryChargeLimiter)

## 📲 Petunjuk Langkah demi Langkah

### 1. Memasang TWRP Recovery

1. Unduh dan ekstrak tool Odin di PC Anda
2. Unduh file TWRP recovery
3. Boot perangkat ke Mode Download:
   - Matikan perangkat sepenuhnya
   - Tekan dan tahan tombol **Volume Bawah + Bixby + Power** secara bersamaan
   - Tekan Volume Atas untuk konfirmasi ketika diminta
4. Buka Odin di PC Anda
5. Hubungkan perangkat ke PC melalui kabel USB
6. Di Odin:
   - Pastikan perangkat terdeteksi (kotak biru di Odin)
   - Klik tombol **AP** dan pilih file TWRP
   - Pastikan hanya opsi "F. Reset Time" dan "Auto Reboot" yang dicentang
   - Klik **Start** untuk memulai flashing
7. Ketika flashing selesai, segera boot ke Mode Recovery:
   - Tekan dan tahan tombol **Volume Atas + Bixby + Power**

> 🎬 **Panduan Visual**: [Tutorial Instalasi TWRP](https://youtu.be/uFZhLi0LOWk)

### 2. Memasang Kernel Kustom

1. Saat di TWRP, pertama instal file TWRP permanen:
   - Ketuk **Install**
   - Navigasi ke dan pilih file TWRP permanen
   - Geser untuk mengkonfirmasi flash
2. Selanjutnya, instal kernel kustom:
   - Kembali ke layar Install
   - Navigasi ke dan pilih file zip kernel kustom
   - Geser untuk mengkonfirmasi flash
3. Ketika selesai, pilih **Reboot System**

### 3. Mengatur Root & Modul

1. Instal KernelSU Manager:
   - Unduh APK KernelSU dari link yang disediakan
   - Instal APK di perangkat Anda
   - Buka aplikasi untuk mengkonfirmasi akses root
2. Instal BusyBox:
   - Unduh installer BusyBox
   - Instal dan jalankan aplikasi
   - Berikan izin root ketika diminta
   - Instal binary BusyBox
3. Instal BFR & Manager:
   - Unduh dan instal dari link yang disediakan
   - Ikuti petunjuk pengaturan di layar
4. Instal WebUI (opsional):
   - Unduh dan instal add-on WebUI
   - Konfigurasi sesuai preferensi Anda

### 4. Konfigurasi Lanjutan

#### Aktifkan Auto ADB Debugging
Edit `/system/build.prop` dan tambahkan baris berikut:
```
service.adb.tcp.port=5555
ro.adb.secure=0
ro.debuggable=1
persist.service.adb.enable=1
persist.service.debuggable=1
persist.sys.usb.config=mtp,adb
```

#### Aktifkan Auto Power On Saat Charging
Edit `/init.rc` (sekitar baris 1871):
- Temukan: `#class_start sec-charger`
- Ganti dengan: `setprop sys.powerctl reboot`

#### Kontrol Pengisian Baterai
Instal aplikasi Battery Charge Limiter dari link yang disediakan untuk mengatur batas pengisian baterai.

## 📝 Catatan
- Beberapa fitur mungkin bervariasi tergantung versi firmware Anda
- Peningkatan performa akan bergantung pada optimasi kernel
- Selalu simpan metode recovery cadangan

## ❓ Pemecahan Masalah
- Jika perangkat boot ke sistem alih-alih TWRP setelah flashing, coba boot ke recovery secara manual
- Jika KernelSU menunjukkan status "tidak didukung", verifikasi Anda telah menginstal versi kernel yang benar
- Untuk masalah terkait modul, periksa repositori GitHub masing-masing untuk informasi terbaru

## 🔗 Kredit & Sumber Daya
- Pengembang kernel asli: [Andrey0800770](https://github.com/Andrey0800770)
- Proyek KernelSU: [KernelSU](https://github.com/backslashxx/KernelSU)
- Pengembang BFR: [taamarin](https://github.com/taamarin)
- Komunitas Samsung SDM845: [Telegram](https://t.me/samsung845)
</details>

---

<div align="center">
  <i>Last updated: May 10, 2025 | Terakhir diperbarui: 10 Mei 2025</i>
</div>
