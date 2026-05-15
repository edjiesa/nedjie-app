<div align="center">
  <h1>🌟 NEDJIE Corporate Web Application</h1>
  <p><em>Solusi Profil Perusahaan Modern, Dinamis, & Premium Berbasis Node.js</em></p>
</div>

---

## 📖 Daftar Isi
- [Tentang Proyek](#-tentang-proyek)
- [Fitur Utama](#-fitur-utama)
- [Teknologi yang Digunakan](#-teknologi-yang-digunakan)
- [Struktur Direktori](#-struktur-direktori)
- [Panduan Instalasi Lokal](#-panduan-instalasi-lokal)
- [Panduan Deployment cPanel Lengkap](#-panduan-deployment-cpanel-lengkap)
- [Penyelesaian Masalah Umum (Troubleshooting)](#-penyelesaian-masalah-umum)

---

## 🏢 Tentang Proyek

**NEDJIE** adalah aplikasi web (*Company Profile*) yang dirancang khusus untuk mempresentasikan citra perusahaan secara profesional di ranah digital. Aplikasi ini tidak hanya menyajikan informasi statis, tetapi dibangun di atas infrastruktur **Node.js (Express)**, memungkinkan pengembangan fitur tingkat lanjut di masa depan (seperti API, form kontak dinamis, dan integrasi database). 

Tampilan antarmuka mengusung filosofi desain modern dengan palet warna elegan (*Midnight Blue* dan *Gold*) dipadukan dengan tren *Glassmorphism* untuk kesan korporat yang mewah.

## ✨ Fitur Utama

- **Premium UI/UX:** Transisi halus, *hover states* interaktif, dan efek *glass* pada kartu layanan.
- **Mobile-First & Responsive:** Tampil sempurna pada semua perangkat (Desktop, Tablet, Smartphone).
- **SEO Optimized:** Struktur semantik HTML5 dengan meta tag yang siap dikembangkan.
- **Extensible Architecture:** Menggunakan EJS (Embedded JavaScript) sehingga bagian header dan footer bersifat modular (dapat digunakan ulang di halaman lain).
- **Zero Heavy-Frameworks:** Antarmuka murni menggunakan *Vanilla CSS* dan *Vanilla JavaScript* untuk performa maksimum tanpa *bloatware*.

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi | Deskripsi |
| :--- | :--- | :--- |
| **Backend** | `Node.js` & `Express.js` | Web framework yang cepat dan ringan. |
| **Templating** | `EJS` | Sistem rendering view untuk HTML dinamis. |
| **Styling** | `Vanilla CSS3` | Custom variabel CSS, flexbox, grid, dan keyframes. |
| **Font** | `Google Fonts` | Menggunakan typeface *Outfit* yang modern. |

## 📁 Struktur Direktori

```text
nedjie-app/
│
├── public/                 # Folder statis (dapat diakses publik)
│   ├── css/
│   │   └── style.css       # Sistem desain CSS utama
│   └── js/
│       └── main.js         # Logika interaksi frontend (Navbar, Scroll)
│
├── views/                  # Folder EJS Templates
│   ├── partials/           # Komponen layout terpisah
│   │   ├── header.ejs      # Meta tag & Navigasi atas
│   │   └── footer.ejs      # Navigasi bawah & Copyright
│   └── index.ejs           # Konten halaman utama (Home)
│
├── package.json            # Daftar pustaka & skrip Node.js
├── server.js               # Entry point aplikasi / Konfigurasi Server
└── README.md               # Dokumentasi proyek (File ini)
```

---

## 💻 Panduan Instalasi Lokal (Development)

Jika Anda ingin melakukan pengembangan atau modifikasi antarmuka di komputer lokal, ikuti langkah berikut:

### Persyaratan Sistem:
- **Node.js** (Versi 18 LTS atau yang lebih baru)
- **Git** (Opsional, untuk *cloning*)

### Langkah-langkah:
1. **Unduh Repositori**
   ```bash
   git clone https://github.com/edjiesa/nedjie-app.git
   cd nedjie-app
   ```
2. **Instal Dependensi**
   ```bash
   npm install
   ```
3. **Jalankan Mode Pengembangan**
   ```bash
   npm run dev
   # (atau 'node server.js')
   ```
4. Buka browser dan akses **`http://localhost:3000`**.

---

## 🚀 Panduan Deployment cPanel Lengkap

Proyek ini telah dikonfigurasi agar ramah terhadap lingkungan *Shared Hosting* yang menggunakan fitur **Setup Node.js App** (Phusion Passenger).

### Tahap 1: Persiapan File
1. Buka folder proyek di komputer Anda.
2. Blok semua file (`server.js`, `package.json`, folder `views`, dan `public`).
3. Kompres menjadi format **.zip** (misal: `nedjie_deploy.zip`). *Pastikan Anda tidak menyertakan folder `node_modules` jika ada.*

### Tahap 2: Konfigurasi App di cPanel
1. Login ke **cPanel**, cari menu **Setup Node.js App** (di kategori *Software*).
2. Klik **Create Application**.
3. Isi parameter berikut:
   - **Node.js version:** Pilih versi LTS (misal: `20.x` atau `22.x`).
   - **Application mode:** `Production`
   - **Application root:** Ketik nama folder tempat file akan disimpan (misal: `nedjie-app`).
   - **Application URL:** Pilih domain utama Anda. **PENTING: Kosongkan kotak teks di sebelah kanan domain** agar website tampil di halaman depan, bukan di sub-folder.
   - **Application startup file:** Ketik `server.js`.
4. Klik **Create**. cPanel akan membuat folder *root* tersebut di File Manager.

### Tahap 3: Unggah & Instal
1. Masuk ke **File Manager** cPanel.
2. Buka folder *Application root* yang baru dibuat (contoh: `nedjie-app`).
3. **Hapus** file `app.js` default yang dibuatkan oleh cPanel.
4. Klik **Upload**, unggah file `nedjie_deploy.zip` Anda, lalu **Extract**.
5. Kembali ke menu **Setup Node.js App**, edit aplikasi Anda.
6. Scroll ke bagian bawah, klik tombol **Run NPM Install** untuk mengunduh `express` dan `ejs`.
7. Terakhir, klik tombol **RESTART**. Website Anda sudah online!

---

## ⚠️ Penyelesaian Masalah Umum (Troubleshooting)

| Masalah / Gejala | Penyebab | Solusi Cepat |
| :--- | :--- | :--- |
| **Error "Cannot GET /..."** | Application URL di cPanel disetel dengan sub-path (misal: `/main`). | Edit aplikasi di cPanel, **kosongkan** kotak teks di samping nama domain, lalu Restart App. |
| **Halaman Menampilkan "Coming Soon" atau "Index of /"** | Web server Apache memprioritaskan file `index.html` statis bawaan hosting yang ada di dalam `public_html`. | Buka File Manager, masuk ke `public_html`, cari file `index.html`, `default.html`, atau `index.php` bawaan hosting, lalu **Hapus** atau **Rename** file tersebut. |
| **Desain CSS Tidak Muncul (Teks Berantakan)** | Server gagal merutekan file statis di folder `public` karena letak Application URL tidak di root (`/`). | Pastikan Application URL kosong dari sub-path. Jika terpaksa memakai sub-path, modifikasi path di EJS menjadi absolut sesuai direktori. |

---
*Dikembangkan dengan ❤️ untuk masa depan emas korporasi Anda.*
