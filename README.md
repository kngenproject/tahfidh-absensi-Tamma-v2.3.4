# 📖 Tamma — Tahfidh Juz Amma

Aplikasi web progresif (PWA) untuk pencatatan dan monitoring setoran hafalan Juz 30 (Juz Amma). Dirancang khusus untuk guru/ustadz tahfidh agar mudah merekam dan menganalisis progres hafalan siswa.

---

## ✨ Fitur Utama

- **📝 Setoran Hafalan** — Catat setoran per siswa, pilih surat, ayat, status lancar/kurang lancar, dan ayat yang salah
- **📅 Absensi Harian** — Rekam kehadiran siswa (Hadir, Ijin, Sakit, Alpha)
- **📊 Dashboard & Statistik** — Grafik progres hafalan, persentase kehadiran, leaderboard poin
- **👀 Viewer Data** — Import & tampilkan file Excel (.xlsx/.xls/.csv) hasil export
- **🏆 Gamifikasi** — Poin dan lencana untuk memotivasi siswa
- **📱 PWA** — Bisa diinstall di HP, bekerja offline
- **💾 Lokal Storage** — Data tersimpan di browser, tanpa server/database

---

## 🚀 Cara Deploy ke GitHub Pages

### 1. Buat Repository Baru
- Buka [github.com](https://github.com) → **New repository**
- Nama repo: `tamma` (atau sesuai keinginan)
- Set ke **Public**
- Klik **Create repository**

### 2. Upload File
Upload semua file berikut ke repository:

```
tamma/
├── index.html          ← Aplikasi utama
├── manifest.json       ← Konfigurasi PWA
├── sw.js               ← Service Worker (offline support)
├── README.md           ← Dokumentasi ini
└── icons/
    ├── icon-192.png    ← Icon PWA kecil
    ├── icon-512.png    ← Icon PWA besar
    └── favicon.png     ← Favicon browser
```

### 3. Aktifkan GitHub Pages
- Di repository → **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main** → folder: **/ (root)**
- Klik **Save**

### 4. Akses Aplikasi
Setelah beberapa menit, aplikasi bisa diakses di:
```
https://<username>.github.io/<nama-repo>/
```

---

## 📁 Struktur File

| File | Keterangan |
|------|------------|
| `index.html` | Seluruh aplikasi (HTML + CSS + JS dalam 1 file) |
| `manifest.json` | Metadata PWA untuk instalasi di HP |
| `sw.js` | Service Worker untuk mode offline |
| `icons/` | Icon aplikasi berbagai ukuran |

---

## 📱 Cara Install di HP (PWA)

**Android (Chrome):**
1. Buka URL aplikasi di Chrome
2. Tap ikon **⋮** (menu) → **"Tambahkan ke layar utama"**
3. Atau tunggu banner install muncul → tap **Pasang**

**iOS (Safari):**
1. Buka URL aplikasi di Safari
2. Tap ikon **Share** (kotak dengan panah ke atas)
3. Pilih **"Add to Home Screen"**

---

## 🛠️ Teknologi

- HTML5 + CSS3 + Vanilla JavaScript
- [Chart.js](https://www.chartjs.org/) — Grafik statistik
- [SheetJS (xlsx)](https://sheetjs.com/) — Import/export Excel
- [Font Awesome](https://fontawesome.com/) — Icon
- PWA (Service Worker + Web App Manifest)
- localStorage — Penyimpanan data lokal

---

## 📊 Format Excel untuk Import

Kolom yang dikenali saat import file Excel:

| Kolom | Nama yang Diterima |
|-------|--------------------|
| Tanggal | `tanggal`, `date` |
| Nama Siswa | `nama siswa`, `nama`, `name` |
| Surat | `surat` |
| Rentang Ayat | `rentang ayat`, `rentang`, `ayat` |
| Status | `status` |
| Jumlah Salah | `jml salah`, `jumlah salah` |
| Ayat Salah | `ayat salah` |
| Kategori | `kategori salah`, `kategori`, `ket` |
| Kelas | `tambahan`, `kelas`, `catatan` |
| Waktu | `waktu`, `time` |

---

## 📄 Lisensi

Dibuat untuk keperluan pendidikan tahfidh. Bebas digunakan dan dimodifikasi.

---

> **Versi:** 2.3.4 | Dibuat dengan ❤️ untuk kemudahan guru tahfidh
