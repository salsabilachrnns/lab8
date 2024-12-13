# Deskripsi Program Daftar Nilai Mahasiswa

Program ini adalah implementasi sederhana dari pengelolaan data mahasiswa menggunakan konsep pemrograman berorientasi objek (OOP) dalam Python. Program terdiri dari beberapa kelas yang saling berinteraksi untuk menangani data mahasiswa secara efektif. Berikut adalah penjelasan detail dari setiap bagian program.

## 1. Kelas `Person`

### Deskripsi
Kelas `Person` berfungsi sebagai dasar untuk mendefinisikan atribut dan metode yang umum untuk semua orang, termasuk mahasiswa. Kelas ini memiliki atribut private dan menggunakan property untuk mengelola akses ke atribut tersebut.

### Atribut
- `__nama`: Atribut private yang menyimpan nama.
- `__umur`: Atribut private yang menyimpan umur.

### Metode
- `__init__(self, nama)`: Konstruktor yang menginisialisasi nama dan umur.
- `umur`: Property untuk mendapatkan dan mengatur nilai umur.
    - **Getter**: Mengembalikan nilai umur.
    - **Setter**: Mengatur nilai umur, dengan validasi agar tidak negatif.
- `tampilkan_nama()`: Mengembalikan nama.

## 2. Kelas `Mahasiswa`

### Deskripsi
Kelas `Mahasiswa` merupakan subclass dari `Person` yang menambahkan atribut dan metode khusus untuk mahasiswa. Kelas ini memungkinkan pengelolaan data mahasiswa, termasuk NIM dan alamat.

### Atribut
- `nim`: Menyimpan nomor induk mahasiswa.
- `alamat`: Menyimpan alamat mahasiswa.

### Metode
- `__init__(self, nim, nama)`: Konstruktor yang menginisialisasi NIM dan nama, serta memanggil konstruktor dari `Person`.
- `set_alamat(self, alamat)`: Menetapkan alamat mahasiswa.
- `tampilkan_data(self)`: Mengembalikan string yang berisi informasi lengkap tentang mahasiswa (NIM, nama, umur, alamat).

## 3. Kelas `DaftarNilaiMahasiswa`

### Deskripsi
Kelas ini bertanggung jawab untuk mengelola daftar mahasiswa, termasuk operasi untuk menambah, menampilkan, menghapus, dan mengubah data mahasiswa.

### Atribut
- `data_mahasiswa`: Dictionary yang menyimpan objek mahasiswa dengan NIM sebagai kunci.

### Metode
- `__init__(self)`: Konstruktor untuk menginisialisasi dictionary.
- `tambah(self, mahasiswa)`: Menambahkan objek mahasiswa ke dalam `data_mahasiswa`. Memeriksa apakah NIM sudah ada.
- `tampilkan(self)`: Menampilkan semua data mahasiswa yang tersimpan.
- `hapus(self, nim)`: Menghapus data mahasiswa berdasarkan NIM.
- `ubah(self, nim, umur_baru)`: Mengubah umur mahasiswa berdasarkan NIM.

## 4. Contoh Penggunaan

Di bagian ini, program membuat beberapa instansi dari kelas `Mahasiswa` dan menambahkannya ke dalam kelas `DaftarNilaiMahasiswa`. Berikut adalah langkah-langkah yang dilakukan:

1. **Membuat Instansi Mahasiswa**: 
   - Lima mahasiswa dengan nama dan NIM yang berbeda dibuat, dan umur serta alamat diatur menggunakan setter.

2. **Menambahkan Mahasiswa ke Daftar**: 
   - Setiap objek mahasiswa ditambahkan ke dalam daftar menggunakan metode `tambah`.

3. **Menampilkan Data Mahasiswa**: 
   - Metode `tampilkan` digunakan untuk menampilkan semua data mahasiswa.

4. **Mengubah Data Mahasiswa**: 
   - Umur salah satu mahasiswa diubah dan ditampilkan kembali.

5. **Menghapus Data Mahasiswa**: 
   - Data mahasiswa dihapus berdasarkan NIM dan daftar ditampilkan lagi untuk memverifikasi penghapusan.

## Kesimpulan

Program ini menunjukkan bagaimana menggunakan OOP untuk mengelola data secara terstruktur. Menggunakan kelas dan objek memungkinkan pemisahan tanggung jawab dan memudahkan pengelolaan data mahasiswa, serta memberikan fleksibilitas dalam menambah fitur di masa mendatang. Program ini dapat diperluas dengan menambahkan fitur lain seperti penyimpanan ke file atau pengolahan data lebih lanjut.
