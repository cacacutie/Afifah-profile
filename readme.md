# Afifah-profile
Saya membuat sebuah web profile sederhana yang menampilkan foto, nama, dan link sosial media.

## Penjelasan Kode HTML
- ```<!DOCTYPE html>``` : digunakan untuk memberi tahu browser bahwa dokumen ini menggunakan HTML5
- ```<html lang="en">``` : menandakan bahasa halaman adalah Bahasa Inggris
- Di dalam ```<head>```, terdapat `<meta charset="UTF-8">` yang berfungsi agar teks, simbol, dan emoji bisa terbaca dengan benar, 
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` : membuat tampilan website responsif di berbagai perangkat.
- `<title>My Profile</title>` : digunakan untuk memberi judul pada tab browser.  
- `<link rel="preconnect" href="https://fonts.googleapis.com">`: digunakan untuk menghubungkan dan mengambil font dari Google Fonts seperti Open Sans dan Montserrat agar tampilan teks lebih menarik.  
- `<link rel="stylesheet" href="style.css">` : digunakan untuk menghubungkan file CSS eksternal yang mengatur desain seperti warna, ukuran, dan tata letak. 
- `<script src="https://kit.fontawesome.com/..."></script>`: digunakan untuk memanggil icon dari Font Awesome seperti icon Instagram, Facebook, Twitter, LinkedIn, dan GitHub.  
- Di dalam`<body>`, terdapat `<div class="container">` sebagai pembungkus seluruh isi halaman.
- `<div class="profil">` yang berisi `<img src="caca.jpg" alt="foto profil">` untuk menampilkan foto profil.
- `<h2 class="fontsaya">`: untuk menampilkan nama atau sapaan. 
- `<div class="social">` yang berisi beberapa tag `<a href="...">` sebagai link menuju sosial media. 
- `<div class="sosmed open-sans">` sebagai tombol yang menampilkan icon `<i class="fa-brands ..."></i>` atau emoji `<span class="emoji">🏎️</span>`beserta nama platform, dan pada link YouTube ditambahkan `target="_blank"` serta `rel="noopener noreferrer"` agar link terbuka di tab baru dengan lebih aman.

## Penjelasan Kode CSS
- `* { margin: 0; padding: 0; }`: Mereset margin dan padding bawaan semua elemen agar layout konsisten.
- `body { height: 100vh; width: 100%; background-image: url('images/bglily.jpeg'); background-position: center; background-size: cover; background-repeat: no-repeat; display: flex; justify-content: center; align-items: center; }`: Mengisi viewport penuh dengan latar belakang bunga, lalu memanfaatkan flexbox untuk memusatkan `.container` secara horizontal dan vertikal.
- `.container { display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 30px; }`: Membuat wrapper utama sebagai flex column dengan jarak 30px antarblok.
- `.profil { display: flex; flex-direction: column; justify-content: center; align-items: center; gap: 20px; }`: Menyusun informasi profil secara vertikal dan memusatkan konten dengan jarak antar item.
- `.profil img { width: 100px; height: 95px; border-radius: 50%; }`: Mengatur foto profil menjadi lingkaran kecil.
- `.profil h2 { color: white; font-size: 1.1rem; }`: Memberi warna putih dan ukuran font 1.1rem pada nama/profil utama.
- `.social { display: flex; flex-direction: column; text-align: center; gap: 10px; font-size: 0.7rem; background-color: rgba(158, 100, 109, 0.8); padding: 2rem; border-radius: 2rem; }`: Menjadikan area sosial sebagai kolom pusat dengan latar semi-transparan, padding 2rem, dan sudut bundar.
- `.social a { text-decoration: none; color: whitesmoke; }`: Menghilangkan underline link dan menjaga warna teks agar kontras dengan latar belakang.
- `.sosmed { background-color: rgba(246, 141, 157, 0.5); backdrop-filter: blur(8px); -webkit-backdrop-filter: blur(8px); width: 200px; height: 30px; display: flex; align-items: center; justify-content: center; position: relative; border-radius: 20px; transition: background-color 0.3s ease; cursor: pointer; }`: Menyiapkan tombol sosial dengan latar kabur, ukuran tetap, posisi relatif untuk ikon, sudut membulat, dan transisi warna plus kursor pointer.
- `.sosmed .emoji { position: absolute; left: 8px; top: 30%; transform: translateY(-50%); font-size: 1.8rem; line-height: 1; }`: Menempatkan emoji di sisi kiri tombol.
- `.sosmed i { position: absolute; left: 16px; top: 50%; transform: translateY(-50%); font-size: 1.2rem; }`: Meletakkan ikon Font Awesome secara simetris di dalam tombol.
- `.sosmed:hover { background-color: rgb(65, 24, 24); transition: 0.3s; }`: Menggelapkan tombol saat pengguna mengarahkan kursor untuk memberi umpan balik visual.
- `.fontsaya { font-family: "Montserrat", sans-serif; font-weight: 400; font-style: normal; font-size: 1rem; }`: Memastikan teks nama profil memakai Montserrat dengan ukuran 1rem.
- `.open-sans { font-family: "Open Sans", sans-serif; font-optical-sizing: auto; font-style: normal; font-size: 0.9rem; font-variation-settings: "wdth" 100; }`: Mengatur label sosial menggunakan Open Sans dengan variasi lebar khusus.
