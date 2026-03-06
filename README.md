Tamma - Tahfidh Juz Amma

Aplikasi Progressive Web App (PWA) untuk manajemen setoran hafalan Juz 30 (Juz Amma) dan absensi harian siswa. Dirancang khusus untuk guru TPQ/TPA, ustadz/ustadzah, atau lembaga tahfidh yang ingin mencatat perkembangan hafalan dan kehadiran siswa secara praktis, offline, dan tanpa database server.

data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj48cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgcng9IjExMiIgZmlsbD0iIzBjNGEyYSIvPjx0ZXh0IHg9IjI1NiIgeT0iMzIwIiBmb250LXNpemU9IjI4MCIgdGV4dC1hbmNob3I9Im1pZGRsZSI+8J+VjDwvdGV4dD48L3N2Zz4=

---

Fitur Unggulan

· 📖 Manajemen Setoran Juz 30
    Catat setoran harian per surat dan ayat, status lancar/kurang lancar, ayat yang salah, serta kategori kesalahan (Tajwid, Panjang Pendek, Makhraj).
· 👥 Absensi Harian Terintegrasi
    Tandai kehadiran siswa (Hadir, Ijin, Sakit, Alpha) dengan tampilan kartu per siswa. Data siswa diimpor sekali untuk digunakan di semua fitur.
· 📊 Dashboard & Analitik
    Lihat progress hafalan, streak harian, total poin, heatmap aktivitas 30 hari terakhir, target hari ini, dan aktivitas terbaru.
· 🏆 Gamifikasi
    Dapatkan poin setiap setoran (10 poin lancar, 5 poin kurang lancar), streak harian, dan lencana pencapaian (badge) seperti Langkah Pertama, Pemula Rajin, Khatam Juz 30, dll.
· 📈 Statistik & Leaderboard
    Grafik performa mingguan, perbandingan antar siswa, leaderboard, dan insight AI berdasarkan pola mengaji.
· 📂 Viewer File Excel
    Upload file setoran/absensi (format .xlsx, .xls, .csv) untuk melihat dan memfilter data dengan cepat.
· 💾 Offline First & PWA
    Semua data tersimpan di localStorage perangkat. Aplikasi dapat dipasang ke layar utama (seperti aplikasi native) dan tetap berfungsi tanpa koneksi internet.
· 📱 Responsif & Mobile Friendly
    Tampilan dioptimalkan untuk layar kecil dengan navigasi bottom bar, gesture swipe antar halaman, dan dukungan safe area (notch/gesture bar).

---

Cara Penggunaan

1. Import Data Siswa

· Buka tab Tahfidh.
· Klik tombol Import dan pilih file Excel dengan format:
  · Kolom A: Nama siswa
  · Kolom C: Kelas (opsional)
· Data siswa akan tersimpan dan muncul di tab Tahfidh maupun Absensi.

2. Mencatat Setoran Hafalan

· Pilih siswa, surat, rentang ayat, status (Lancar/Kurang Lancar), dan tambahan (opsional).
· Ketuk ayat-ayat yang salah pada grid untuk menandainya.
· Klik Simpan. Poin dan streak akan otomatis bertambah.

3. Absensi Harian

· Buka tab Absen.
· Pada setiap kartu siswa, pilih status kehadiran.
· Klik Simpan Excel untuk mengunduh laporan absensi hari ini.
· Gunakan tombol Reset Hari Ini untuk mengosongkan absensi.

4. Melihat Statistik

· Tab Statistik menampilkan grafik performa pribadi, leaderboard kelas, dan tren 30 hari terakhir.
· Klik badge atau leaderboard untuk detail.

5. Viewer File

· Upload file Excel setoran/absensi di tab Viewer untuk melihat data dengan filter dan pencarian.

6. Instalasi sebagai Aplikasi

· Saat pertama kali dibuka di HP, akan muncul banner Install (jika browser mendukung PWA).
· Atau melalui menu browser: Add to Home screen.

---

Teknologi yang Digunakan

· HTML5, CSS3, JavaScript (ES6) – Struktur dan logika aplikasi.
· Font Awesome 6 – Ikon-ikon antarmuka.
· SheetJS (XLSX) – Membaca dan menulis file Excel.
· Chart.js – Visualisasi grafik statistik.
· Service Worker – Caching aset dan dukungan offline.
· LocalStorage – Penyimpanan data persisten di browser.
· PWA Manifest – Agar dapat diinstal sebagai aplikasi.

---

Lisensi

Aplikasi ini bersifat open source dan dapat digunakan, dimodifikasi, serta didistribusikan kembali dengan tetap menyertakan atribusi kepada pembuat asli.
Dikembangkan oleh Tim Tamma untuk kemajuan pendidikan Al-Qur'an.

---

Catatan: Semua data tersimpan di perangkat pengguna. Tidak ada data yang dikirim ke server. Pastikan untuk mencadangkan data secara berkala dengan mengunduh laporan Excel.
