# Panduan Instalasi di HP (Mobile App)

Karena Anda ingin menjalankan aplikasi ini di HP (Android/iOS), ada 2 cara paling mudah tanpa perlu ribet coding ulang.

## Opsi 1: Jadikan APK (Web-to-App Converter)
Cara ini akan mengubah file HTML Anda menjadi file `.apk` yang bisa diinstall.

1.  Buka website converter gratis, contohnya: **WebIntoApp.com** atau **AppsGeyser**.
2.  Pilih opsi **"HTML Files"** atau **"Upload Files"** (bukan input URL).
3.  Upload file `TaskReminder.html`.
4.  Isi nama aplikasi (Contoh: "Task Reminder") dan upload icon jika ada.
5.  Klik **Build** / **Download**.
6.  Kirim file `.apk` tersebut ke HP Anda (via WhatsApp/Kabel) dan install.

> **Catatan**: Beberapa converter gratis mungkin menyisipkan iklan atau watermark.

## Opsi 2: PWA (Progressive Web App) - *Rekomendasi*
Aplikasi Anda sebenarnya sudah mendukung PWA (lihat kode `manifest` di `TaskReminder.html`). Ini cara paling bersih dan modern.

### Langkah 1: Hosting Gratis (Drag & Drop)
Agar fitur PWA jalan maksimal, file harus "online" (HTTPS).
1.  Buka **[Netlify Drop](https://app.netlify.com/drop)** (Tanpa daftar akun juga bisa untuk sementara, tapi disarankan daftar gratis).
2.  Tarik (Drag & Drop) folder `TaskReminder` Anda ke area upload.
3.  Tunggu sebentar, Anda akan dapat **Link Website** (contoh: `https://random-name.netlify.app`).

### Langkah 2: Install di HP
1.  Buka Link tersebut di Browser HP (Chrome untuk Android, Safari untuk iPhone).
2.  **Android (Chrome)**:
    -   Klik menu titik tiga (⋮) di pojok kanan atas.
    -   Pilih **"Install App"** atau **"Add to Home Screen"**.
3.  **iPhone (Safari)**:
    -   Klik tombol Share (kotak dengan panah ke atas).
    -   Pilih **"Add to Home Screen"**.

Sekarang aplikasi akan muncul di menu HP Anda seperti aplikasi native biasa, full screen tanpa bar browser!
