# Lab4Web
# Lab4Web.
Mata Kuliah: Pemrograman WebDosen Pengampu: Agung Nugroho, S.T., M.Kom.Nama Mahasiswa: Siti Nurainah NIM: 312510171 Kelas: I253C Teknik Informatika Universitas Pelita Bangsa📌 Tujuan Praktikum Mahasiswa mampu memahami struktur dasar pembuatan Layout.   Mahasiswa mampu memahami konsep dasar Box Element.   Mahasiswa mampu memahami penggunaan CSS Floating dan Clearfix.   Mahasiswa mampu mengimplementasikan elemen semantik pada HTML5 (<header>, <nav>, <section>, <aside>, <footer>).   Mahasiswa mampu membuat Layout Website Sederhana yang responsif dan terstruktur.   🛠️ Langkah-Langkah Praktikum1. Persiapan AwalMembuka teks editor (Visual Studio Code).Membuat direktori atau folder kerja baru dengan nama Lab4Web.   2. Praktikum 1: Konsep Box Element & CSS FloatPada latihan ini, kita mempelajari bagaimana elemen HTML diperlakukan sebagai sebuah kotak (box) yang memiliki properti margin, border, padding, dan content, serta cara mengatur penempatannya menggunakan properti CSS float.Kode HTML (lab4_box.html):HTML<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
    <style>
        div {
            float: left;
            padding: 10px;
        }
        .div1 { background: red; }
        .div2 { background: yellow; }
        .div3 { background: green; }
        .div4 {
            background-color: blue;
            clear: left;
            float: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
</body>
</html>
Penjelasan Langkah:Struktur Dasar (<header>, <h1>): Membuat judul utama halaman web "Box Element".   Box Element & Float: Menggunakan elemen <div> dengan kelas .div1, .div2, dan .div3. Dengan memberikan properti float: left;, kotak-kotak tersebut yang awalnya berbaris secara vertikal (block) akan bergeser dan sejajar secara horizontal ke sebelah kiri.   Clearfix (clear: left;): Menambahkan .div4 dengan properti clear: left; agar elemen ke-4 tidak ikut mengapung sejajar di samping elemen sebelumnya, melainkan turun ke baris baru di bawah elemen yang mengapung.   Screenshot Hasil Praktikum Box Element & Float:
(Referensi Tampilan: Menunjukkan kotak Div 1, Div 2, Div 3 sejajar secara horizontal, dan Div 4 berada di baris bawahnya dengan warna biru).   3. Praktikum 2: Membuat Layout SederhanaPada bagian ini, kita membangun kerangka layout website lengkap menggunakan elemen semantik HTML5 dan styling CSS eksternal.A. Struktur File & FolderStruktur folder di dalam Lab4Web:PlaintextLab4Web/
│
├── home.html
└── style.css
B. Kode HTML (home.html)HTML<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <!-- Header -->
        <header>
            <h1>Layout Sederhana</h1>
        </header>

        <!-- Navigasi Menu -->
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>

        <!-- Hero Panel -->
        <section id="hero">
            <h1>Hello World!</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
            <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
        </section>

        <!-- Wrapper (Main Content & Sidebar) -->
        <section id="wrapper">
            <section id="main">
                <!-- 3 Kolom Box -->
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>

                <hr class="divider" />

                <!-- Artikel Section -->
                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
                </article>
            </section>

            <!-- Sidebar -->
            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>
                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
                </div>
            </aside>
        </section>

        <!-- Footer -->
        <footer>
            <p>&copy; 2026 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
C. Kode CSS (style.css)CSS/* Import Google Font */
@import url('https://fonts.googleapis.com/css?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height: 1;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
}
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* Header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}

/* Navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active, nav a:hover {
    background-color: #2b83ea;
}

/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}

/* Main Content & Sidebar Layout */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
    box-sizing: border-box;
}
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
    box-sizing: border-box;
}

/* Widget Sidebar */
.widget-box {
    border: 1px solid #eee;
    margin-bottom: 20px;
}
.widget-box .title {
    padding: 10px 16px;
    background-color: #428bca;
    color: #fff;
}
.widget-box ul {
    list-style-type: none;
}
.widget-box li {
    border-bottom: 1px solid #eee;
}
.widget-box li a {
    padding: 10px 16px;
    color: #333;
    display: block;
    text-decoration: none;
}
.widget-box li:hover a {
    background-color: #eee;
}

/* Box 3 Kolom */
.box {
    display: block;
    float: left;
    width: 33.333333%;
    box-sizing: border-box;
    padding: 0 10px;
    text-align: center;
}
.box h3 { margin: 15px 0; }
.box p { line-height: 20px; font-size: 14px; margin-bottom: 15px; }
.image-circle { border-radius: 50%; }

/* Clearfix untuk Row */
.row:after {
    content: '';
    display: table;
    clear: both;
}

/* Artikel */
.divider {
    border: 0;
    border-top: 1px solid #eeeeee;
    margin: 40px 0;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}

/* Footer */
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
    text-align: center;
}
📸 Dokumentasi Screenshot PraktikumBerikut adalah rangkuman tahapan tampilan di browser dari kode di atas:Tampilan Kerangka Layout Dasar: Menampilkan Header judul web serta menu navigasi sederhana.   Tampilan Hero Panel: Penambahan section banner utama dengan latar belakang abu-abu terang dan tombol ajakan (Call to Action).   Tampilan Sidebar Widget: Penataan widget navigasi dan widget teks di sisi kanan menggunakan layout float.   Tampilan 3 Kolom Box & Artikel: Penambahan komponen grid 3 kolom melingkar di area konten utama beserta layout artikel featurette.   ✅ Tugas & Pertanyaan TambahanLayout Menu About: Dibuat dengan menambahkan file about.html berisi informasi profil, 


<img width="1599" height="822" alt="jawaban tugas 2" src="https://github.com/user-attachments/assets/b42b9df3-8671-481a-a22e-660947042fae" />
<img width="1600" height="791" alt="jawaban tugas 1" src="https://github.com/user-attachments/assets/4fbe9c9a-394e-4fa7-90e4-4c6013fea845" />
<img width="1297" height="828" alt="Hasil dari coding ke dua 12" src="https://github.com/user-attachments/assets/42fea804-5247-40e8-82b2-8753c74d6f77" />
<img width="1239" height="727" alt="Hasil dari coding ke dua 11" src="https://github.com/user-attachments/assets/91772ec1-beb6-4f5c-a3a4-0de20667006e" />
<img width="1240" height="725" alt="Hasil dari coding ke dua 10" src="https://github.com/user-attachments/assets/726119b3-728e-4da0-9770-7ab54caa97e3" />
<img width="1600" height="826" alt="Hasil dari coding ke dua 9" src="https://github.com/user-attachments/assets/bc0a0f0d-9b76-4b5f-8227-0363479055a9" />
<img width="1599" height="809" alt="Hasil dari coding ke dua 8" src="https://github.com/user-attachments/assets/fdc2e21e-fae4-4ac2-a5fd-6257d175e0d6" />
<img width="1575" height="833" alt="Hasil dari coding ke dua 7" src="https://github.com/user-attachments/assets/0e05ad46-d3db-47ca-8c0d-98619e9dca04" />
<img width="1588" height="816" alt="Hasil dari coding ke dua 6" src="https://github.com/user-attachments/assets/8f889f62-3adf-460b-9c7b-31fef58b681f" />
<img width="1600" height="851" alt="Hasil dari coding ke dua 5" src="https://github.com/user-attachments/assets/08c52241-3294-4eed-803e-17b888e197e2" />
<img width="1600" height="826" alt="Hasil dari coding ke dua 4" src="https://github.com/user-attachments/assets/43276faf-e438-4a42-89bb-7cab7f7964f5" />
<img width="1590" height="808" alt="Hasil dari coding ke dua 3" src="https://github.com/user-attachments/assets/2f80bfe5-ed0f-41c2-9134-a97c13c1bf7e" />
<img width="1600" height="811" alt="Hasil dari coding ke dua 1" src="https://github.com/user-attachments/assets/7b723931-ffbd-420b-b84c-4d320b291edd" />
<img width="1593" height="797" alt="Hasil 4" src="https://github.com/user-attachments/assets/37e86cd8-077c-45a3-99df-188a1ec10e9d" />
<img width="1600" height="818" alt="Hasil 3" src="https://github.com/user-attachments/assets/6539b2a8-a954-441a-b190-1986e1924f96" />
<img width="1598" height="842" alt="Hasil 2" src="https://github.com/user-attachments/assets/eeb3d81c-3662-431e-ab4e-3b9e74f54be1" />
<img width="1600" height="850" alt="Hasil 1" src="https://github.com/user-attachments/assets/02ae597b-cf5a-41b4-93bc-4cd146afe1b7" />
<img width="1600" height="857" alt="gambar dari tugas" src="https://github.com/user-attachments/assets/338416cc-461f-42e4-b2fc-d42fecbe59c0" />
<img width="1297" height="828" alt="Gambar dari coding ke dua 12" src="https://github.com/user-attachments/assets/ad8a8c3a-f345-4dd3-8e0f-5c54a006f0be" />
<img width="1590" height="819" alt="Gambar dari coding ke dua 11 1" src="https://github.com/user-attachments/assets/468f9821-0f84-4cee-bd92-b6d972847913" />
<img width="1295" height="819" alt="Gambar dari coding ke dua 10" src="https://github.com/user-attachments/assets/303ec7ff-62c9-4096-b20e-57f89a62873b" />
<img width="1591" height="830" alt="Gambar dari coding ke dua 9 2" src="https://github.com/user-attachments/assets/5c0e4435-cc8f-4f98-b20c-df01b5f94cea" />
<img width="1568" height="778" alt="Gambar dari coding ke dua 9 1" src="https://github.com/user-attachments/assets/2ce1225a-98a0-40ee-824b-5e50ba56c6a1" />
<img width="1600" height="838" alt="Gambar dari coding ke dua 8" src="https://github.com/user-attachments/assets/164698d7-3635-4628-8573-f1bc9f54cf6b" />
<img width="1590" height="845" alt="Gambar dari coding ke dua 7" src="https://github.com/user-attachments/assets/c17239b7-1666-4b16-97ec-6dd9aefef362" />
<img width="1583" height="822" alt="Gambar dari coding ke dua 6" src="https://github.com/user-attachments/assets/5128bcbc-798a-4ac8-8ebb-d9c95b43c7b1" />
<img width="1594" height="832" alt="Gambar dari coding ke dua 5" src="https://github.com/user-attachments/assets/01df1656-f0a2-49f3-b320-e4b4235d5335" />
<img width="1587" height="845" alt="Gambar dari coding ke dua 4" src="https://github.com/user-attachments/assets/def15123-11ee-4bae-b451-4fbe8e3abc23" />
<img width="1195" height="798" alt="Gambar dari coding ke dua 3" src="https://github.com/user-attachments/assets/77189fc8-582f-4737-b17c-e66cc885c8ee" />
<img width="1193" height="773" alt="Gambar dari coding ke dua 2" src="https://github.com/user-attachments/assets/ec1b3227-2913-4531-b53b-ff04ae5cf604" />
<img width="1196" height="800" alt="Gambar dari coding ke dua 1" src="https://github.com/user-attachments/assets/de125c69-a1f7-4ff8-97a3-9c32e815e40c" />
<img width="1594" height="843" alt="gambar 11 2" src="https://github.com/user-attachments/assets/f2b432bd-0516-444f-b89c-dd8e407e5236" />
<img width="1196" height="790" alt="Gambar 4" src="https://github.com/user-attachments/assets/397a3315-9f60-4ca8-b234-71400b15d12e" />
<img width="1193" height="804" alt="Gambar 3" src="https://github.com/user-attachments/assets/c98dc3c3-5063-4f83-9e45-60602397e606" />
<img width="1197" height="797" alt="Gambar 2" src="https://github.com/user-attachments/assets/bf9d03c0-5661-4195-8f4e-d4feecacc80f" />
<img width="1200" height="802" alt="Gambar 1" src="https://github.com/user-attachments/assets/9d613ebe-e129-4bf9-8ab5-c3fd94b8ee71" />


deskripsi diri, serta portofolio mahasiswa.Layout Menu Contact: Dibuat dengan menambahkan file kontak.html yang dilengkapi elemen formulir input HTML (<input> untuk Nama dan Email, <textarea> untuk pesan, serta tombol Kirim).Laporan praktikum ini disusun dan dikerjakan secara mandiri untuk memenuhi tugas mata kuliah Pemrograman Web Universitas Pelita Bangsa.
