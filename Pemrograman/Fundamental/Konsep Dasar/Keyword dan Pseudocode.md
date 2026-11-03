#programming 

Dua konsep mendasar yang akan selalu Anda temui saat pertama kali mempelajari pemrograman adalah kata kunci khusus yang dipesan oleh bahasa komputer (**Keyword**) dan cara merancang logika program dalam bahasa manusia (**Pseudocode**).

## 1. Kata Kunci Khusus (Reserved Keywords)

Dalam bahasa manusia, kita mengenal ribuan kosakata dalam kamus. Namun di dalam bahasa pemrograman, jumlah kata perintah inti (*keywords*) sebenarnya sangat sedikit dan ramah dihafalkan:
- Bahasa **Python** hanya memiliki sekitar 35 keyword.
- Bahasa **JavaScript** memiliki sekitar 60 keyword.
- Bahasa **Go** hanya memiliki 25 keyword.

Keyword adalah kata-kata khusus yang telah dipesan oleh pembuat bahasa pemrograman dan memiliki fungsi spesifik yang sudah ditentukan oleh sistem.

### Tabel Contoh Keyword Populer dalam Python
| Keyword | Fungsi Singkat |
| :--- | :--- |
| `if`, `elif`, `else` | Mengatur percabangan keputusan. |
| `for`, `while` | Mengatur perulangan kode. |
| `def`, `return` | Mendefinisikan fungsi dan mengembalikan nilai. |
| `True`, `False` | Nilai kebenaran tipe data Boolean. |
| `and`, `or`, `not` | Operator gerbang logika. |
| `import`, `from` | Mengambil modul kode dari berkas lain. |
| `class` | Membuat cetak biru objek (OOP). |

> [!WARNING] Aturan Penamaan Variabel Terkait Keyword
> Anda **TIDAK BOLEH** menggunakan kata kunci di atas sebagai nama variabel buatan Anda sendiri. 
> Misalnya kode `let if = 5;` atau `let for = "Aryanda";` akan langsung ditolak oleh komputer dengan pesan *SyntaxError: Unexpected token* karena komputer mengira Anda sedang ingin membuat percabangan atau perulangan, bukan membuat wadah variabel.

## 2. Kode Semu (Pseudocode)

Sebelum mulai mengetik baris kode asli yang rumit dengan tanda kurung dan titik koma, programmer profesional hampir selalu menyusun alur berpikirnya terlebih dahulu dalam bentuk **Pseudocode (Kode Semu)**.

Pseudocode adalah cara menuliskan instruksi program menggunakan bahasa manusia sehari-hari (bisa bahasa Indonesia atau bahasa Inggris) yang diformat menyerupai struktur kode pemrograman tanpa terikat aturan ketat bahasa tertentu.

Tujuan utama pseudocode adalah **memastikan alur logika Anda sudah benar 100% sebelum Anda mulai berurusan dengan sintaksis bahasa komputer**.

## 3. Contoh Praktis: Merancang Pseudocode Sistem Login

Bayangkan kita ingin membuat sistem otentikasi login pengguna:
- Pengguna memasukkan alamat email dan kata sandi.
- Sistem mencocokkan data tersebut dengan basis data.
- Jika cocok, pengguna dipersilakan masuk ke halaman utama dasbor.
- Jika tidak cocok, sistem menampilkan pesan peringatan dan meminta pengguna mencoba kembali.

Berikut adalah contoh penulisan pseudocode yang rapi dan mudah dipahami:

```text
ALGORITMA SistemLogin:

  // 1. Ambil input dari pengguna satu per satu
  BACA inputEmail DARI kolom_email
  BACA inputPassword DARI kolom_password

  // 2. Lakukan pengecekan kondisi ke basis data
  JIKA (inputEmail COCOK DENGAN database.email) DAN (inputPassword COCOK DENGAN database.password) MAKA:
      TAMPILKAN "Selamat Datang! Login Berhasil."
      ARAHKAN PENGGUNA KE "Halaman_Dasbor"
  LAINNYA:
      TAMPILKAN "Kombinasi email atau password salah. Silakan coba lagi."
      BERSIHKAN KOLOM inputPassword
  AKHIR_JIKA

SELESAI
```

Perhatikan betapa jelasnya alur di atas:
- Siapa pun yang membaca pseudocode tersebut (baik programmer junior, programmer senior, maupun manajer produk) dapat langsung memahami alur kerja sistem dalam hitungan detik.
- Ketika pseudocode ini diberikan kepada programmer Python, ia akan menerjemahkannya menggunakan `if ... else:`.
- Ketika diberikan kepada programmer JavaScript, ia akan menerjemahkannya menggunakan `if (...) { ... } else { ... }`.
- Alur logikanya tetap sama persis, yang berbeda hanyalah pakaian bahasanya.
