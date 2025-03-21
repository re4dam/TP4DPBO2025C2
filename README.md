# Tugas Praktikum 4 Desain Pemrograman Berorientasi Objek 2025
Saya Zaki Adam dengan NIM 2304934 mengerjakan Tugas Praktikum 4 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk Keberkahan-Nya maka saya tidak akan melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Desain Program
## Penjelasan Alur
## Dokumentasi

# Desain dan Alur Kerja Aplikasi Manajemen Mahasiswa

## Gambaran Umum Program
Aplikasi Java ini adalah Sistem Manajemen Mahasiswa yang dibangun dengan Swing. Program ini menyediakan antarmuka pengguna grafis untuk melihat dan mengelola data mahasiswa, meliputi:
- Menampilkan mahasiswa dalam tabel
- Menambahkan mahasiswa baru
- Memperbarui informasi mahasiswa yang sudah ada
- Menghapus mahasiswa dari database

## Struktur Kelas

### Kelas Utama: `Menu`
Kelas `Menu` merupakan turunan dari `JFrame` dan berfungsi sebagai jendela utama aplikasi.

### Model Data: `Mahasiswa`
Meskipun tidak ditunjukkan dalam kode yang diberikan, aplikasi ini bergantung pada kelas `Mahasiswa` yang kemungkinan berisi:
- `nim` (Nomor Induk Mahasiswa)
- `nama` (Nama Mahasiswa)
- `jenisKelamin` (Jenis Kelamin)
- `statusMahasiswa` (Status Mahasiswa: Aktif atau Cuti)

## Komponen GUI

### Jendela Utama
- Ukuran: 480×560 piksel
- Latar belakang: Putih
- Diposisikan di tengah layar

### Elemen Formulir
1. **Label Judul**: Menampilkan judul aplikasi dalam huruf tebal, font 20pt
2. **Kolom Input**:
   - `nimField`: Kolom teks untuk NIM
   - `namaField`: Kolom teks untuk Nama Mahasiswa
   - `jenisKelaminComboBox`: Dropdown untuk pemilihan Jenis Kelamin ("Laki-laki" atau "Perempuan")
   - Tombol radio untuk Status:
     - `aktifRadioButton`: Untuk status "Aktif"
     - `cutiRadioButton`: Untuk status "Cuti" (dikelompokkan dengan `aktifRadioButton`)

3. **Tombol**:
   - `addUpdateButton`: Tombol multi-fungsi untuk operasi Tambah/Perbarui
   - `deleteButton`: Untuk menghapus data yang dipilih (disembunyikan secara default)
   - `cancelButton`: Untuk membersihkan formulir

4. **Tabel**:
   - `mahasiswaTable`: Menampilkan data mahasiswa dengan kolom:
     - No. (Nomor baris)
     - NIM (Nomor Induk Mahasiswa)
     - Nama
     - Jenis Kelamin
     - Status (Aktif/Cuti)

## Alur Kerja Aplikasi

### 1. Inisialisasi
1. Aplikasi membuat jendela `Menu` baru
2. Jendela diatur ukurannya, diposisikan, dan ditampilkan
3. ArrayList `listMahasiswa` diinisialisasi
4. Data mahasiswa contoh dimuat melalui `populateList()`
5. Tabel diisi dengan data mahasiswa
6. Elemen formulir diinisialisasi (nilai combo box, grup tombol radio)

### 2. Menambahkan Mahasiswa
1. Pengguna memasukkan informasi mahasiswa di kolom formulir
2. Pengguna mengklik tombol "Add"
3. Metode `insertData()` dipanggil, yang:
   - Mengambil nilai dari kolom formulir
   - Membuat objek `Mahasiswa` baru
   - Menambahkan objek ke `listMahasiswa`
   - Memperbarui tampilan tabel
   - Menampilkan pesan sukses
   - Membersihkan formulir

### 3. Memperbarui Data Mahasiswa
1. Pengguna mengklik sebuah baris dalam tabel
2. Penangan kejadian `mousePressed`:
   - Mencatat indeks baris yang dipilih
   - Mengisi kolom formulir dengan data dari mahasiswa yang dipilih
   - Mengubah tombol "Add" menjadi "Update"
   - Menampilkan tombol "Delete"
3. Pengguna memodifikasi data di kolom formulir
4. Pengguna mengklik tombol "Update"
5. Metode `updateData()` dipanggil, yang:
   - Mengambil nilai dari kolom formulir
   - Memperbarui objek `Mahasiswa` yang sesuai dalam `listMahasiswa`
   - Memperbarui tampilan tabel
   - Menampilkan pesan sukses
   - Membersihkan formulir

### 4. Menghapus Mahasiswa
1. Pengguna mengklik sebuah baris dalam tabel (sama seperti langkah 1 dalam pembaruan)
2. Pengguna mengklik tombol "Delete"
3. Dialog konfirmasi muncul
4. Jika dikonfirmasi, metode `deleteData()` dipanggil, yang:
   - Menghapus objek `Mahasiswa` yang dipilih dari `listMahasiswa`
   - Memperbarui tampilan tabel
   - Menampilkan pesan sukses
   - Membersihkan formulir

### 5. Membatalkan Operasi
1. Pengguna mengklik tombol "Cancel"
2. Metode `clearForm()` dipanggil, yang:
   - Membersihkan semua kolom formulir
   - Mengatur ulang teks tombol Add/Update
   - Menyembunyikan tombol Delete
   - Menghapus status pemilihan

## Aliran Data

1. **Penyimpanan Data**: Semua data mahasiswa disimpan dalam ArrayList `listMahasiswa`.
2. **Tampilan Tabel**: Metode `setTable()` menghasilkan `DefaultTableModel` dari data ArrayList.
3. **Validasi Data**: Tidak ada validasi eksplisit yang diterapkan dalam kode yang disediakan.

## Detail Implementasi Teknis

### Pengelolaan Model Tabel
- Metode `setTable()` membuat model tabel baru setiap kali dipanggil
- Kolom tabel: No, NIM, Nama, Jenis Kelamin, Status

### Penanganan Kejadian
- Kejadian klik tombol dikelola melalui implementasi `ActionListener`
- Pemilihan baris tabel ditangani melalui implementasi `MouseAdapter`

### Manajemen Status UI
- Variabel `selectedIndex` melacak baris mana yang sedang dipilih
- Keadaan dan visibilitas tombol berubah berdasarkan apakah sebuah baris dipilih
- Kolom formulir dibersihkan setelah setiap operasi
