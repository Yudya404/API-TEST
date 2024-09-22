# Test-API
A example create API konfiguration
=======
#Product API
Product API adalah RESTful API yang dibangun dengan Node.js, Express.js, dan MariaDB/MySQL. API ini mendukung operasi 
CRUD (Create, Read, Update, Delete) untuk mengelola data product. Aplikasi ini juga dapat dijalankan menggunakan Docker untuk 
memudahkan proses deployment.

#Fitur Utama
- GET /api/products  : Mendapatkan daftar product/ List Product
- POST /api/products  : Menambahkan product baru/ Created Product
- GET /api/products/id  : Mendapatkan detail product berdasarkan ID
- PUT /api/products/id : Memperbarui product berdasarkan ID/ Update Product
- DELETE /api/products/id  : Menghapus product berdasarkan ID/ Delete Product

#Prasyarat Sistem
Sebelum menjalankan aplikasi ini, pastikan Anda telah menginstal perangkat berikut:

Node.js: Versi 14 atau lebih tinggi
MariaDB/MySQL: Versi 10.4.32-MariaDB Database untuk menyimpan data product
Docker: versi 3.8 atau yang lebih tinggi (Opsional) Untuk menjalankan aplikasi dan database dalam container

#Instalasi dan Menjalankan Aplikasi

1. Konfigurasi Variabel Lingkungan
Buat file .env di direktori proyek (misal: test-api) anda untuk menyimpan konfigurasi basis data dan pengaturan server:

DB_HOST=localhost
DB_USER=root
DB_PASS=
DB_NAME=user_management
PORT=3000

*Keterangan
- DB_HOST: Host database (gunakan localhost jika dijalankan secara lokal, atau db jika menggunakan Docker).
- DB_USER: Nama pengguna untuk basis data (misalnya, root).
- DB_PASS: Kata sandi untuk pengguna basis data.
- DB_NAME: Nama database yang digunakan (misalnya, user_management).
- PORT: Port yang digunakan oleh server Node.js (default 3000).

2. Menjalankan Aplikasi Tanpa Docker (Opsional)
2.1. Install Dependencies
Jalankan perintah ini untuk menginstall dependencies yang diperlukan:
 --> npm install
 
2.2. Buat Database di MariaDB/MySQL
Sebelum menjalankan aplikasi, buat database di MariaDB atau MySQL. Gunakan perintah berikut:

3. Menjalankan Aplikasi dengan Docker (Disarankan)
3.1. Setup Docker
Jika Anda lebih memilih menjalankan aplikasi menggunakan Docker, langkah-langkah berikut akan memandu Anda.

3.2. Jalankan Docker Compose
Pastikan Docker dan Docker Compose sudah terinstall. Untuk menjalankan aplikasi dan database, jalankan perintah berikut:
 --> docker-compose up

*Keterangan
Ini akan memulai dua container:
1. db: Container MariaDB dengan database user_management.
2. app: Container Node.js yang menjalankan aplikasi pada port 3000.

3. Menjalankan Aplikasi dengan Node.js langsung Gunakan perintah berikut:
 --> node app.js

#Deployment dengan Docker
Berikut adalah langkah-langkah untuk deployment menggunakan Docker:

1. Pastikan Docker dan Docker Compose sudah terpasang di sistem Anda.
2. Clone repository:
	--> git clone https://github.com/Yudya404/API-TEST
	--> cd user-management-api
3. Jalankan Docker Compose:
	--> docker-compose up
*Keterangan
Docker Compose akan:
1. Membuat container untuk MariaDB dan Node.js.
2. Menginstall dependencies dan melakukan setup database.
3. Menjalankan aplikasi di port 3000.
4. Akses API melalui http://localhost:3000/api/products.

Menghentikan Aplikasi
Jika Anda ingin menghentikan aplikasi dan menghapus container, jalankan perintah:
	--> docker-compose down

Lisensi
Aplikasi ini dilisensikan di bawah MIT License.
