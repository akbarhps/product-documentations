## Laravel Fuzzy C Means

Aplikasi implementasi algoritma fuzzy c means yang dibuat menggunakan PHP Laravel.

<img src="https://drive.google.com/thumbnail?id=1e_qXon6N0EmE0B0cX9kn5eqhYOHILpya&sz=w1000" alt="Image">

---

### Daftar Fitur

- Login dan mendaftarkan akun
- Menambah atau mengubah Kategori
- Import data dari file CSV
- Export data ke file CSV dan Excel
- Tersedia dalam 2 bahasa, bahasa inggris dan bahasa indonesia
- Tersedia dalam 2 mode, light dan dark mode

---

### Aplikasi yang diperlukan untuk menjalankan program

- [XAMPP](https://www.apachefriends.org/)
- [Composer](https://getcomposer.org/)

---

### Cara install dan menjalankan program

- Buka project di terminal/command prompt (cmd)
- Di terminal/cmd, Jalankan perintah `composer install` untuk menginstall dependency

  <img src="https://drive.google.com/thumbnail?id=1vbFMqv6UDAYfcQrtfr7YstlyvJ7KKbaw&sz=w1000" alt="Image">

- Copy file `.env.example` dan rename menjadi `.env`
- Edit file `.env` dengan mengisi konfigurasi berikut:

```text
- APP_NAME="Clustering Fuzzy C Means" (nama website yang akan ditampilkan, gunakan petik 2 jika nama mengandung spasi)
...
- APP_LOCALE=id (jika ingin menggunakan bahasa inggris, isi dengan en, jika bahasa indonesia id)
...
- DB_CONNECTION=mysql (jika menggunakan mysql)
- DB_DATABASE=clustering (nama database myusql yang akan digunakan)
- DB_USERNAME=root (username database, default: root)
- DB_PASSWORD= (password database, default: kosong)
```

- Di terminal/cmd, jalankan perintah `php artisan migrate:fresh --seed` untuk membuat tabel di database

  <img src="https://drive.google.com/thumbnail?id=1lM7BP_Hz32vPR3yUN7Uk_tniC1PNZI2Z&sz=w1000" alt="Image">

- Kemudian, jalankan perintah `php artisan key:generate` untuk mengupdate `APP_KEY` yang digunakan pada session
  aplikasi
- Selanjutnya, jalankan perintah `php artisan optimize` untuk mengoptimalkan jalannya aplikasi

  <img src="https://drive.google.com/thumbnail?id=1_7uAsxtPZ_gIEouj-KH8j3ONpHmSNtqa&sz=w1000" alt="Image">

- Terakhir, jalankan perintah `php artisan serve` untuk menjalankan aplikasi

  <img src="https://drive.google.com/thumbnail?id=1x6sc87zgof1YOwnphmo1Z764qDRsWUKa&sz=w1000" alt="Image">

- Aplikasi berhasil dijalankan, buka browser dan ketikkan `http://localhost:8000`
- Lakukan pendaftaran akun atau login menggunakan akun

```text
email: admin@admin.com   
password: password
```

---

### Cara import data menggunakan CSV

- Buka halaman Kategori, dan tekan tombol Impor Kategori

  <img src="https://drive.google.com/thumbnail?id=1bvbXx1SeMcqYJzD2skNwIHeKr1V-6SWi&sz=w1000" alt="Image">

- Tekan tombol `Unduh contoh berkas CSV`, dan isi data sesuai dengan kolom headernya

  <img src="https://drive.google.com/thumbnail?id=1qH-HBlqBFWh8oehuy3Vf_gW4MI_uCNjP&sz=w1000" alt="Image">

> Catatan: Jangan mengubah atau menghapus kolom header seperti name, description, is_included_in_calculation,
> data_type.  
> **Hanya perlu menambahkan data dibawahnya saja**

- Setelah selesai mengisi data, simpan file CSV tersebut
- Kembali ke halaman Kategori, dan tekan tombol `Unggah berkas CSV`, kemudian pilih file CSV yang sudah diisi tadi.

  <img src="https://drive.google.com/thumbnail?id=1pkVB4tei5MOw-Ck9C3lVADBnj9ZyZ02I&sz=w1000" alt="Image">

- Kemudian tekan tombol Impor, dan data akan masuk ke dalam database

> Dataset (Kumpulan data) hanya bisa di import jika sudah ada kategori yang dibuat.  
> Untuk impor dataset, ulangi langkah diatas.

---

### Cara export data ke CSV dan Excel

> Tombol Export hanya muncul ketika data sudah ada

- Buka halaman Kategori, dan tekan tombol `Ekpor Kategori`

  <img src="https://drive.google.com/thumbnail?id=1XQ6x_K0Y50ErvpJcim4rGoyNOpt3CFBH&sz=w1000" alt="Image">

- Pilih kolom yang ingin kamu export, kemudian tekan tombol `Ekspor`

  <img src="https://drive.google.com/thumbnail?id=1HFvfHa-BcTeCwQEBsY02KeVbRW6y4S1d&sz=w1000" alt="Image">

- Setelahnya akan muncul pop up hasil ekspor, pilih format yang ingin kamu download

  <img src="https://drive.google.com/thumbnail?id=1fZBYLmLoXwY1PPYkGseNz25euF_6uVw3&sz=w1000" alt="Image">

> Ulangi langkah diatas untuk ekspor dataset (Kumpulan data)
