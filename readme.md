# Afifah-profile
Saya membuat sebuah web profile sederhana yang menampilkan foto, nama, dan link sosial media.

## Penjelasan Kode HTML
```html
<!DOCTYPE html> /* digunakan untuk memberi tahu browser bahwa dokumen ini menggunakan HTML5 */
<html lang="en"> /* menandakan bahasa halaman adalah Bahasa Inggris */
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Profile</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://kit.fontawesome.com/7f4731297f.js" crossorigin="anonymous"></script>
</head>
<body>
```


- ```html<!DOCTYPE html>``` 
- ```<html lang="en">```  
- ```<head>``` terdapat `<meta charset="UTF-8">` yang berfungsi agar teks, simbol, dan emoji bisa terbaca dengan benar, 
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` yang membuat tampilan website responsif di berbagai perangkat.
- `<title>My Profile</title>` digunakan untuk memberi judul pada tab browser.  
- `<link rel="preconnect" href="https://fonts.googleapis.com">`: digunakan untuk menghubungkan dan mengambil font dari Google Fonts seperti Open Sans dan Montserrat agar tampilan teks lebih menarik.  
- `<link rel="stylesheet" href="style.css">` digunakan untuk menghubungkan file CSS eksternal yang mengatur desain seperti warna, ukuran, dan tata letak. 
- `<script src="https://kit.fontawesome.com/..."></script>` digunakan untuk memanggil icon dari Font Awesome seperti icon Instagram, Facebook, Twitter, LinkedIn, dan GitHub.  
- `<body>` terdapat `<div class="container">` sebagai pembungkus seluruh isi halaman.
- `<div class="profil">` yang berisi `<img src="caca.jpg" alt="foto profil">` untuk menampilkan foto profil.
- `<h2 class="fontsaya">` untuk menampilkan nama atau sapaan. 
- `<div class="social">` yang berisi beberapa tag `<a href="...">` sebagai link menuju sosial media. 
- `<div class="sosmed open-sans">` sebagai tombol yang menampilkan icon `<i class="fa-brands ..."></i>` atau emoji `<span class="emoji">🏎️</span>`beserta nama platform, dan pada link YouTube ditambahkan `target="_blank"` serta `rel="noopener noreferrer"` agar link terbuka di tab baru dengan lebih aman.

## Penjelasan Kode CSS
* { margin: 0; padding: 0; } Reset semua elemen dengan menghilangkan margin dan padding default untuk konsistensi layout.
body { height: 100vh; width: 100%; background-image: url('bglily.jpeg'); background-position: center; background-size: cover; background-repeat: no-repeat; display: flex; justify-content: center; align-items: center; } Mengatur body penuh tinggi viewport, lebar 100%, latar belakang gambar yang diposisikan tengah, ukuran cover, tidak diulang, dan menggunakan flexbox untuk memusatkan konten secara horizontal dan vertikal.
container { display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 30px; } Membuat container sebagai flexbox vertikal, memusatkan item secara horizontal dan vertikal, dengan jarak 30px antar elemen.
.profil { display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 20px; } Membuat bagian profil sebagai flexbox vertikal, memusatkan item, dengan jarak 20px antar elemen.
.profil img { width: 100px; height: 95px; border-radius: 50%; } Mengatur gambar profil lebar 100px, tinggi 95px, dan bentuk bulat (lingkaran).
.profil h2 { color: white; font-size: 1.1rem; } Mengatur warna teks heading h2 menjadi putih, ukuran font 1.1rem.
.social { display: flex; flex-direction: column; text-align: center; gap: 10px; font-size: 0.7rem; } Membuat bagian sosial sebagai flexbox vertikal, teks rata tengah, jarak 10px antar item, ukuran font 0.7rem.
.social a { text-decoration: none; color: whitesmoke; } Menghilangkan garis bawah link dan mengatur warna teks menjadi abu-abu terang.
/* button */` Komentar untuk menandai bagian styling tombol sosial.
.sosmed { background-color: rgba(158, 100, 109, 0.5); backdrop-filter: blur(8px); -webkit-backdrop-filter: blur(8px); width: 200px; height: 30px; display: flex; align-items: center; justify-content: center; position: relative; border-radius: 20px; transition: background-color 0.3s ease; } Mengatur tombol sosial dengan latar belakang semi-transparan, efek blur, lebar 200px, tinggi 30px, flexbox untuk memusatkan, posisi relatif, sudut bulat 20px, dan transisi warna latar saat hover.
.sosmed .emoji { position: absolute; left: 8px; top: 30%; transform: translateY(-50%); font-size: 1.8rem; line-height: 1; } Memposisikan emoji secara absolut di kiri tombol, ukuran font 1.8rem, tinggi baris 1.
.sosmed i { position: absolute; left: 16px; top: 50%; transform: translateY(-50%); font-size: 1.2rem; } Memposisikan ikon Font Awesome secara absolut di kiri tombol, ukuran font 1.2rem.
.sosmed:hover { background-color: rgb(65, 24, 24); transition: 0.3s; } Mengubah warna latar tombol menjadi gelap saat hover, dengan transisi 0.3 detik.
/* font */ Komentar untuk menandai bagian font.
.fontsaya { font-family: "Montserrat", sans-serif; font-weight: 400; font-style: normal; font-size: 1rem; } Mengatur font untuk class "fontsaya" menggunakan Montserrat, berat normal, gaya normal, ukuran 1rem.
.open-sans { font-family: "Open Sans", sans-serif; font-optical-sizing: auto; font-style: normal; font-size: 0.9rem; font-variation-settings: "wdth" 100; } Mengatur font untuk class "open-sans" menggunakan Open Sans, sizing otomatis, gaya normal, ukuran 0.9rem, dengan variasi lebar 100.
.sosmed { cursor: pointer; } Mengubah kursor menjadi pointer saat hover pada tombol sosial.
