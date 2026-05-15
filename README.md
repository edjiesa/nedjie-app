# NEDJIE Corporate Web Application

Selamat datang di repositori web perusahaan **NEDJIE**. Aplikasi ini adalah website *company profile* berdesain premium yang dibangun menggunakan teknologi **Node.js**, **Express.js**, dan **EJS**, serta menggunakan sistem gaya (styling) modern berbasis Vanilla CSS (*Glassmorphism*, aksen *Gold*).

## ✨ Fitur Utama

- **Desain Premium & Elegan**: Menggunakan skema warna *Midnight Blue* dan *Gold* yang memberikan kesan mewah.
- **Glassmorphism UI**: Elemen kartu dan navigasi menggunakan efek kaca (*blur backdrop*) yang sedang tren.
- **Responsive & Mobile-First**: Dioptimalkan untuk tampil sempurna di seluruh ukuran layar mulai dari *smartphone* hingga monitor *desktop*.
- **Animasi Super Mulus**: Terdapat efek transisi, hover (*hover-lift*), dan animasi saat elemen muncul (Intersection Observer/CSS Keyframes).
- **SEO Friendly & Cepat**: Dibangun dengan struktur HTML semantik (Vanilla/EJS) dan aset statis yang ringan.
- **cPanel Ready**: Dirancang secara khusus agar sangat mudah diunggah dan dijalankan melalui fitur **Setup Node.js App** di shared hosting cPanel.

## 🛠️ Teknologi yang Digunakan

- **Backend**: Node.js, Express.js
- **Templating Engine**: EJS (Embedded JavaScript templates)
- **Frontend**: HTML5, Vanilla CSS3, Vanilla JavaScript (Tanpa jQuery)

## 📁 Struktur Direktori

```text
/
├── public/               # File statis (CSS, JS Klien, Gambar)
│   ├── css/
│   │   └── style.css     # File styling utama dengan tema Gold
│   └── js/
│       └── main.js       # Logika interaktivitas UI klien
├── views/                # EJS Templates
│   ├── partials/         # Komponen yang dapat digunakan ulang (header, footer)
│   └── index.ejs         # Halaman utama (Home)
├── .gitignore            # Aturan file yang diabaikan oleh Git
├── package.json          # Konfigurasi proyek & dependensi Node.js
└── server.js             # Entry point aplikasi (konfigurasi Express)
```

## 🚀 Panduan Menjalankan Secara Lokal (Local Development)

Jika Anda ingin mencoba atau memodifikasi aplikasi ini di komputer Anda sendiri, pastikan Anda telah menginstal **Node.js** (disarankan versi LTS).

1. **Kloning Repositori**
   ```bash
   git clone https://github.com/edjiesa/nedjie-app.git
   cd nedjie-app
   ```

2. **Instal Dependensi**
   ```bash
   npm install
   ```

3. **Jalankan Server**
   ```bash
   npm run dev
   # Atau bisa menggunakan: node server.js
   ```

4. **Buka di Browser**
   Buka peramban (browser) Anda dan kunjungi `http://localhost:3000`.

## 🌐 Panduan Deployment ke cPanel

Aplikasi ini disiapkan untuk kemudahan deployment. Ikuti langkah singkat ini:
1. Kompres seluruh file dan folder (kecuali `node_modules` jika ada) menjadi satu file `.zip`.
2. Di cPanel, buka menu **Setup Node.js App** dan buat aplikasi baru (pilih *Application startup file* ke `server.js`).
3. Buka **File Manager**, arahkan ke folder root aplikasi yang baru Anda buat, lalu *Upload* dan *Extract* file `.zip` tadi.
4. Kembali ke menu **Setup Node.js App**, klik tombol **Run NPM Install** pada pengaturan aplikasi Anda.
5. Klik **Restart** dan **Start App**. Website NEDJIE Anda sekarang sudah online!

---
*Dibuat khusus untuk **NEDJIE**.* Hak Cipta Dilindungi Undang-Undang.
