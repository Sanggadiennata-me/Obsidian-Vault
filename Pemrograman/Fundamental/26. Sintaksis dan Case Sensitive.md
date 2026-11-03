#programming 

Sama halnya seperti bahasa manusia yang memiliki tata bahasa (tanda titik, tanda koma, susunan Subjek-Predikat-Objek), setiap bahasa pemrograman juga memiliki aturan baku yang mengatur bagaimana kode harus ditulis. Kumpulan aturan penulisan inilah yang disebut **Sintaksis (Syntax)**.

Jika Anda melanggar aturan sintaksis, program tidak akan bisa dijalankan sama sekali. Komputer akan langsung menolak dan memunculkan pesan kesalahan yang disebut **Syntax Error**.

## 1. Mengenal Aturan Sintaksis Dasar

Setiap bahasa pemrograman memiliki kebiasaan sintaksis yang berbeda:

### A. Tanda Baca Akhir Baris (Semicolon / Titik Koma `;`)
Pada bahasa seperti C++, Java, PHP, dan JavaScript, setiap baris perintah (*statement*) secara tradisional diakhiri dengan tanda titik koma `;`:
```php
<?php
$nama = "Aryanda";
echo $nama;
?>
```
Jika Anda lupa mengetik tanda titik koma di akhir baris, program akan langsung berhenti dengan pesan *Parse Error / Syntax Error*. Sebaliknya, bahasa seperti Python tidak menggunakan titik koma, melainkan mengandalkan tombol Enter (baris baru).

### B. Tanda Petik untuk Teks (Quotes)
Komputer membedakan antara angka murni dan teks menggunakan tanda petik:
- `100` adalah angka integer (bisa dijumlahkan atau dikalikan).
- `"100"` atau `'100'` adalah teks string (karakter tulisan biasa).
Jika Anda lupa menutup tanda petik, misalnya `let pesan = "Halo;`, komputer akan bingung dan memicu Syntax Error.

## 2. Sensitivitas Huruf Kapital: Case Sensitive vs Non Case Sensitive

Hampir seluruh bahasa pemrograman modern yang populer saat ini (Python, JavaScript, C, C++, Java, PHP, Go, Rust, Swift) bersifat **Case Sensitive**.

Artinya: **huruf besar (kapital) dan huruf kecil dianggap sebagai dua karakter yang sama sekali berbeda**.

Perhatikan contoh berikut:
```javascript
let nama = "Budi";
let Nama = "Siti";
let NAMA = "Rudi";
```

Meskipun secara arti ketiga kata di atas sama-sama berarti "nama", bagi komputer ketiga variabel tersebut adalah **tiga wadah yang berbeda di memori**:
- `nama` (semua huruf kecil) berisi `"Budi"`.
- `Nama` (huruf 'N' kapital) berisi `"Siti"`.
- `NAMA` (semua huruf kapital) berisi `"Rudi"`.

Jika Anda membuat variabel bernama `totalBelanja` (dengan huruf 'B' kapital), namun saat memanggilnya Anda mengetik `totalbelanja` (dengan huruf 'b' kecil):
```javascript
let totalBelanja = 50000;

// KESALAHAN UMUM PEMULA:
console.log(totalbelanja); 
// Hasil: ReferenceError: totalbelanja is not defined!
```
Komputer akan mengeluh bahwa variabel `totalbelanja` tidak pernah ditemukan, karena huruf 'b'-nya berbeda kapitalisasi.

### Apakah Ada Bahasa yang Non-Case Sensitive?
Ada beberapa bahasa lama atau bahasa khusus yang bersifat *Non-Case Sensitive* (tidak membedakan huruf besar dan kecil), contohnya:
- **SQL** (perintah `SELECT * FROM users` sama persis dengan `select * from users`).
- **HTML** (tag `<div>` sama dengan `<DIV>`).
- **Pascal** dan **Visual Basic**.

Namun untuk penulisan logika kode program modern, biasakanlah selalu teliti terhadap setiap huruf kapital yang Anda ketik.

## 3. Konvensi Penamaan Populer (Naming Conventions)

Karena spasi tidak diizinkan di tengah nama variabel, para programmer di seluruh dunia menggunakan konvensi penamaan standar agar kode mudah dibaca:

1. **camelCase**: Kata pertama huruf kecil, kata berikutnya diawali huruf kapital.
   - *Contoh*: `totalHargaBarang`, `namaLengkapSiswa`, `isUserLoggedIn`.
   - Populer di: JavaScript, Java, C#.
2. **snake_case**: Semua huruf kecil dipisahkan oleh garis bawah (*underscore*).
   - *Contoh*: `total_harga_barang`, `nama_lengkap_siswa`, `is_user_logged_in`.
   - Populer di: Python, PHP, basis data SQL.
3. **PascalCase**: Setiap kata diawali dengan huruf kapital (termasuk kata pertama).
   - *Contoh*: `TotalHargaBarang`, `DataPengguna`.
   - Populer untuk: Penamaan Class atau Komponen di React/OOP.
