# Aplikasi CRUD Data Pengguna dengan Node.js, Express, dan Multer (Web Pemrograman - Bu Andita Pertama S.Kom., M.Kom.)

![Image](https://github.com/user-attachments/assets/9a98c336-46e4-4a3a-ad10-5386b7d2a715)
![Image](https://github.com/user-attachments/assets/6ecde4fd-2d70-4459-b839-022231538fd1)

---

## Deskripsi Proyek

Proyek ini adalah aplikasi dasar **CRUD (Create, Read, Update, Delete) Data Pengguna** yang dikembangkan menggunakan **Node.js** sebagai *backend*, **Express.js** sebagai *web framework*, dan **Multer** untuk fungsionalitas *upload* foto. Aplikasi ini juga dilengkapi dengan integrasi *front-end* sederhana untuk berinteraksi dengan *endpoint* API yang telah dibuat.

Proyek ini merupakan bagian dari tugas mata kuliah **Web Pemrograman** yang diampu oleh **Bu Andita Pertama S.Kom., M.Kom.**, dengan referensi dari modul-modul berikut:
* [Modul 1: CRUD Basic untuk Mengelola Data Pengguna Menggunakan Node.js](https://medium.com/@anditaurban/crud-basic-untuk-mengelola-data-pengguna-menggunakan-node-js-418353df5f59)
* [Modul 2: Integrasi Front-end Sederhana untuk Berinteraksi dengan CRUD Data Pengguna](https://medium.com/@anditaurban/integrasi-front-end-sederhana-untuk-berinteraksi-dengan-crud-data-pengguna-dengan-endpoint-api-node-6d68db19d3c5)
* [Modul 3: Integrasi Multer (Upload Foto) dalam Aplikasi CRUD Node.js](https://medium.com/@anditaurban/integrasi-multer-upload-foto-dalam-aplikasi-crud-node-js-4a3b8475007e)

## Fitur Utama

* **Tambah Pengguna (Create):** Menambahkan data pengguna baru ke database.
* **Lihat Daftar Pengguna (Read):** Menampilkan semua data pengguna yang tersimpan.
* **Perbarui Data Pengguna (Update):** Mengubah informasi data pengguna yang sudah ada.
* **Hapus Pengguna (Delete):** Menghapus data pengguna dari database.
* **Upload Foto Pengguna:** Mengunggah dan menyimpan foto profil untuk setiap pengguna menggunakan Multer.
* **API Endpoint:** Menyediakan RESTful API untuk operasi CRUD.
* **Antarmuka Sederhana:** Front-end dasar untuk berinteraksi dengan API.

---

## Teknologi yang Digunakan

* **Backend:** Node.js, Express.js
* **Database:** MySQL
* **Library:** Multer (untuk upload file)
* **Front-end:** HTML, Tailwind CSS dan JavaScript
---

## Instalasi dan Cara Menjalankan Proyek

Ikuti langkah-langkah di bawah ini untuk menginstal dan menjalankan proyek di lingkungan lokal Anda.

### Prerequisites

Pastikan Anda telah menginstal yang berikut ini:
* Node.js ([Disarankan versi LTS](https://nodejs.org/en/download/))
* npm (Node Package Manager, biasanya terinstal bersama Node.js)
* MySQL / MariaDB

### Langkah-langkah Instalasi

1.  **Clone Repositori:**
    ```bash
    git clone https://github.com/ucupdev23/tugas-web-1.git
    ```
2.  **Masuk ke Direktori Proyek:**
    ```bash
    cd crud-auth
    ```
3.  **Instal Dependensi Backend:**
    Masuk ke folder crud-auth/back-end.
    ```bash
    npm install
    ```
    *(Ini akan menginstal semua package yang terdaftar di `package.json` seperti Express, Multer, dll.)*

4.  **Konfigurasi Database:**
    * Pastikan server MySQL Anda berjalan.
    * Buka file konfigurasi database Anda (`config/db.js`).
    * Sesuaikan `database: "crud_auth"` dengan nama database anad (contoh: `database: "latihan-crud"`).

5.  **Jalankan Server Backend:**
    ```bash
    node app.js
    ```
    Server akan berjalan di `http://localhost:3000`.

6.  **Akses Aplikasi Front-end:**
    * Setelah server *backend* berjalan, masuk ke folder frond-end kemudian buka file `index.html` di *browser* Anda.
    * Aplikasi *front-end* akan berkomunikasi dengan *backend* yang sedang berjalan.

---

## Struktur Direktori

Berikut adalah struktur direktori back-end dari proyek ini:

-   `back-end`
    -   `config/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
        -   `db.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Konfigurasi koneksi database
    -   `controllers/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
        -   `userController.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;    # Logika bisnis untuk operasi CRUD pengguna
    -   `middlewar/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
        -   `authMiddleware.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;    # Middleware untuk autentikasi
        -   `uploadMiddleware.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Middleware untuk upload file (Multer)
    -   `models/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
        -   `userModel.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Definisi skema data pengguna
    -   `public/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Folder untuk file-file front-end yang disajikan secara statis
        -   `uploads/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Folder untuk menyimpan foto yang diunggah
            -  `nama_file_foto.jpg` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Contoh file foto yang diunggah
    -   `routes/` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
        -   `userRoutes.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # Definisi rute API untuk pengguna
    -   `gitignore` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # File untuk mengabaikan file/folder tertentu dari Git
    -   `app.js` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # File utama aplikasi / entry point server (`app.js`)
    -   `package.json` &nbsp; &nbsp; &nbsp; &nbsp; # Daftar dependensi dan script proyek
    -   `README.md` &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; # File README ini

---

## Kontribusi

Proyek ini adalah tugas perkuliahan. Jika Anda memiliki saran atau menemukan *bug*, silakan buka *issue* atau *pull request*.

---

## Kontak

Jika Anda memiliki pertanyaan lebih lanjut, Anda bisa menghubungi saya:

* **Nama:** Yusuf Abdilhaq
* **Email:** ucup.dev23@gmail.com
* **LinkedIn:** https://www.linkedin.com/in/yusuf-abdilhaq/

---

**Terima kasih telah mengunjungi repositori ini!**
