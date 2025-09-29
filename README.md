# Lab2Web
Praktikum 2 CSS Dasar

1.Tahap awal (Membuat Dokumen HTML)
Disini kita membuat Dokumen HTML agar website ini terbentuk kerangka nya dan nanti akan di isi dengan css, setelah itu lalu masukan kode dalam editor kode kalian seperti VSCode.
Didalamnya seperti ini:

```html

<!DOCTYPE html> <html lang="en"> <head> <meta charset="UTF-8"> <meta name="viewport" content="width=device-width, initial-scale=1.0"> <title>CSS Dasar</title> </head> <body> <header> <h1>CSS Internal dan <i>Inline CSS</i></h1> </header> <nav> <a href="lab2_css_dasar.html">CSS Dasar</a> <a href="lab2_css_eksternal.html">CSS Eksternal</a> <a href="lab1_tag_dasar.html">HTML Dasar</a> </nav> <!-- CSS ID Selector --> <div id="intro"> <h1>Hello World</h1> <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p> <!-- CSS Class Selector --> <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a> </div> </body> </html>

```
Setelah memasukan kode tersebut ada perubahan di website nya yaitu seperti gambar di bawah ini, tahap awal berarti sudah selesai dengan baik.


<img width="550" height="129" alt="image" src="https://github.com/user-attachments/assets/1ced244e-2798-46b6-b923-e423d5e187ce" />

2.Tahap kedua (Mendeklarasikan CSS Internal)
Lalu ditahap ini kita akan menambahkan css agar website nya tidak polos atau seperti kerangka saja, kita tambahkan kode berikut dan lihat hasilnya pada gambar:
```
<head>
<title>CSS Dasar</title>
<style>
body {
font-family:'Open Sans', sans-serif;
}
header {
min-height: 80px;
border-bottom:1px solid #77CCEF;
}
h1 {
font-size: 24px;
color: #0F189F;
text-align: center;
padding: 20px 10px;
}
h1 i {
color:#6d6a6b;
}
</style>
</head>
```
ketika kode tersebut di eksekusi terdapat perubahan seperti gambar di bawah ini:
<img width="1362" height="691" alt="image" src="https://github.com/user-attachments/assets/7e6a6d50-b7f6-4729-8339-59cf9d7bf746" />

3.Tahap ketiga (Menambahkan Inline CSS)
Pada tahap tiga ini kita mengubah warna text pada tag <p> (Paragraf) di VScode, kita memasukan kode di dalam tag <p> seperti ini agar tampilannya berubah:
```
<p style="text-align: center; color: #ccd8e4;">
```
setelah di masukan lalu save dan refresh website kalian hasilnya seperti gambar di bawah ini:
<img width="1323" height="653" alt="image" src="https://github.com/user-attachments/assets/6d7fc523-9807-4af2-a657-4083c9618891" />

4.Tahap keempat (Membuat CSS Eksternal)
Disini kita akan membuat CSS eksternal dengan cara menambahkan file baru dengan nama "style_eksternal.css" setelah di buat lalu masukan kode:
```
nav {
background: #20A759;
color:#fff;
padding: 10px;
}
nav a {
color: #fff;
text-decoration: none;
padding:10px 20px;
}
nav .active,
nav a:hover {
background: #0B6B3A;
}
```
reminder kalian harus masukanpada bagiann <head>:
```
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```

Lalu hasilnya seperti di bawah dimana yang dari awal seperti kerangka pelan pelan mulai berkembang.
<img width="1365" height="698" alt="image" src="https://github.com/user-attachments/assets/ccf64722-8ce7-4e64-b4a7-8be4d23e5bfd" />

5.Tahap kelima (Menambahkan CSS Selector)
Sekarang kita coba tambahkan CSS Selector dengan ID dan Class. Buka file style_eksternal.css, lalu sisipkan kode berikut:
```
/* ID Selector */
#intro {
background: #418fb1;
border: 1px solid #099249;
min-height: 100px;
padding: 10px;
}
#intro h1 {
text-align: left;
border: 0;
color: #fff;
}
/* Class Selector */
.button {
padding: 15px 20px;
background: #bebcbd;
color: #fff;
display: inline-block;
margin: 10px;
text-decoration: none;
}
.btn-primary {
background: #E42A42;
}
```
Setelah kalian memasukan kode tersebut dalam style css kalian, lalu refresh dan tampilan nya akan berubah seperti ini

<img width="1366" height="655" alt="image" src="https://github.com/user-attachments/assets/db610f67-93b9-4d79-8f13-87ed2398ec13" />


Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )

Jawaban Pertanyaan dan Tugas
1. Eksperimen CSS
Di bagian ini kita diminta coba-coba ganti properti CSS. Misalnya ubah warna teks, ukuran huruf, atau cara paragraf diratakan. Tujuannya biar kita terbiasa mainin property CSS.
Contoh:
```
p {
  font-size: 18px;
  color: darkgreen;
  text-align: justify;
}
```
Kalau ini dijalankan, paragraf bakal tampil lebih besar, warnanya hijau, dan teksnya rata kiri-kanan.

2. Bedanya h1 {} sama #intro h1 {}
```
h1 {} berlaku buat semua tag <h1> yang ada di halaman.

#intro h1 {} khusus buat <h1> yang ada di dalam elemen dengan id intro.
Jadi kalau ada aturan bentrok, CSS yang lebih spesifik (#intro h1) yang bakal dipakai.

3. Kalau ada Internal, Eksternal, dan Inline di elemen yang sama, mana yang menang?
Urutannya gini: Inline paling kuat, lalu Internal, terakhir Eksternal.
```
Contoh:
```
<p style="color:red;">Teks ini merah</p>
```
Walaupun di internal atau eksternal warnanya di-set biru, browser tetep nurut ke inline, jadi teksnya merah.

4. Kalau elemen punya ID dan Class, mana yang kepake?
ID selalu lebih kuat dibanding Class. Kalau dua-duanya punya aturan berbeda, browser bakal nurut sama ID.
Contoh:
```
html:
<p id="paragraf-1" class="text-paragraf">Halo</p>
```
```
css:
.text-paragraf { color: blue; }
#paragraf-1 { color: red; }
```
Hasilnya teks warna merah, karena ID lebih spesifik daripada Class.









