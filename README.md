# 📖 Tamma — Tahfidh Juz Amma

Aplikasi web progresif (PWA) untuk mencatat dan memantau setoran hafalan Juz 30, absensi harian, dan perkembangan siswa. Dirancang untuk digunakan guru/ustadz di kelas tahfidh, dapat diinstall di ponsel dan berjalan sepenuhnya secara offline.

---

## ✨ Fitur Utama

### 🏠 Beranda (Dashboard)
- **Filter per siswa** — pantau progress, streak, poin, dan aktivitas masing-masing siswa secara individual
- **Progress Ring Juz 30** — visualisasi persentase surat yang sudah disetor
- **Streak harian** — hitungan hari berturut-turut siswa aktif menyetor
- **Heatmap 30 hari** — kalender aktivitas setoran bergaya GitHub contribution graph
- **Target hari ini** — tampilkan setoran terakhir hari ini beserta statusnya
- **Aktivitas terbaru** — 5 setoran terbaru secara real-time

### 📝 Tahfidh (Setoran)
- Form setoran Juz 30 lengkap: pilih siswa, surat (An-Naba' s/d An-Nas), rentang ayat
- **Evaluasi ayat** — ketuk ayat yang salah, tandai kategori (Tajwid / Panjang Pendek / Makhraj)
- Status setoran: Lancar (L) / Kurang Lancar (KL)
- Tambahan: Belum Khatam / Muroja'ah / Tasmi'
- Riwayat setoran dengan tabel lengkap + tombol hapus per baris
- Filter kelas pada form setoran
- Import daftar siswa dari file Excel (Kolom A = Nama, Kolom C = Kelas)
- **Download laporan Excel** — setoran saja, atau gabungan setoran + absensi

### 📋 Absensi
- Kartu absensi per siswa dengan tombol cepat: Hadir / Ijin / Sakit / Alpha
- Filter kelas pada daftar siswa
- Statistik ringkasan: total hadir, ijin, sakit, alpha
- Riwayat absensi hari ini
- **Simpan Excel** — satu file semua siswa
- **Export Per Kelas** — file terpisah per kelas (`absensi_7A_2026-03-06.xlsx`, dst.) untuk kemudahan distribusi ke wali kelas

### 📊 Statistik & Analitik
- **Tab Pribadi** — grafik performa mingguan, statistik detail (total setoran, rata-rata ayat/hari, persentase lancar, surat terbanyak, khatam count), lencana pencapaian
- **Tab Kelas** — grafik perbandingan antar siswa, leaderboard ranking
- **Tab Trend** — grafik trend 30 hari terakhir, insight analisis pola mengaji

### 📂 Viewer
- Upload file Excel riwayat setoran atau absensi dari luar
- Filter berdasarkan status (Lancar, Kurang Lancar, Hadir, Ijin, Sakit, Alpha)
- Filter kelas pada data viewer
- Hapus baris data langsung dari viewer

### ⚙️ Tentang / Pengaturan
- Manajemen data siswa (lihat daftar, hapus semua)
- Pengaturan ukuran font (Kecil / Normal / Sedang / Besar)
- Aktifkan notifikasi reminder mengaji harian (jam 16.00)
- Informasi aplikasi dan versi

---

## 📲 Instalasi sebagai Aplikasi

Tamma adalah PWA — dapat diinstall langsung dari browser tanpa perlu App Store:

1. Buka file `index.html` di browser (Chrome / Safari / Edge)
2. Buka sekali saat ada koneksi internet agar aset ter-cache
3. Klik banner **"Pasang sebagai Aplikasi"** atau gunakan menu browser → *Add to Home Screen*
4. Aplikasi siap digunakan offline sepenuhnya

---

## 🔌 Offline Support

Semua fitur inti berjalan tanpa koneksi internet setelah dibuka sekali saat online:

| Fitur | Online | Offline |
|---|---|---|
| Setoran & absensi | ✅ | ✅ |
| Progress & dashboard | ✅ | ✅ |
| Export Excel | ✅ | ✅ (jika sudah pernah online) |
| Grafik statistik | ✅ | ✅ (jika sudah pernah online) |
| Ikon Font Awesome | ✅ | ✅ (jika sudah pernah online) |

Data disimpan di `localStorage` browser — tidak memerlukan server atau database.

---

## 📁 Struktur Data Excel Import

### Import Daftar Siswa
| Kolom A | Kolom B | Kolom C |
|---|---|---|
| Nama Siswa | *(bebas)* | Kelas |

### Export Setoran
| Tanggal | Nama | Surat | Rentang | Status | Jml Salah | Ayat Salah | Kategori | Tambahan |
|---|---|---|---|---|---|---|---|---|

### Export Absensi
| No | Nama | Kelas | Status | Waktu |
|---|---|---|---|---|

---

## 🛠️ Teknologi

- **Vanilla HTML/CSS/JS** — tidak ada framework, tidak ada build step
- **Chart.js** — grafik statistik
- **SheetJS (XLSX)** — baca dan tulis file Excel
- **Font Awesome 6** — ikon
- **Service Worker + Cache API** — offline-first PWA
- **localStorage** — penyimpanan data lokal

---

## 🚀 Cara Pakai

1. Clone atau download repository ini
2. Buka `index.html` langsung di browser (tidak perlu server)
3. Import daftar siswa via Excel di tab **Tahfidh**
4. Mulai catat setoran dan absensi

```bash
git clone https://github.com/username/tamma-tahfidh.git
cd tamma-tahfidh
# Buka index.html di browser
```

---

## 📄 Lisensi

MIT License — bebas digunakan dan dimodifikasi untuk kebutuhan pendidikan.