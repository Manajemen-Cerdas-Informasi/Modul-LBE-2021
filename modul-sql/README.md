# Modul 1 LBE MCI 2021: Database & SQL

# 1. Database

## Konsep Database

### Apa itu database?

<b>Database</b> atau <b>basis data</b> adalah kumpulan data yang dikelola sedemikian rupa berdasarkan ketentuan tertentu yang saling berhubungan sehingga mudah dalam pengelolaannya. Melalui pengelolaan tersebut pengguna dapat memperoleh kemudahan dalam mencari informasi, menyimpan informasi, dan membuang informasi. Perangkat lunak yang digunakan untuk mengelola dan memanggil kueri (<i>query</i>) basis data tersebut disebut dengan sistem manajemen basis data (<i>Database Management System</i>/<b>DBMS</b>).

### Istilah pada database

- <b>Entitas</b>
  
  Entitas adalah objek yang mewakili sesuatu dalam dunia nyata dan dapat dibedakan antara satu dengan lainnya (<i>unique</i>). Objek dapat berupa barang, orang, tempat atau suatu kejadian. Misalnya, dosen, mahasiswa, sepeda motor, rumah, pegawai, dan lain-lain.
  
- <b>Atribut</b>

  Deskripsi/karakteristik dari suatu entitas, berisi penjelasan detail tentang entitas itu sendiri. Misalnya, entitas mahasiswa mempunyai atribut nama, alamat, NRP, <i>email</i>, dan lain-lain.
  
- <i><b>Field</b></i>

  Tempat atau kolom yang terdapat pada tabel untuk mengisikan salah satu elemen data.
  
- <i><b>Record</b></i>
  
  Kumpulan <i>field</i> yang berhubungan satu sama lain dan biasanya dihitung dalam satu baris.

<b>Gambaran untuk membantu memahami istilah pada database</b>

<img src="https://user-images.githubusercontent.com/37539546/131708987-10383a7c-aa2e-47a1-9685-5b6f90ef8650.jpg" width="598.29" height="208.29">

### Key pada database

<i>Key</i> adalah elemen <i>record</i> yang dipakai untuk menemukan <i>record</i> tersebut pada waktu akses. <i>Key</i> di dalam database berfungsi sebagai suatu cara untuk mengidentifikasi dan menghubungkan suatu tabel data dengan tabel yang lain. Terdapat beberapa jenis <i>key</i>, yaitu:

- <i><b>Primary key</b></i>

  <i>Field</i> yang mengidentifikasi sebuah <i>record</i> dan bersifat unik (tidak sama atau ganda). <i>Field</i> di sini juga tidak boleh <b>null</b>.

  <img src="https://user-images.githubusercontent.com/37539546/131865844-a7843364-56f5-4f5c-bb4e-616aa092741b.jpg" width="374" height="151.25">
  
- <i><b>Secondary key</b></i>

  <i>Field</i> yang mengidentifikasi sebuah <i>record</i> dan tidak bersifat unik. Biasanya digunakan secara kombinasi dan hanya bertujuan untuk mengambil data.
  
  <img src="https://user-images.githubusercontent.com/37539546/131866668-38b49bbf-ed29-4491-90c5-87b7410352d6.jpg" width="418.5" height="153">
  
- <i><b>Foreign key</b></i>

  <i>Field</i> yang bukan key, tetapi <i>key</i> pada tabel lain (tabel induk). Digunakan untuk menghubungkan suatu tabel dengan tabel lainnya.

  <img src="https://user-images.githubusercontent.com/37539546/131866956-b53732e4-02c4-4b58-b795-e43670c8d412.jpg" width="402.25" height="245">
  
- <i><b>Candidate key</b></i>

  <i>Field</i> yang bisa dipilih untuk dijadikan <i>primary key</i>.
  
  <img src="https://user-images.githubusercontent.com/37539546/131868034-2d5f35c0-d964-481b-ae0a-e124f5108d1f.jpg" width="434.75" height="178.75">
  
- <i><b>Composite key</b></i>

  <i>Field</i> yang dibentuk dari beberapa <i>field</i>.

  <img src="https://user-images.githubusercontent.com/37539546/131868087-e603d5a7-ec56-40a1-b47d-271b7694bfed.jpg" width="398" height="166">

### Database Management System (DBMS)

<b><i>Database Management System</i></b> (DBMS) adalah suatu sistem atau perangkat lunak yang dirancang untuk mengelola suatu basis data dan menjalankan operasi terhadap data yang diminta banyak pengguna.

Contoh DMBS:
- Oracle
- MySQL
- Microsoft Access
- PostgreSQL
- Microsoft SQL Server

## Referensi

- https://www.dicoding.com/blog/apa-itu-database/
- https://informatika.poltektegal.ac.id/?p=bidang-keilmuan&s=database
- http://www.pengertianku.net/2014/12/pengertian-field-record-table-file-data-dan-basis-data-lengkap.html
- https://www.dumetschool.com/blog/perbedaan-primary-key-foreign-key-dan-candidate-key
- https://www.w3schools.com/sql
- https://www.dewaweb.com/blog/sql-pengertian-fungsi-beserta-perintah-dasarnya/
