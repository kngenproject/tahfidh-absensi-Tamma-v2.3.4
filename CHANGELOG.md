# Changelog

Semua perubahan penting pada proyek ini didokumentasikan di sini.  
Format mengikuti [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [2.4.0] — 2026-03-06

### Ditambahkan
- **Filter siswa di Beranda** — dropdown pilih siswa di bagian atas dashboard; semua komponen (Progress Ring, Streak, Poin, Heatmap, Target Hari Ini, Aktivitas Terbaru) otomatis difilter berdasarkan siswa yang dipilih
- **Export Absensi Per Kelas** — tombol baru di tab Absensi yang menghasilkan file Excel terpisah per kelas dengan nama file menyertakan nama kelas dan tanggal (contoh: `absensi_7A_2026-03-06.xlsx`)
- **Offline-first Service Worker** — strategi cache-first dengan pre-caching semua aset CDN (Font Awesome, XLSX, Chart.js) saat install; aplikasi kini berjalan penuh tanpa koneksi setelah dibuka sekali saat online
- **Fallback UI saat offline** — tombol export di-disable dengan tooltip informatif jika library belum ter-cache; grafik diganti pesan penjelasan
- **Toast notifikasi online/offline** — informasi status koneksi real-time kepada pengguna

### Diperbaiki
- **Bug: `hapusSemuaDataSiswa` tidak reset dropdown beranda** — setelah semua data dihapus, dropdown filter siswa di beranda tidak kembali ke "Semua Siswa"; kini `activeDashboardSiswa` direset ke `'SEMUA'` secara otomatis
- **Bug: deklarasi variabel `vData`/`vFil`/`vCols` ganda** — variabel dideklarasi dua kali menyebabkan potensi konflik; dipindahkan ke satu deklarasi global bersama variabel lainnya
- **Icon notifikasi dari URL eksternal** — icon push notification sebelumnya mengambil dari `cdn-icons-png.flaticon.com`; diganti ke SVG inline agar berfungsi saat offline

### Diubah
- Service Worker lama (network-first tanpa pre-cache) diganti total dengan implementasi cache-first yang benar
- `updateDashboard()` kini memanggil `updateDashboardSiswaDropdown()` sehingga dropdown selalu sinkron dengan data terbaru
- Export per kelas menghasilkan file terpisah (bukan multi-sheet dalam satu file) untuk kemudahan distribusi

---

## [2.3.4] — Sebelumnya

### Fitur yang sudah ada
- Form setoran Juz 30 lengkap (37 surat An-Naba' s/d An-Nas) dengan evaluasi per ayat
- Import daftar siswa dari Excel (Kolom A = Nama, Kolom C = Kelas)
- Absensi harian dengan status Hadir / Ijin / Sakit / Alpha
- Dashboard dengan Progress Ring, Streak, Poin, Heatmap aktivitas 30 hari
- Statistik 3 tab: Pribadi, Kelas, Trend dengan Chart.js
- Leaderboard dan sistem lencana (badges)
- Viewer file Excel riwayat setoran/absensi dari luar
- Download laporan Excel (setoran, absensi, gabungan)
- Filter kelas di tab Tahfidh, Absensi, dan Viewer
- PWA dasar dengan manifest dan Service Worker
- Pengaturan ukuran font
- Notifikasi reminder mengaji harian
- Mode offline indicator