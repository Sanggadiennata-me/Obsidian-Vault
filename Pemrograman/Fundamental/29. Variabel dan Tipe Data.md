#programming 

Ketika kita membuat sebuah program, hampir semua aktivitas yang kita lakukan adalah menyimpan data sementara, mengolah data tersebut, dan menampilkan hasilnya. Untuk menyimpan data sementara di dalam memori komputer (RAM), kita menggunakan konsep yang disebut **Variabel** dan **Tipe Data**.

## 1. Apa Itu Variabel? (Analogi Toples Berlabel)

Bayangkan Anda sedang menata bumbu di dapur:
- Anda memiliki sebuah toples kaca kosong.
- Anda menempelkan stiker label pada toples tersebut dengan tulisan: `"Gula Pasir"`.
- Anda mengisi toples tersebut dengan 500 gram gula pasir.
- Kapan pun Anda membutuhkan gula untuk membuat teh, Anda cukup mencari toples dengan label `"Gula Pasir"`.
- Jika gula pasir tersebut habis dan Anda ingin menggantinya dengan gula merah, Anda bisa mengosongkan toples tersebut dan mengisinya dengan gula merah. Labelnya tetap sama, tetapi isinya berubah (*bervariasi*).

Itulah **Variabel** di dalam komputer:
- **Nama Variabel** adalah label pada stiker (misalnya `namaPengguna`, `totalHarga`, `skorPemain`).
- **Nilai Variabel** adalah isi benda di dalam toples (misalnya `"Aryanda"`, `50000`, `100`).
- **Memori Komputer** adalah rak dapur tempat toples-toples tersebut diletakkan dengan aman.

## 2. Mengapa Tipe Data (Data Types) Itu Ada?

Di dunia nyata, Anda tidak bisa menyimpan air mineral di dalam kantong kertas yang berlubang, dan Anda tidak bisa menyimpan pisau dapur tajam di dalam wadah kain tipis. Setiap jenis benda membutuhkan wadah yang sesuai dengan wujud fisiknya.

Komputer juga demikian. Komputer harus tahu jenis data apa yang sedang disimpan agar komputer dapat mengalokasikan ukuran memori yang pas dan tidak salah menjalankan operasi:
- Angka `10` dan `20` dapat dijumlahkan menjadi `30`.
- Teks `"Halo "` dan `"Dunia"` dapat disambung menjadi `"Halo Dunia"`.
- Tetapi Anda tidak bisa mengalikan teks `"Kucing"` dengan teks `"Mobil"`.

## 3. Empat Tipe Data Primitif Paling Mendasar

Hampir seluruh bahasa pemrograman di dunia memiliki empat tipe data dasar berikut:

| Tipe Data | Nama Lengkap | Karakteristik | Contoh Nilai |
| :--- | :--- | :--- | :--- |
| **Integer** | Bilangan Bulat | Angka utuh tanpa koma desimal, bisa bernilai positif, nol, atau negatif. | `1`, `42`, `0`, `-15`, `2026` |
| **Float / Double** | Bilangan Desimal | Angka yang memiliki nilai pecahan atau tanda koma titik desimal. | `3.14`, `0.75`, `-2.5`, `99.9` |
| **String** | Teks / Tulisan | Rangkaian karakter huruf, kata, atau simbol yang wajib diapit tanda petik (`"` atau `'`). | `"Aryanda"`, `'Belajar Koding'`, `"12345"` |
| **Boolean** | Nilai Kebenaran | Tipe data paling sederhana di dunia yang hanya memiliki tepat dua kemungkinan nilai: Benar atau Salah. | `true` atau `false` |

> [!NOTE] Perhatikan Perbedaan String dan Angka
> Angka `500` tanpa tanda petik adalah tipe data **Integer** yang bisa dijumlahkan (`500 + 500 = 1000`).
> Namun `"500"` di dalam tanda petik adalah tipe data **String** (teks tulisan). Jika Anda menjumlahkan `"500" + "500"`, komputer akan menyambung teks tersebut menjadi `"500500"`.

## 4. Cara Menuliskan Variabel di Berbagai Bahasa

Meskipun konsep variabel sama di semua bahasa, cara penulisannya sedikit berbeda:

```javascript
// JavaScript: Menggunakan kata kunci let atau const
let nama = "Aryanda";
let usia = 20;
let sudahLulus = true;

// Python: Langsung menulis nama variabel tanpa kata kunci pembungkus
nama = "Aryanda"
usia = 20
sudah_lulus = True

// PHP: Semua variabel wajib diawali dengan simbol tanda dolar ($)
$nama = "Aryanda";
$usia = 20;
$sudah_lulus = true;

// C++ / Java (Statically Typed): Wajib menyebutkan tipe data wadah di depan nama
String nama = "Aryanda";
int usia = 20;
boolean sudahLulus = true;
```

## 5. Tipe Data Dinamis (Dynamic) vs Tipe Data Statis (Static)

1. **Dynamically Typed (Contoh: Python, JavaScript, PHP)**:
   Tipe data ditentukan secara otomatis oleh komputer berdasarkan nilai yang Anda masukkan. Sebuah variabel yang tadinya berisi angka `10`, di baris berikutnya boleh diubah isinya menjadi teks `"Sepuluh"`. Sangat fleksibel dan cepat untuk pemula.
2. **Statically Typed (Contoh: Java, C++, Go, Rust)**:
   Tipe data harus dideklarasikan secara tegas sejak awal dan tidak boleh diubah sembarangan. Jika sebuah variabel dideklarasikan sebagai `int`, ia menolak jika Anda mencoba memasukkan teks string. Sangat aman dan mencegah kesalahan program di level industri besar.

## 6. Tiga Aturan Penting Memberi Nama Variabel

1. **Tidak Boleh Mengandung Spasi**: Gunakan format camelCase (`namaLengkap`) atau snake_case (`nama_lengkap`), bukan `nama lengkap`.
2. **Tidak Boleh Diawali dengan Angka**: Nama `pemain1` diizinkan, tetapi `1pemain` dilarang oleh komputer.
3. **Pilihlah Nama yang Deskriptif**: Hindari menamai variabel dengan satu huruf misterius seperti `x`, `y`, `a`, `b`. Lebih baik tulis `totalHargaBarang` atau `jumlahPengunjung` agar kode Anda mudah dipahami orang lain.
