# Panduan Build dengan Android Studio (Native WebView)

Karena Anda memilih menggunakan Android Studio, kita akan membuat aplikasi Android sederhana yang berfungsi sebagai "pembungkus" (WebView) untuk file html Anda. Cara ini **tidak memerlukan Node.js**.

## Prasyarat
-   Android Studio sudah terinstall.
-   Koneksi Internet (karena aplikasi Anda meload React/Tailwind dari CDN).

## Langkah 1: Buat Project Baru
1.  Buka Android Studio.
2.  Klik **New Project**.
3.  Pilih **Empty Views Activity** (Pastikan pilih yang "Views", bukan "Compose" agar lebih simpel untuk pemula).
4.  **Name**: Task Reminder.
5.  **Language**: Java (atau Kotlin, panduan ini menggunakan Java agar umum).
6.  Klik **Finish** dan tunggu Gradle selesai loading.

## Langkah 2: Siapkan Aset HTML
1.  Di panel Project (kiri), cari folder `app` > `src` > `main`.
2.  Klik kanan pada folder **`main`** -> **New** -> **Directory**.
3.  Beri nama `assets` (huruf kecil semua).
4.  Copy file **`TaskReminder.html`** Anda.
5.  Paste ke dalam folder `assets` yang baru dibuat tadi.

## Langkah 3: Edit AndroidManifest.xml
Kita butuh izin internet karena aplikasi mengambil script React dan Tailwind dari web.
1.  Buka `app` > `manifests` > `AndroidManifest.xml`.
2.  Tambahkan kode izin internet **di atas tag `<application`**:

```xml
<!-- Tambahkan baris ini -->
<uses-permission android:name="android.permission.INTERNET" />

<application ...>
```

## Langkah 4: Edit Layout (activity_main.xml)
Ubah tampilan utama menjadi WebView penuh.
1.  Buka `app` > `res` > `layout` > `activity_main.xml`.
2.  Ganti **SEMUA** kodenya dengan ini:

```xml
<?xml version="1.0" encoding="utf-8"?>
<WebView xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/webview"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

## Langkah 5: Coding Java (MainActivity.java)
Hubungkan WebView dengan file HTML.
1.  Buka `app` > `java` > (nama paket anda) > `MainActivity.java`.
2.  Ganti isinya (pertahankan baris `package` paling atas) dengan:

```java
// Pertahankan baris package di sini...

import android.os.Bundle;
import android.webkit.WebSettings;
import android.webkit.WebView;
import android.webkit.WebViewClient;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        WebView myWebView = findViewById(R.id.webview);
        WebSettings webSettings = myWebView.getSettings();
        
        // Aktifkan JavaScript (Wajib untuk React)
        webSettings.setJavaScriptEnabled(true);
        // Aktifkan Local Storage (Untuk simpan data misi)
        webSettings.setDomStorageEnabled(true); 
        
        // Agar link tetap buka di aplikasi yang sama
        myWebView.setWebViewClient(new WebViewClient());

        // Load file HTML dari folder assets
        myWebView.loadUrl("file:///android_asset/TaskReminder.html");
    }
}
```

## Langkah 6: Build APK
1.  Klik menu **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**.
2.  Tunggu notifikasi "Build APK(s): APK(s) generated successfully".
3.  Klik **locate** di notifikasi itu untuk mengambil file `.apk` nya.
4.  Install di HP Anda!
