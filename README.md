# Tugas Praktikum 4 Desain Pemrograman Berorientasi Objek 2025
Saya Zaki Adam dengan NIM 2304934 mengerjakan Tugas Praktikum 4 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk Keberkahan-Nya maka saya tidak akan melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Desain Program
Aplikasi ini merupakan interface dengan Java Swing GUI untuk mengelola data mahasiswa yang meliputi NIM, nama, kelamin, dan status keaktifan. Aplikasi ini berkemampuan untuk menambah, memperbarui, dan menghapus data-data mahasiswa.

### Mahasiswa.java
Merupakan class untuk data mahasiswa yang terdiri dari atribut `nim`, `nama`, `jenis kelamin`, `status mahasiswa`. Class ini memiliki getter dan setter untuk masing-masing atribut dalam class tersebut.

### Menu.java
Merupakan class graphics user interface untuk program ini. Class ini juga dapat `Add`, `Update`, dan `Delete` data yang ada.

## Penjelasan Alur
### 1. Inisialisasi
Membuat window dari aplikasi, lalu juga memasukkan data secara statis ke dalam program. Tampilan program akan menyajikan Formulir data, Tombol Add/Update, Tombol Delete, Tombol Cancel, dan List data mahasiswa.

### 2. Add
Memasukkan NIM dan Nama, lalu memilih jenis kelamin yang tersedia, selanjutnya memilih status mahasiswa. Setelah itu menekan tombol Add untuk menambahkan data baru ke dalam program.

### 3. Update
Memilih data terlebih dahulu. Opsi Add sebelumnya berubah menjadi Update. Formulir Data terisi dengan atribut data yang diakses. Memodifikasi setiap atribut yaitu NIM, Nama, Jenis Kelamin, dan Status Mahasiswa. Setelah menekan tombol Update untuk memperbarui.

### 4. Delete
Memilih data terlebih dahulu. Opsi Delete akan muncul. Formulir Data terisi dengan atribut data yang diakses. Menekan tombol Delete, akan memunculkan pop up untuk konfirmasi penghapusan data. Tekan Yes untuk menghapus data.

### 5. Clear
Setelah melakukan salah satu perintah di atas (`Add`, `Update`, ataupun `Delete`). Formulir akan dibersihkan datanya sehingga tidak ada satu pun nilai yang mengisi kolom formulir tersebut.
## Dokumentasi
