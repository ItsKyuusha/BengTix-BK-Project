# 🎫 BengTix  
**Sistem Ticketing Konser Berbasis Web (Non-Payment)**

## 📌 Overview
**BengTix** adalah aplikasi simulasi sistem pemesanan tiket konser berbasis web yang dibangun menggunakan **Laravel 12** dengan **Laravel Breeze** untuk autentikasi.  
Aplikasi ini tidak menggunakan sistem pembayaran (non-payment), sehingga setiap pemesanan tiket yang dilakukan user akan langsung tercatat sebagai transaksi.

Tujuan utama pengembangan BengTix:
- Memahami alur bisnis sistem ticketing konser
- Menerapkan konsep **CRUD**
- Mengimplementasikan arsitektur **MVC (Model–View–Controller)** pada Laravel

---

## 🛠️ Tools & Technology
- PHP ≥ 8.2  
- Laravel 12  
- Laravel Breeze  
- MySQL  
- Composer  
- Visual Studio Code  

---

## 🚀 Fitur Aplikasi

### 👤 Admin
- Manajemen Event (CRUD)
- Manajemen Kategori Event (CRUD)
- Manajemen Tiket (CRUD & pengaturan kuota)
- Melihat Riwayat Transaksi User

### 👥 User
- Melihat Daftar Event
- Filter Event Berdasarkan Kategori
- Pemesanan Tiket (tanpa pembayaran)
- Melihat Riwayat Pemesanan Tiket

### 🔐 Autentikasi
- Login
- Register
- Logout  
(menggunakan Laravel Breeze)

---

## 🎭 Role & Hak Akses

| Role  | Hak Akses |
|------|-----------|
| Admin | Mengelola event, kategori, tiket, dan transaksi |
| User  | Melihat event, memesan tiket, dan melihat riwayat pemesanan |

---

## 📊 Use Case Utama

### Admin
- Login ke sistem
- Kelola Event
- Kelola Kategori Event
- Kelola Tiket
- Melihat Riwayat Transaksi

### User
- Login / Registrasi
- Melihat dan mencari event
- Memesan tiket
- Melihat riwayat pemesanan

---

## 🗂️ Struktur Database
Tabel utama yang digunakan:
- `users`
- `kategori`
- `events`
- `tikets`
- `orders`
- `detail_orders`

Relasi database:
- Event memiliki kategori
- Event memiliki banyak tiket
- User dapat melakukan banyak order
- Order memiliki detail tiket yang dipesan

---

## ⚙️ Cara Menjalankan Project

1. Clone repository
   ```bash
   git clone https://github.com/username/bengtix.git
2. Masuk ke folder project
   ```bash
   cd bengtix
3. Install dependency
   ```bash
   composer install
   npm install
   npm run build
4. Copy file environment
   ```bash
   cp .env.example .env
5. Copy file environment
   ```bash
   php artisan key:generate
6. Konfigurasi database di file .env
7. Jalankan migrasi
   ```bash
   php artisan migrate
8. Jalankan seeder
   ```bash
   php artisan db:seed
9. Jalankan server
   ```bash
   php artisan server