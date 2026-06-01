# ☕ Backseat Barista

![Status](https://img.shields.io/badge/status-production-blue)
![Version](https://img.shields.io/badge/version-1.0.0-green)
![Node.js](https://img.shields.io/badge/Node.js-20.x-green)
![License](https://img.shields.io/badge/license-MIT-orange)

**Backseat Barista** adalah sebuah website e-commerce berbasis AI untuk penjualan minuman (kopi dan non-kopi) serta wadah kolaborasi dengan UMKM F&B. Website ini dikembangkan untuk mengatasi permasalahan pemesanan manual yang selama ini masih berjalan melalui media sosial.

🌐 **Live Demo**: [https://backseatbarista.up.railway.app](https://backseatbarista.up.railway.app)

---

## 📋 Daftar Isi

- [Fitur Utama](#fitur-utama)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Arsitektur Sistem](#arsitektur-sistem)
- [Instalasi & Menjalankan](#instalasi--menjalankan)
  - [Prasyarat](#prasyarat)
  - [Langkah Instalasi](#langkah-instalasi)
- [Struktur Proyek](#struktur-proyek)
- [Pengujian](#pengujian)
- [Tim Pengembang](#tim-pengembang)

---

## ✨ Fitur Utama

### Untuk Pelanggan (Customer)
- Registrasi dan login akun
- Menjelajahi katalog produk (nama, harga, foto, status stok)
- Menambahkan produk ke keranjang belanja
- Mengubah jumlah atau menghapus produk dari keranjang
- Menyimpan produk favorit
- Melakukan checkout pemesanan
- Mengunggah bukti pembayaran manual (transfer bank)
- Melihat riwayat transaksi dan status pesanan

### Untuk Pemilik / Admin
- Login dengan akses khusus admin
- Manajemen produk (tambah, edit, hapus produk)
- Update status stok (Tersedia / Habis)
- Verifikasi pembayaran pelanggan (setujui atau tolak)
- Update status pesanan (Diproses / Selesai)

### Untuk Mitra Bisnis (UMKM F&B)
- Melihat informasi kolaborasi
- Mengisi formulir pendaftaran kolaborasi
- Pengajuan kerja sama tersimpan di database

---

## 🛠 Teknologi yang Digunakan

| Lapisan | Teknologi |
|---------|-----------|
| **Backend** | Node.js, Express.js |
| **Database** | SQLite |
| **Autentikasi** | JWT (JSON Web Token), bcrypt |
| **Frontend** | HTML, CSS, JavaScript |
| **File Upload** | Multer |
| **Deployment** | Railway |

---

## 🏗 Arsitektur Sistem

Sistem ini menggunakan **Layered Architecture** dengan tiga lapisan utama:

1. **Presentation Layer** – Antarmuka pengguna (HTML/CSS/JS)
2. **Business Logic Layer** – Controller (Express.js)
3. **Data Layer** – Database SQLite

### Entity Relationship Diagram (ERD)

Entitas utama yang digunakan:
- **Users** – menyimpan data pelanggan dan admin
- **Products** – menyimpan data produk minuman
- **Carts** – menyimpan item sementara di keranjang
- **Orders** – menyimpan data pesanan
- **OrderItems** – detail item dalam pesanan
- **Favorites** – daftar favorit pelanggan
- **Collaborations** – data pengajuan kolaborasi UMKM

---

## 💻 Instalasi & Menjalankan

### Prasyarat

Pastikan Anda telah menginstal:
- [Node.js](https://nodejs.org/) (versi 20.x atau lebih baru)
- [Git](https://git-scm.com/)

### Langkah Instalasi

1. **Clone repository**
   ```bash
   git clone https://github.com/username/backseat-barista.git
   cd backseat-barista
## Struktur Proyek
backseat-barista/

├── public/

  │   ├── css/            # Stylesheet
  
  │   ├── js/             # Frontend JavaScript
  
  │   └── uploads/        # Folder upload bukti pembayaran
  
├── views/

  │   ├── index.html      # Halaman beranda
  
  │   ├── menu.html       # Halaman katalog produk
  
  │   ├── cart.html       # Halaman keranjang
  
  │   ├── login.html      # Halaman login
  
  │   ├── register.html   # Halaman registrasi
  
  │   ├── dashboard.html  # Dashboard admin
  
  │   └── collaboration.html # Halaman kolaborasi UMKM
  
├── backend/

  │   ├── server.js       # Entry point server
  
  │   ├── database.js     # Konfigurasi SQLite
  
  │   ├── routes/         # Definisi route API
  
  │   └── middleware/     # Middleware (auth, upload)
  
├── .env                # Environment variables

├── package.json

└── README.md

## 🧪 Pengujian

Pengujian dilakukan menggunakan metode Black-Box Testing. Berikut adalah beberapa test case yang telah diuji:

ID Test Case - Fitur	Status
TC_REG_001:	Registrasi dengan data valid	✅ PASSED

TC_LOG_001:	Login dengan data valid	✅ PASSED

TC_KER_001:	Menambah produk ke keranjang	✅ PASSED

TC_FAV_001:	Menambah produk ke favorit	✅ PASSED

TC_PES_001:	Checkout pemesanan	✅ PASSED

TC_VER_001:	Verifikasi pembayaran oleh admin	✅ PASSED

TC_MAP_001:	Admin menambah produk baru	✅ PASSED

Bug yang Ditemukan (Perbaikan di Sprint Selanjutnya)

Validasi email – Sistem masih meloloskan email tanpa karakter '@'
Filter file upload – Sistem masih menerima file PDF untuk bukti bayar

## 👥 Tim Pengembang

Nama - NIM - Peran

Alifia Rahmah	(M0405241064):	Registrasi & Login, Checkout, Riwayat Transaksi, Update Status Pesanan

Abiyyurasyiddhiya Ghulmy P	(M0405241065):	Keranjang, Logout, Upload Bukti, Formulir Kolaborasi

Malika Azkia Kindah	(M0405241066):	Katalog Produk, Favorit, Manajemen Produk, Verifikasi Pembayaran

Mata Kuliah: Rekayasa Perangkat Lunak

Program Studi: Kecerdasan Buatan

Sekolah Sains Data, Matematika dan Informatika

Institut Pertanian Bogor 

Tahun Akademik: 2025/2026 - Semester Genap

📧 Kontak

Untuk pertanyaan lebih lanjut, silakan hubungi:

Website: https://backseatbarista.up.railway.app

<p align="center"> <i>Experience the Art of Coffee</i><br> Dibangun dengan ☕ oleh Tim Backseat Barista </p> 
