# Modul 2 LBE MCI 2021: Tableau

  - [Tentang Tableau](#tentang-tableau)
  - [Tableau Workspace](#tableau-workspace)
  - [Tableau Navigation](#tableau-navigation)
  - [Praktik Tableau](#praktik-tableau)
  
# <a name="tentang-tableau"></a>Tentang Tableau
Tableau adalah sebuah aplikasi yang dirancang untuk melakukan *Business Intellegent* secara cepat dan melakukan visualisasi data. Aplikasi ini memungkinkan Anda untuk melakukan analisis dari sebuah struktur data dan menghasilkan grafik, dashboard, dan laporan yang sangat interaktif dan indah, hanya dalam hitungan menit. Adapun kelebihan dari tableau yaitu sebagai berikut:
  - Hasil cepat untuk informasi yang bermanfaat.
  - Mudah digunakan untuk semua level skill, karena untuk menggunakannya cukup dengan klik, drag and drop.
  - Jalur migrasi yang sangat baik untuk pengguna Excel.
  - Dapat dengan mudah diintegrasikan dengan berbagai bahasa contohnya R dan Python, serta DBMS seperti MySQL dan Oracle.
  
 Tableau sendiri memiliki beberapa versi, di antaranya:
  - Tableau Desktop
    
    Tableau desktop memiliki banyak sekali fitur yang sudah disediakan, dimana bisa melakukan pengkodean dan meng-custom laporan. Mulai dari membuat bagan, laporan, hingga
    memadukan semuanya bersama untuk membentuk dashboard, semuanya dapat dilakukan hanya dengan menggunakan tableau desktop. Untuk melakukan analisis data secara langsung,
    tableau desktop dapat dihubungkan dengan *data warehouse* secara langsung. Tableau desktop memiliki 2 lisensi yaitu personal dan professional.
  - Tableau Public 
    
    Pada tableau public semua data pekerjaan disimpan di dalam cloud dan dapat dilihat atau diakses oleh siapapun. Tidak ada batasan pada jenis ini. Pada jenis ini juga dapat
    dengan mudah mendownload data pekerjaan orang lain. Merupakan versi yang cocok untuk memulai belajar tableau.
  - Tableau Server
    
    Jenis ini adalah versi yang memungkinkan untuk membagi hasil pengolahan atau *workbooks* kepada orang tertentu. Sangat berguna di dalam sebuah organisasi dimana setiap
    informasi dibutuhkan oleh banyak orang sekaligus. Untuk membaginya pertama maka harus memiliki Tableau desktop terlebih dahulu barulah setelah itu diupload ke server.
    Admin server dapat mengntrol segala kegiatan yang berlangsung di server.
  - Tableau Online
    
    Versi ini hampir mirip seperti tableau server, tetapi dalam versi ini semua data yang diupload akan disimpan di dalam cloud server. Tableau online tidak membatasi
    penyimpanannya, selain itu juga bisa langsung mengkoneksikannya dengan banyak database/big data platform seperti MySQL, Hive, Amazon Aurora, Spark SQL dan masih banyak
    lagi.
  - Tableau Reader
    
    Jenis ini adalah versi gratis yang memungkinkan untuk melihat hasil pengolahan data atau workbooks dari tableau desktop. Namun, tetap saja tidak bisa mengedit *workbooks*
    tersebut dan fiturnya sangat terbatas.
  
  <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/tableau_product_suite.jpg" width=""></img><br>
    
  # <a name="tableau-workspace"></a>Tableau Workspace
  Berikut tampilan workspace pada tableau:
  
  <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/tableau_workspace.jpg" width=""></img><br>
  
  - Menu Bar
  
    Pada menu bar terdapat opsi menu seperti File, Data, Worksheet, Dashboard, Story, Analysis, Map, Format, Server, dan Windows. Opsi pada menu bar menyertakan fitur seperti
    file saving, data source connection, file export, table calculation options, and design features for creating a worksheet, dashboard, and storyboard.
  - Toolbar Icon

    Toolbar icon yang berada di bawah menu bar dapat digunakan untuk mengedit *workbook* menggunakan berbagai fitur seperti undo, redo, save, new data source, slideshow, dan       sebagainya.
  
  Pada tableau juga terdapat *Component View* yang terdiri dari:
  - Columns & Rows
  
    Panel ini digunakan untuk mendapatkan visualisasi data yang diinginkan dengan cara melakukan *drag dimensions* dan *measures* kemudian *drop* pada panel ini.
  - Pages Shelf

    Page shelf menunjukkan perubahan data dari waktu ke waktu pada *dimensions*.
  - Filter Shelf

    Penggunaannya yaitu dengan cara melakukan *drag* lalu *drop* ke panel filter untuk membatasi jumlah field yang ditunjukkan. Filter yang nampak pada dashboard memungkinkan 
    pengguna mengontrol bagaiman melihat visualisasi.
  - Marks Card

    Marks card digunakan untuk mendesain visualisasi. Komponen data visualisasi seperti color, size, label, detail, tooltip yang digunakan dalam visualisasi dapat dimodifikasi 
    dalam marks card.
  - Worksheet

    Worksheet adalah tempat di mana visualisasi sebenarnya dapat dilihat di workbook. Desain dan fungsionalitas visual dapat dilihat pada worksheet.
   
  Pada panel sebelah kiri terdapat pula *data pane* yang terdiri dari:
  - Dimensions

    Panel yang berisi data kategorik seperti teks dan tanggal.
  - Measures

    Panel yang berisi angka yang bisa dilakukan operasi-operasi statistik / aritmatika, seperti sum, average, max, min, dan sebagainya.
  - Parameters
  
    Variabel yang dapat menggantikan nilai konstan yang ditentukan oleh peneliti. 
  - Sets

    Subset dari data yang didefinisikan.
   
  Berikut icon dan deskripsi yang terdapat pada data pane:
  
  <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/data_pane.png" width=""></img><br>
  
  Selain itu, juga terdapat *Analytics Pane* yang terdiri dari:
  - Summarize

    Tombol yang digunakan untuk menambahkan komponen yang telah ditentukan seperti garis konstan, rata-rata, median dengan kuartil, dan total.
  - Model

    Menu untuk menambahkan informasi pemodelan menurut keinginan peneliti seperti garis trend, peramalan, dan distribusi rata-rata.
  - Custom

    Menu untuk menambahkan custom lines, bands, dan boxplot.
    
  # <a name="tableau-navigation"></a>Tableau Navigation
  Navigasi pada tableau terdapat pada pojok kiri bawah yang meliputi:
  
  <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/tableau_navigation.png" width=""></img><br>
  
  - Data Source
    
    Penambahan data source baru dari modifikasi data source yang ada dapat dilakukan dengan menggunakan tab 'Data Source' yang ada di bagian pojok kiri bawah.
  - Current Sheet

    Current sheet dapat dilihat dengan nama sheet. Semua sheet, dashboard, dan story yang ada di workbook dapat dilihat di sini.
  - New Sheet

    Icon ew sheet digunakan untuk membuat sheet baru pada workbook tableau.
  - New Dashboard

    Icon new dashboard digunakan untuk membuat dashboard baru pada workbook tableau.
  - New Story

    Icon new story digunakan untuk membuat storyboard baru pada workbook tableau.
    
  # <a name="praktik-tableau"></a>Praktik Tableau
  1. Pastikan Anda telah mendownload dataset yang terdapat di folder dataset.
  2. Buka aplikasi Tableau, Anda dapat menggunakan Tableau Desktop (Free Trial atau Lisensi Mahasiswa) atau menggunakan Tableau Online (Free Trial). Tampilan workspace 
     pada tableau desktop akan seperti berikut:
     
     <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/image_1.png" width=""></img><br>
     
  3. Klik Data Source yang terletak pada pojok kiri bawah, maka tampilan akan menjadi seperti berikut:
  
     <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/image_2.png" width=""></img><br>
     
  4. Klik More... kemudian pilih file dataset yang sudah di-download sehingga tampilannya akan seperti ini:

     <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/image_3.png" width=""></img><br>
     
  5. Selanjutnya klik Sheet 1 untuk menampilkan *Worksheet* dan mulailah memvisualisasikan data tersebut. Tampilannya seperti berikut ini:
     
     <img src="https://github.com/Manajemen-Cerdas-Informasi/Modul-LBE-2021/blob/main/modul-tableu/img/image_4.png" width=""></img><br>
  
  Sumber Referensi:
  - https://anaktik.com/tableau/
  - https://www.datacamp.com/community/tutorials/data-visualisation-tableau
  - https://www.guru99.com/introduction-tableau-workspace-navigation.html
