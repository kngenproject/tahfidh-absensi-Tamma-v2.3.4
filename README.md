<div align="center">

<br/>

```
████████╗ █████╗ ███╗   ███╗███╗   ███╗ █████╗
╚══██╔══╝██╔══██╗████╗ ████║████╗ ████║██╔══██╗
   ██║   ███████║██╔████╔██║██╔████╔██║███████║
   ██║   ██╔══██║██║╚██╔╝██║██║╚██╔╝██║██╔══██║
   ██║   ██║  ██║██║ ╚═╝ ██║██║ ╚═╝ ██║██║  ██║
   ╚═╝   ╚═╝  ╚═╝╚═╝     ╚═╝╚═╝     ╚═╝╚═╝  ╚═╝
```

### **Tahfidh Juz Amma Management System**

*Solusi digital terintegrasi untuk manajemen program tahfidh Al-Qur'an Juz 30*

<br/>

![Version](https://img.shields.io/badge/versi-3.1-2da55f?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-PWA%20%7C%20Web-0c4a2a?style=for-the-badge)
![License](https://img.shields.io/badge/lisensi-MIT-e6b830?style=for-the-badge)
![Status](https://img.shields.io/badge/status-aktif-22884d?style=for-the-badge)

<br/>

</div>

---

## 📌 Tentang Tamma

**Tamma** adalah aplikasi manajemen tahfidh Juz Amma berbasis web yang dirancang khusus untuk **guru, ustadz, dan pengelola program tahfidh** di sekolah maupun pesantren. Seluruh aplikasi berjalan dalam satu file HTML — tanpa server, tanpa instalasi, tanpa koneksi internet setelah pertama kali dibuka.

> _"Tamma"_ (تَمَّ) bermakna **sempurna / selesai** — mencerminkan tujuan program: khatam hafalan Juz 30.

<br/>

## ✦ Fitur Unggulan

<br/>

### 🏠 Dashboard Interaktif
| Komponen | Deskripsi |
|---|---|
| **Progress Ring** | Visualisasi persentase khatam Juz 30 per siswa |
| **Streak & Poin** | Sistem gamifikasi: hari berturut-turut + total poin ⭐ |
| **Heatmap Aktivitas** | Kalender aktivitas 30 hari terakhir ala GitHub |
| **Target Harian** | Reminder setoran hari ini |
| **Aktivitas Terbaru** | Log aktivitas real-time |

<br/>

### 📝 Manajemen Setoran Tahfidh
- Pencatatan setoran per surat (An-Naba' s.d. An-Nas) dengan rentang ayat
- Status hafalan: **Lancar (L)** atau **Kurang Lancar (KL)**
- Kategori tambahan: Muroja'ah · Tasmi' · Belum Khatam
- **Grid evaluasi ayat** — ketuk langsung ayat yang salah
- Kategori kesalahan: `Tajwid` · `Panjang Pendek` · `Makhraj`
- Riwayat setoran lengkap & export ke `.xlsx`

<br/>

### 📋 Absensi Harian
- Status kehadiran: **Hadir · Ijin · Sakit · Alpha**
- Rekap statistik per siswa otomatis
- Filter per kelas
- Export rekap ke Excel

<br/>

### 📂 Viewer & Analisis Data
- Import file Excel/CSV eksternal
- Filter dinamis berdasarkan status dan kelas
- Drag & drop file langsung ke halaman
- Statistik ringkasan otomatis

<br/>

### 🏅 Gamifikasi
- Sistem poin berdasarkan konsistensi setoran
- Streak harian (hari berturut-turut tanpa absen)
- Leaderboard ranking siswa 🏆
- Sistem lencana / badge pencapaian 🎖️
- Achievement popup saat target tercapai

<br/>

---

## 🚀 Memulai

### Prasyarat

Tidak ada instalasi yang diperlukan. Cukup browser modern:

| Browser | Versi Minimum |
|---|---|
| Google Chrome | 90+ ✅ |
| Safari (iOS) | 14+ ✅ |
| Firefox | 88+ ✅ |
| Microsoft Edge | 90+ ✅ |

<br/>

### Menjalankan Aplikasi

```bash
# Opsi 1 — Buka langsung (paling sederhana)
Klik dua kali file index.html

# Opsi 2 — Server lokal Python
python -m http.server 8000
# → buka http://localhost:8000

# Opsi 3 — Server lokal Node.js
npx serve .
# → buka http://localhost:3000
```

> ⚠️ **Penting:** Buka aplikasi **minimal sekali saat online** agar library XLSX.js dan Chart.js ter-cache untuk penggunaan offline.

<br/>

### Alur Penggunaan Pertama Kali

```
1. Buka index.html di browser
        │
        ▼
2. Siapkan file Excel daftar siswa
   (Kolom A = Nama, Kolom C = Kelas)
        │
        ▼
3. Tab Setoran → tekan "Import" → pilih file Excel
        │
        ▼
4. Mulai catat setoran & absensi harian
        │
        ▼
5. Export Excel kapan saja sebagai backup
```

<br/>

---

## 📊 Format Data Excel

### Import Daftar Siswa

| Kolom | Field | Keterangan |
|---|---|---|
| A | **Nama Siswa** | Wajib diisi |
| B | *(bebas)* | Diabaikan sistem |
| C | **Kelas** | Opsional, untuk filter |

**Contoh isi file:**

```
| A                  | B    | C      |
|--------------------|------|--------|
| Ahmad Fauzi        | -    | VII A  |
| Siti Rahmawati     | -    | VII B  |
| Muhammad Rizky     | -    | VIII A |
```

<br/>

### Format Export Setoran

| Field | Deskripsi |
|---|---|
| Nama | Nama siswa |
| Tanggal | Tanggal setoran |
| Surat | Nama surat yang disetorkan |
| Rentang Ayat | Misal: `1-10` |
| Status | `L` atau `KL` |
| Jml Salah | Jumlah ayat salah |
| Ayat Salah | Nomor ayat yang salah |
| Kategori | Jenis kesalahan |
| Tambahan | Muroja'ah / Tasmi' / dll |

<br/>

---

## 🗃️ Penyimpanan Data

Semua data disimpan di **localStorage** browser — tidak ada data yang dikirim ke server manapun.

```
localStorage
├── db_master_siswa      → Daftar siswa (nama + kelas)
├── db_setoran           → Riwayat seluruh setoran hafalan
├── db_absensi_harian    → Riwayat absensi harian
├── db_points            → Poin gamifikasi per siswa
└── db_streaks           → Streak harian per siswa
```

> ⚠️ **Backup rutin sangat disarankan.** Data dapat hilang jika cache browser dihapus. Lakukan export Excel secara berkala sebagai cadangan permanen.

<br/>

---

## 🔌 Dependensi

| Library | Versi | Fungsi | Sumber |
|---|---|---|---|
| [XLSX.js](https://github.com/SheetJS/sheetjs) | `0.18.5` | Import & export Excel | cdnjs |
| [Chart.js](https://www.chartjs.org/) | latest | Grafik statistik | jsDelivr |
| [Font Awesome](https://fontawesome.com/) | `6.4.0` | Ikon antarmuka | cdnjs |

Semua library dimuat via CDN — tidak ada `npm install` yang diperlukan.

<br/>

---

## 📱 Progressive Web App (PWA)

Tamma dapat diinstal sebagai aplikasi native di perangkat mobile maupun desktop.

**Cara Instalasi:**

```
Android (Chrome)
└── Menu ⋮  →  "Tambahkan ke layar utama"

iOS (Safari)
└── Tombol Bagikan □↑  →  "Tambahkan ke Layar Utama"

Desktop (Chrome)
└── Ikon install ⊕ di address bar
```

**Keunggulan sebagai PWA:**
- ✅ Dapat digunakan **offline penuh** setelah dibuka sekali online
- ✅ Tampil seperti aplikasi native (tanpa address bar)
- ✅ Safe area otomatis untuk iPhone (notch & gesture bar)
- ✅ Dukungan notifikasi push untuk reminder mengaji
- ✅ Responsif di semua ukuran: HP · Tablet · Desktop

<br/>

---

## 📁 Struktur Proyek

```
tamma/
└── index.html          ← Seluruh aplikasi dalam satu file
                          (HTML + CSS + JavaScript)
```

Aplikasi dikemas dalam **satu file tunggal** untuk kemudahan distribusi — cukup kirim satu file via WhatsApp atau Google Drive, langsung bisa digunakan tanpa setup apapun.

<br/>

---

## 🗺️ Roadmap

- [x] Pencatatan setoran hafalan Juz 30
- [x] Absensi harian siswa
- [x] Sistem gamifikasi (poin, streak, badge, leaderboard)
- [x] Export Excel (setoran & absensi)
- [x] PWA & offline support
- [x] Filter per kelas
- [ ] Sinkronisasi cloud (Google Drive / Dropbox)
- [ ] Dukungan multi-ustadz / multi-halaqah
- [ ] Laporan PDF otomatis
- [ ] Notifikasi jadwal setoran terjadwal
- [ ] Statistik perbandingan antar kelas

<br/>

---

## 🤝 Kontribusi

Kontribusi sangat disambut! Silakan ikuti alur berikut:

1. **Fork** repositori ini
2. Buat branch fitur baru
   ```bash
   git checkout -b fitur/nama-fitur
   ```
3. Commit perubahan
   ```bash
   git commit -m "feat: deskripsi singkat perubahan"
   ```
4. Push ke branch
   ```bash
   git push origin fitur/nama-fitur
   ```
5. Buat **Pull Request** dan deskripsikan perubahan yang dibuat

<br/>

---

## 📜 Lisensi

Proyek ini menggunakan lisensi **MIT** — bebas digunakan, dimodifikasi, dan didistribusikan untuk keperluan pendidikan dan non-komersial.

```
MIT License — Copyright (c) 2025 Tamma Project
```

<br/>

---

<div align="center">

<br/>

**Tamma v3.1** · Tahfidh Juz Amma Management System

Dibuat dengan ❤️ untuk kemudahan manajemen program Tahfidh Al-Qur'an

<br/>

> *"خَيْرُكُمْ مَنْ تَعَلَّمَ الْقُرْآنَ وَعَلَّمَهُ"*
>
> _"Sebaik-baik kalian adalah yang mempelajari Al-Qur'an dan mengajarkannya."_
> — HR. Bukhari

<br/>

</div>
