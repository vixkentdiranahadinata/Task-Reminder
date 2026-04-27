# Checklist Persiapan APK (Opsi 1)

Anda memilih untuk membuat APK menggunakan Converter. Berikut adalah hal-hal yang perlu dipastikan sebelum upload:

## 1. Persiapan File
-   [ ] Pastikan Anda menggunakan file **`TaskReminder.html`** yang terbaru (yang sudah ada placeholder API Key-nya).
-   [ ] **PENTING**: Aplikasi ini membutuhkan **Internet** saat dibuka di HP.
    -   Alasannya: Kita menggunakan teknologi CDN (React, Tailwind, Firebase) yang mengambil data dari internet.
    -   Jika HP offline, aplikasi mungkin akan "putih" (blank) atau tidak tampil sempurna.

## 2. Rekomendasi Converter
Saya sarankan mencoba **WebIntoApp.com** karena cukup stabil untuk file HTML tunggal.
1.  Buka [WebIntoApp.com](https://www.webintoapp.com/).
2.  Klik **"Get Started"** atau **"Make App"**.
3.  Di bagian **Content Source**, pilih **"HTML files"**.
4.  Klik box upload dan pilih file `TaskReminder.html` Anda.
5.  **App Name**: Isi "Task Reminder".
6.  **Icon**: (Opsional) Jika punya gambar bujur sangkar, upload sebagai icon. Jika tidak, pakai default saja.
7.  Klik **Next** terus sampai tombol **"Make App"**.
8.  Tunggu proses, lalu download file `.apk` nya.

## 3. Instalasi di HP
-   Saat install, jika muncul peringatan *"Unsafe App"* atau *"Unknown Source"*, itu wajar karena aplikasi ini tidak masuk Play Store.
-   Klik **"Install Anyway"** atau izinkan instalasi dari sumber tidak dikenal.
