# Modul 1 LBE MCI 2021: Database & SQL

- [Database](#database)
  - [Konsep](#konsep-database)
  - [Istilah](#istilah-database)
  - [Key](#key-database)
  - [Database Management System (DBMS)](#dbms-database)
- [SQL](#sql)
  - [Install XAMPP](#installxampp-sql)
  - [Run XAMPP](#runxampp-sql)
  - [Tentang](#tentang-sql)
  - [Data Definition Language (DDL)](#ddl-sql)
    - [DDL Database](#ddl-database)
    - [DDL Tabel](#ddl-tabel)
  - [Data Manipulation Language (DML)](#dml-sql)
  - [Latihan](#latihan-sql)
- [Referensi](#referensi)

# <a name="database"></a>1. Database

## <a name="konsep-database"></a>Konsep Database

### Apa itu database?

<b>Database</b> atau <b>basis data</b> adalah kumpulan data yang dikelola sedemikian rupa berdasarkan ketentuan tertentu yang saling berhubungan sehingga mudah dalam pengelolaannya. Melalui pengelolaan tersebut pengguna dapat memperoleh kemudahan dalam mencari informasi, menyimpan informasi, dan membuang informasi. Perangkat lunak yang digunakan untuk mengelola dan memanggil kueri (<i>query</i>) basis data tersebut disebut dengan sistem manajemen basis data (<i>Database Management System</i>/<b>DBMS</b>).

### <a name="istilah-database"></a>Istilah pada database

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

### <a name="key-database"></a>Key pada database

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

### <a name="dbms-database"></a>Database Management System (DBMS)

<b><i>Database Management System</i></b> (DBMS) adalah suatu sistem atau perangkat lunak yang dirancang untuk mengelola suatu basis data dan menjalankan operasi terhadap data yang diminta banyak pengguna.

<b>Contoh DBMS</b>:
- Oracle
- MySQL
- Microsoft Access
- PostgreSQL
- Microsoft SQL Server

# <a name="sql"></a>2. SQL

### <a name="installxampp-sql"></a>Install XAMPP

Pada LBE kali ini, kita akan menggunakan DBMS MySQL dengan menggunakan aplikasi XAMPP yang bisa diunduh [di sini](https://www.apachefriends.org/download.html "di sini"). Cara instalasinya:

- [Windows](https://www.youtube.com/watch?v=N43oVPkrTg8 "Windows")
- [Mac](https://www.youtube.com/watch?v=EK_AUTzV7OI "Mac")
- [Linux (Ubuntu)](https://www.youtube.com/watch?v=R5CUn5wGQGg "Linux (Ubuntu)")

### <a name="runxampp-sql"></a>Cara Run XAMPP

- Buka XAMPP Control Panel
- Klik Start pada modul Apache dan MySQL
- Klik Admin pada modul MySQL

<img src="https://user-images.githubusercontent.com/37539546/131892134-7cd1f759-5e92-4e84-a47c-6a0321a7457f.JPG" width="668" height="434.67">

## <a name="tentang-sql"></a>Tentang SQL

### Apa itu SQL?

SQL (<i>Structured Query Language</i>) adalah sebuah bahasa yang digunakan untuk mengakses data dalam basis data relasional. SQL dapat digunakan untuk mendefinisikan struktur data, pengubahan data, memanipulasi/memperoleh data, pengaturan sekuritas, dan lain lain.

## <a name="ddl-sql"></a>Data Definition Language (DDL)

DDL digunakan untuk mendefinisikan, mengubah, serta menghapus database dan objek-objek yang diperlukan dalam database. Dalam implementasinya, DDL digunakan untuk membuat dan memanipulasi tabel maupun <i>view</i>. Terdapat dua macam DDL, yaitu:

### <a name="ddl-database"></a>DDL untuk database

1. <b>CREATE DATABASE</b> untuk membuat database.
  
   ```MySQL
   CREATE DATABASE mahasiswa;                                     /* Membuat database 'mahasiswa' */
   ```
     
2. <b>DROP DATABASE</b> untuk menghapus database.
  
   ```MySQL
   DROP DATABASE mahasiswa;                                       /* Menghapus database 'mahasiswa' */
   ```
   
### <a name="ddl-tabel"></a>DDL untuk tabel

1. <b>CREATE TABLE</b> untuk membuat tabel baru pada database.
  
   ```MySQL
   CREATE TABLE Mahasiswa (                                       /* Membuat tabel 'mahasiswa' dengan 4 atribut */
      NRP VARCHAR(16) NOT NULL,                                   /* NRP tidak NULL */
      Nama VARCHAR(50) NOT NULL,                                  /* Nama tidak NULL */
      Usia INT,
      Semester INT,
      PRIMARY KEY(NRP)                                            /* NRP adalah primary key */
   );
   ```
     
2. <b>ALTER TABLE</b> untuk memodifikasi atribut pada tabel yang sudah ada (menambah, mengubah, menghapus).
   
   <b>ADD</b>
   
   ```MySQL
   ALTER TABLE Mahasiswa
   ADD Tanggal_Lahir date;                                        /* Menambah atribut baru 'Tanggal_Lahir' */
   ```
   
   <b>DROP COLUMN</b>
   
   ```MySQL
   ALTER TABLE Mahasiswa
   DROP COLUMN Usia;                                              /* Menghapus atribut 'Usia' */
   ```
   
   <b>MODIFY COLUMN</b>
   
   ```MySQL
   ALTER TABLE Mahasiswa
   MODIFY COLUMN NRP VARCHAR(14);                                 /* Mengubah tipe data atribut NRP menjadi VARCHAR(14) */
   ```

3. <b>RENAME TABLE</b> untuk mengganti nama tabel pada database.
    
   ```MySQL
   RENAME TABLE Mahasiswa TO Mhs;                                 /* Mengganti nama tabel 'Mahasiswa' menjadi 'Mhs' */
   ```

4. <b>DROP TABLE</b> untuk menghapus tabel pada database.
    
   ```MySQL
   DROP TABLE Mhs;                                                /* Menghapus tabel 'Mhs' */
   ```

## <a name="dml-sql"></a>Data Manipulation Language (DML)

DML digunakan untuk memanipulasi data yang ada dalam suatu tabel. Beberapa kuerinya antara lain:

1. <b>INSERT</b> untuk memasukkan <i>record</i> baru pada tabel.
  
   ```MySQL
   INSERT INTO Mahasiswa(NRP, Nama, Usia, Semester)               /* Menambah record baru ke tabel */
   VALUES('05111940000062', 'James', 20, 3);
   ```

2. <b>DELETE</b> untuk menghapus <i>record</i> pada tabel.
  
   ```MySQL
   DELETE FROM Mahasiswa WHERE Nama = 'James';                    /* Menghapus record yang atribut Nama-nya 'James' */
   ```

3. <b>UPDATE</b> untuk memperbarui/mengubah <i>record</i> yang sudah ada pada tabel.
  
   ```MySQL
   UPDATE Mahasiswa                                               /* Mengubah record yang atribut Semester-nya '4' menjadi '3' */
   SET Semester = 4
   WHERE Semester = 3;
   ```

4. <b>SELECT</b> untuk menampilkan/mengambil data dari database. Dapat menggunakan `DISTINCT` jika ingin menampilkan data tunggal (tidak dobel/kembar) ataupun `*` jika ingin menampilkan semua atribut dari suatu tabel.
  
   ```MySQL
   SELECT NRP, Nama                                               /* Menampilkan data NRP dan Nama dari tabel 'Mahasiswa' */
   FROM Mahasiswa;
   ```
   
5. <b>WHERE</b> untuk filter suatu <i>record</i>.

   ```MySQL
   SELECT Nama                                                    /* Menampilkan data Nama dengan Usia '20' */
   FROM Mahasiswa
   WHERE Usia = 20;
   ```
   
6. <b>BETWEEN</b> untuk operator rentang nilai.

   ```MySQL
   SELECT Nama                                                    /* Menampilkan data Nama dengan Usia '17-20' */
   FROM Mahasiswa
   WHERE Usia BETWEEN 17 AND 20;
   ```

6. <b>ORDER BY</b> untuk menampilkan <i>record</i> secara <i>ascending</i> (naik) maupun <i>descending</i> (turun).

   ```MySQL
   SELECT Nama                                                    /* Menampilkan data Nama dengan urutan ascending */
   FROM Mahasiswa
   ORDER BY Nama ASC;
   ```

7. <b>MIN</b> dan <b>MAX</b> untuk menampilkan nilai terkecil (minimum) dan nilai terbesar (maksimum).

   ```MySQL
   SELECT MIN(Usia)                                               /* Menampilkan Usia termuda */
   FROM Mahasiswa;
   ```

8. <b>COUNT</b>, <b>AVG</b>, dan <b>SUM</b> sebagai fungsi agregasi. `COUNT()` untuk menghitung jumlah baris yang sesuai dengan kriteria. `AVG()` untuk menghitung rata-rata data kolom yang bertipe data numerik. `SUM()` untuk menghitung total data dalam kolom yang bertipe data numerik.

   ```MySQL
   SELECT AVG(Usia)                                               /* Menampilkan rata-rata Usia */
   FROM Mahasiswa;
   ```
   
9. <b>GROUP BY</b> untuk mengelompokkan baris yang memiliki nilai yang sama. Biasanya digunakan bersamaan dengan fungsi agregasi.
   
   ```MySQL
   SELECT Usia, COUNT(Nama)                                       /* Menampilkan jumlah Nama berdasarkan Usia */
   FROM Mahasiswa;
   GROUP BY Usia;
   ```

## <a name="latihan-sql"></a>Latihan

Sebelum mengerjakan, kalian dapat mengunduh dataset <b>Northwind</b> [di sini](http://downloads.alphasoftware.com/a5v12Download/northwindmysql.zip "di sini"). Setelah itu di-<i>import</i> ke MySQL.

1. Tampilkan daftar nama <i>product</i> dan <i>unit price</i>-nya dari yang paling mahal!
 
2. Hitunglah jumlah <i>product</i> yang saat ini dihentikan produksinya (<i>discontinued</i>)!

3. Tampilkan daftar nama lengkap <i>employee</i> beserta tanggal rekrutnya yang mempunyai jabatan "Sales Representative"!

## <a name="referensi"></a>Referensi

- https://www.dicoding.com/blog/apa-itu-database/
- https://informatika.poltektegal.ac.id/?p=bidang-keilmuan&s=database
- http://www.pengertianku.net/2014/12/pengertian-field-record-table-file-data-dan-basis-data-lengkap.html
- https://www.dumetschool.com/blog/perbedaan-primary-key-foreign-key-dan-candidate-key
- https://www.w3schools.com/sql
- https://www.dewaweb.com/blog/sql-pengertian-fungsi-beserta-perintah-dasarnya/
- https://id.wikipedia.org/wiki/SQL
