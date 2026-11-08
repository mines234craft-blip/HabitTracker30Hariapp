# 30 Days Habit Tracker — Proyek APK

## Cara mendapatkan APK (tanpa memasang apa pun di komputer)

1. Buat akun di https://github.com (gratis), lalu buat repositori baru (boleh private).
2. Unggah **seluruh isi folder ini** ke repositori itu (tombol "Add file" → "Upload files").
   Pastikan folder `.github` ikut terunggah. Kalau folder tersembunyi tidak ikut terpilih,
   buat file manual lewat "Create new file" dengan nama `.github/workflows/build-apk.yml`
   dan salin isinya.
3. Buka tab **Actions** → pilih workflow **Build APK** → **Run workflow**.
   (Build juga jalan otomatis setiap ada push ke branch main.)
4. Tunggu sekitar 5–8 menit sampai hijau. Buka run tersebut, lalu unduh
   **habit-tracker-apk** di bagian *Artifacts* (berupa zip berisi `app-debug.apk`).
5. Kirim `app-debug.apk` ke HP, buka, lalu izinkan "Instal dari sumber tidak dikenal" bila diminta.

## Catatan

- APK ini berjenis debug (ditandatangani kunci debug): cukup untuk dipakai pribadi, tidak untuk Play Store.
- Progres tersimpan di penyimpanan aplikasi (localStorage), bukan di browser.
- Tombol "Unduh progres CSV" memakai unduhan browser dan mungkin tidak berfungsi di WebView Android.
  Kalau dibutuhkan, bisa diganti dengan plugin Share/Filesystem Capacitor.
- Mengubah tampilan: edit `www/index.html`, lalu jalankan ulang workflow.
