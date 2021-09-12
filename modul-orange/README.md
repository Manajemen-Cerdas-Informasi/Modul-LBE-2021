# Modul Orange

## Apa itu Orange?
Orange merupakan aplikasi yang dikembangkan oleh University of Ljubljana, dengan target menghadirkan sebuah aplikasi untuk mengolah data secara visual tanpa perlu pengalaman membuat program sebelumnya. Fitur Orange adalah pemrograman visual untuk analisis data secara eksploratif dan visualisasi data yang interaktif.

Pada Orange, komponen dasarnya adalah widget. Setiap widget punya fungsinya masing-masing dan dapat menerima input atau mengeluarkan output. Misalnya kita ingin membaca data dari sebuah file, kita bisa menggunakan widget File untuk membaca data dari file tersebut dan menggunakan widget Data Table untuk menampilkan isi data yang sudah dibaca.

## Fitur
Orange berisi antarmuka kanvas di mana pengguna dapat meletakkan widget dan membuat workflow analisis data.
Secara umum bagian meja kerja Orange meliputi:

![image](https://user-images.githubusercontent.com/68369091/132945729-cb50db53-d938-48ee-bb8c-4b0b94e891be.png)

- Canvas: grafik frond-end sebagai tempat workflow analisis data
- Workflow : kumpulan dari widget

Widget memiliki beberapa kelompok, yaitu:
- Data: widget untuk input data, filter data, sampling, imputasi dan seleksi fitur
- Visualize: widget untuk visualisasi secara umum (box plot, histograms, scatter plot) dan visualisasi data multivariat (mosaic display, sieve diagram)
- Model: serangkaian widget dari pembelajaran mesin supervised untuk klasifikasi dan regresi
- Evaluate: widget untuk mengukur performa model yang terdiri dari cross-validation, sampling-based procedures, dan reliability estimation
- Unsupervised: widget untuk pembelajaran mesin unsupervised yang terdiri dari algoritma klustering (hierarkikal dan K-Means) dan teknik proyeksi data (multidimensional scaling / MDS, principal component analysis / PCA, correspondence analysis)

Jika ini masih kurang, kalian bisa menambah add-ons pada Orange kalian, seperti add-on bio-informatics, add-on edukasi, dll.


## Penggunaan Widget, Channel, Workflow, dan Data

### Widget
Seperti yang sudah dibahas, widget adalah unit komputasional dari Orange. Widget memiliki beberapa fungsi, seperti membaca data, memproses data, visualisasi data, melakukan klustering, membangun model prediksi, dan banyak lagi. 

![image](https://user-images.githubusercontent.com/68369091/132955292-87f729fc-877a-4c09-9a7b-cdf360df07a9.png)

Widget biasanya terdapat di bagian kiri screen, dan ada beberapa cara kalian bisa menambahkan widget ke dalam _canvas_:
- Mengklik langsung widget dan widget akan ditambahkan ke dalam _canvas_
- Mengklik dan drag untuk menaruh widget ke tempat yang diinginkan
- Mengklik kanan di _canvasnya_ langsung
- Tarik output dari widget lain ke ruang lain di _canvas_ dan akan ditunjukkan list yang menunjukkan widget yang dapat menerima data dari widget yang tadi ditarik, dan tinggal memilih langsung.


### Channel
Channel atau _communication channel_ adalah saluran di mana data akan disalurkan antar widget sebagai sarana widget saling berkomunikasi. Bisa diibaratkan sebagai mesin yang meng-outputkan sebuah data ke input mesin lain.

![image](https://user-images.githubusercontent.com/68369091/132955480-ea5f04a1-9d84-43d0-bc31-207cf081d692.png)

Kebanyakan widget memiliki input di mana data bisa dimasukkan, dan output di mana data bisa dikeluarkan setelah di-proses widget tersebut, dan mereka disebut _input output channel widget_. Ada beberapa widget yang tidak memiliki input, seperti widget _file_, yang dinamai _output channel widget_. Ada juga widget yang tidak memiliki output, seperti widget _save data_, yang dinamai _input channel widget_. 

![image](https://user-images.githubusercontent.com/68369091/132955576-3979456f-18ad-4951-b936-14dfea9bbacf.png)

Channel dibuat dengan menarik line-border yang terdapat di kiri atau kanan widget asal dan menghubungkannya dengan line-border widget yang dituju. Perubahan dari satu widget akan diteruskan ke widget lain melalui channel secara otomatis. Di dalam channel terdapat satu atau lebih link yang dapat diatur sesuai kebutuhan kita. Untuk menghapus channel widget dari canvas, kita dapat meng-klik kanan channel dan memencet `Remove`.

### Workflow
Data Workflow adalah kumpulan widget dan channel yang dirangkai sedemikian rupa untuk melakukan suatu pekerjaan. AAda beberapa contoh data workflow di website Orange. Kalian juga bisa membuat data workflow sendiri sesuai kebutuhan analisis data kalian.

Contoh sederhana data workflow dalam visualisasi data, seperti berikut:

1. Masukkan widget **File** dan widget **Data Table** ke dalam canvas.
2. Buatlah channel antara **File** ke input widget **Data Table**

![1_gIvnErCh2NUjFX6laq3ldA](https://user-images.githubusercontent.com/68369091/132955916-fd7369fa-4619-45c1-890c-69f41dfcbe40.gif)

Di kanvas, klik dua kali pada widget File untuk membukanya. Kemudian, Anda dapat memuat dataset Anda sendiri atau menelusuri dataset kustom dari Orange. Mari kita coba dengan iris.tab melalui datasetnya Orange. Orange dapat menerima format file berikut:
- Tab-separated value (*.tab, *.tsv) file
- Comma-separated value (*.csv) file
- Microsoft Excel/Google Sheet spreadsheet (*.xls, *.xlsx)
- Python pickle

Selain itu, file berbasis teks (CSV, TSV) dapat dikompresi dengan gzip, bzip2 atau xz (misal *.csv.gz).

Kalian akan ditunjukkan screen ini setelah meng-klik widget **File**.

![image](https://user-images.githubusercontent.com/68369091/132956183-c3bdd9c4-1dfc-42ba-84b0-af56a5172d30.png)

Selanjutnya, klik dua kali pada widget **Data Table**. Kalian sekarang harusnya dapat melihat kumpulan data. Anda dapat memencet tombol **Visualize Numeric Values** di sisi kiri untuk memvisualisasikan angka dengan mudah. Anda seharusnya dapat melihat layar berikut setelah Anda memeriksa semua opsi.

![image](https://user-images.githubusercontent.com/68369091/132956258-4baaea9c-1fb6-4373-92b6-c9231902631a.png)

Anda dapat memvisualisasikan data dengan mudah melalui beberapa widget **Visualition**. Distribusi adalah salah satu widget terbaik untuk mengidentifikasi fitur penting untuk dataset. Anda dapat dengan mudah memvisualisasikan apakah dataset dipisahkan dengan baik atau tidak. Mari kita lanjutkan dari langkah sebelumnya.

![1_TPnvjJRut-fC9ehimJqXAQ](https://user-images.githubusercontent.com/68369091/132956308-3ad020bb-a388-4b13-83e1-77028f3a1aa3.gif)

1. Seret widget **Distribusi** ke kanvas.
2. Hubungkan widget **File** ke widget **Distribusi**.
3. Klik dua kali pada widget Distribusi untuk melihat visualisasi.
4. Di kiri atas, pilih variabel yang berbeda dan periksa hasil distribusi.

![image](https://user-images.githubusercontent.com/68369091/132956363-9e2934fd-ba14-4c39-b0f6-0f1bd128fe17.png)

### Load Data Sendiri

Nah, kita kan sudah memakai dataset dari Orange, bagaimana kalau kita ingin memakai dataset kita sendiri? Kita sudah mengetahui format file yang diterima oleh Orange, mari kita buat baru!

1. Pertama, buatlah sebuah spreadsheet dengan data yang diinginkan.

![image](https://user-images.githubusercontent.com/68369091/132974605-a05e8bdb-0d48-4286-b2b3-5f46a036b812.png)

2. Lalu, masukkan widget **File** dan **Data Table** seperti biasa, dan hubungkanlah.

![image](https://user-images.githubusercontent.com/68369091/132974635-7b65fb41-ddd8-42c8-ba27-0b92847e2ad3.png)

3. Klik widget **File** dua kali, dan masukkan link Google Sheets kalian ke kolom URL (jika kalian menggunakan Google Sheets) atau buka file dari komputer jika membuatnya di komputer kalian dengan meng-klik gambar folder.

![image](https://user-images.githubusercontent.com/68369091/132976215-3692914d-afa1-4a09-8de5-4b3098d84588.png)

Di sini, kita bisa lihat sekilas mengenai data kita. Bisa terlihat bahwa ada 5 baris data, 7 fitur/kolom tanpa nilai kosong, 1 atribut meta dan data tidak memiliki target kelas. Kolom type menyatakan tipe data apa, sedangkan role menyatakan data kolom tersebut digunakan sebagai apa didalam dataset.

| Role | Informasi |
| --- | --- |
| c: class attribute | Atribut label kelas |
| m: meta attribute | Atribut meta data (indeks) |
| i: ignore | Atribut kolom yang diabaikan |
| w: instance weights | Atribut kolom bobot |

| Tipe | Informasi |
| --- | --- |
| C (Continuous) | tipe data kategorical dimana data tidak dapat diurutkan (tidak bertingkat) |
| D (Discrete) | tipe data numerik (kontinyu atau diskrit) dimana data dapat diurutkan (bertingkat) |
| T (Time) | tipe data waktu |
| S (String) | tipe data berupa teks |


4. Bukalah widget **Data Table** dan keluarlah isi dataset kalian! Sekarang kalian bisa menggunakannya seperti biasa.

![image](https://user-images.githubusercontent.com/68369091/132976449-2a84e0a8-12b2-4954-b331-a4a94a740c00.png)



## Referensi
- https://orange3.readthedocs.io/projects/orange-visual-programming/en/latest/loading-your-data/index.html
- https://towardsdatascience.com/data-science-made-easy-interactive-data-visualization-using-orange-de8d5f6b7f2b
- https://github.com/ranggakd/Orange_Tutorial
- https://docs.biolab.si/orange/2/data/rst/index.html
