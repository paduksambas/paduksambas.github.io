# MD V14 — Paduka Sambas

Situs utama: https://paduksambas.github.io/

Halaman utama ini menampilkan dashboard publik dari repositori aplikasi:
https://github.com/paduksambas/MD-V14-PADUKA-SAMBAS

## Arsitektur publikasi

- Repositori ini (paduksambas.github.io) berisi halaman pembungkus GitHub Pages.
- Dashboard aplikasi dibangun dan diterbitkan secara terpisah oleh workflow GitHub Actions pada repositori MD V14.
- Halaman utama menampilkan dashboard tersebut melalui iframe satu-origin agar alamat utama tetap singkat.
- Jika diperlukan, dashboard dapat dibuka langsung di https://paduksambas.github.io/MD-V14-PADUKA-SAMBAS/.

## Keamanan dan privasi

- Kedua repositori bersifat publik. Jangan menyimpan token, kata sandi, data pribadi, atau laporan internal di dalamnya.
- Dashboard publik hanya menerbitkan HTML statis. Workflow build memverifikasi bahwa direktori publik hanya berisi index.html, tanpa file JSON laporan atau database.
- Data analisis adalah snapshot dari siklus pengumpulan/build terakhir, bukan streaming real-time.
- Workflow monitoring terpisah tidak mengunggah laporan, dashboard hasil monitoring, atau database SQLite sebagai artifact.

## Pembaruan

Untuk memperbarui isi dashboard, ubah kode pada repositori MD V14 dan pastikan pemeriksaan serta deployment GitHub Actions berhasil. Halaman utama akan tetap menunjuk ke alamat dashboard proyek yang sama.
