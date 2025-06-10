==============================
Panduan Instalasi Aplikasi Dompetku
==============================

Terima kasih telah menggunakan Dompetku. Ikuti langkah-langkah di bawah ini untuk menjalankan aplikasi di lingkungan pengembangan lokal Anda (misalnya menggunakan XAMPP, WAMP, atau MAMP).

---
Langkah 1: Pengaturan Database
---
1.  Buka phpMyAdmin atau klien SQL pilihan Anda.
2.  Buat database baru dengan nama `finance_app`. Anda bisa menggunakan perintah SQL: `CREATE DATABASE finance_app;`
3.  Pilih database `finance_app` yang baru dibuat.
4.  Impor file `database.sql` yang telah disediakan ke dalam database ini. File ini akan membuat semua tabel yang diperlukan (`users`, `transactions`, `categories`, dll.) dan mengisi beberapa data contoh (dummy data).

---
Langkah 2: Konfigurasi Aplikasi
---
1.  Buka file `config/database.php` di editor kode Anda.
2.  Ubah nilai variabel `$db_host`, `$db_name`, `$db_user`, dan `$db_pass` agar sesuai dengan konfigurasi server database MySQL Anda.

    // Contoh konfigurasi untuk XAMPP default:
    $db_host = 'localhost';
    $db_name = 'finance_app';
    $db_user = 'root'; // User default XAMPP
    $db_pass = '';     // Password default XAMPP kosong

---
Langkah 3: Menjalankan Aplikasi
---
1.  Letakkan seluruh folder proyek `dompetku` di dalam direktori root server web Anda.
    * Untuk XAMPP: `C:/xampp/htdocs/dompetku`
    * Untuk WAMP: `C:/wamp/www/dompetku`
2.  Pastikan server Apache dan MySQL Anda berjalan.
3.  Buka browser web Anda dan arahkan ke: `http://localhost/dompetku/auth/login.php`

Anda sekarang dapat login menggunakan akun contoh:
-   **Username**: user01
-   **Password**: user123

---
Struktur Direktori Proyek
---
- `/config`       : File koneksi database.
- `/includes`     : Header, footer, dan fungsi-fungsi pembantu.
- `/auth`         : Skrip untuk login, registrasi, dan logout.
- `/public`       : Halaman utama yang diakses pengguna (Dashboard, Transaksi, dll).
- `/assets`       : Untuk file CSS dan JavaScript kustom.
- `README.txt`    : File panduan ini.