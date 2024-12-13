# SALSABILA CHAIRUNISSA - NIM : 352310473
# PROGRAM SEDERHANA PENGGUNAAN CLASS


Program ini adalah implementasi sederhana dari pengelolaan data mahasiswa menggunakan konsep pemrograman berorientasi objek (OOP) dalam Python. Program terdiri dari beberapa kelas yang saling berinteraksi untuk menangani data mahasiswa secara efektif. Berikut adalah penjelasan detail dan gambar perintah phytonnya : 

![perintah 1](https://github.com/user-attachments/assets/1b3fb66d-15e6-4816-bd24-b19ed1a2e4dc)
![perintah 2](https://github.com/user-attachments/assets/a5944706-bcac-4449-92aa-588af85001a1)
![perintah 3](https://github.com/user-attachments/assets/694e20c1-1629-444c-93d5-eb8b1c368f3a)
![perintah 4](https://github.com/user-attachments/assets/56276f51-9085-4daf-b876-7d522d8b21fd)
![perintah 5](https://github.com/user-attachments/assets/5a29b561-b262-4429-a1ab-bdd876e4e5ed)



## Deskripsi Perintah Program :
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
  
## 5. Hasil Output Run (F5) :

![output](https://github.com/user-attachments/assets/3a90257e-091c-4473-a8fe-6a2aac3a025a)

## 6. Diagram class : 

![diagram kelas (mind mapping)](https://github.com/user-attachments/assets/b23098cb-e3e0-4369-bc71-f9863c28ebba)

## 7. Flowchart perintah program : 

![flowchart](https://github.com/user-attachments/assets/8cde3942-153b-454e-844e-4d2e30469faf)

## Kesimpulan

Program ini menunjukkan bagaimana menggunakan OOP untuk mengelola data secara terstruktur. Menggunakan kelas dan objek memungkinkan pemisahan tanggung jawab dan memudahkan pengelolaan data mahasiswa, serta memberikan fleksibilitas dalam menambah fitur di masa mendatang. Program ini dapat diperluas dengan menambahkan fitur lain seperti penyimpanan ke file atau pengolahan data lebih lanjut.
