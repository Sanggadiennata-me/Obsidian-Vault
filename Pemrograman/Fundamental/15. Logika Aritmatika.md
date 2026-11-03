#programming 

Dalam pemrograman, hampir setiap aplikasi yang kita buat memerlukan perhitungan matematika, mulai dari menghitung total keranjang belanja, kalkulasi pengurangan nyawa musuh dalam game, hingga perhitungan rumus algoritma rekomendasi.

Operator aritmatika adalah simbol-simbol khusus yang digunakan untuk melakukan operasi matematika dasar pada data angka (integer maupun float).

## 1. Simbol Operator Aritmatika Standar

Hampir seluruh bahasa pemrograman (Python, JavaScript, PHP, C++, Java, Go, Rust) menggunakan kumpulan simbol aritmatika yang seragam:

| Operator | Nama Operasi | Contoh Kode | Hasil Perhitungan |
| :--- | :--- | :--- | :--- |
| `+` | Penjumlahan | `10 + 5` | `15` |
| `-` | Pengurangan | `10 - 4` | `6` |
| `*` | Perkalian (menggunakan tanda bintang) | `6 * 7` | `42` |
| `/` | Pembagian | `20 / 4` | `5` |
| `%` | Modulus (Sisa Pembagian Bulat) | `10 % 3` | `1` |
| `**` | Eksponen / Pangkat (Python/JS modern) | `2 ** 3` | `8` (artinya 2 pangkat 3) |

> [!NOTE] Perhatikan Simbol Perkalian dan Pembagian
> Komputer tidak menggunakan tanda `x` atau tanda titik `.` untuk perkalian karena huruf `x` dapat tertukar dengan nama variabel. Komputer selalu menggunakan tanda bintang `*` untuk perkalian dan garis miring `/` untuk pembagian.

## 2. Memahami Operator Modulus (`%`) Secara Mudah

Bagi pemula, operator modulus (`%`) sering kali membingungkan karena disangka sebagai perhitungan persentase diskon. Padahal dalam ilmu komputer, `%` adalah operasi untuk **mencari sisa dari pembagian bilangan bulat**.

### Analogi Membagikan Permen
Bayangkan Anda memiliki **7 butir permen** yang ingin dibagikan secara adil kepada **3 orang anak**:
- Masing-masing anak mendapatkan **2 butir permen** (karena 2 x 3 = 6).
- Masih ada **1 butir permen** yang tersisa di tangan Anda yang tidak bisa dibagikan lagi secara utuh.
- Sisa 1 butir inilah yang disebut modulus: `7 % 3 = 1`.

Contoh lainnya:
- `10 % 2 = 0` (karena 10 dibagi 2 habis pas 5, tidak ada sisa sama sekali).
- `9 % 4 = 1` (karena 4 x 2 = 8, sisanya adalah 1).
- `5 % 10 = 5` (karena 5 tidak cukup dibagi 10, sehingga seluruh 5 menjadi sisa).

### Di Mana Modulus Digunakan dalam Dunia Nyata?
1. **Membedakan Bilangan Genap dan Ganjil**:
   Setiap bilangan genap jika dibagi 2 pasti bersisa 0, sedangkan bilangan ganjil bersisa 1:
   ```javascript
   if (angka % 2 === 0) {
     console.log("Angka Genap");
   } else {
     console.log("Angka Ganjil");
   }
   ```
2. **Konversi Satuan Waktu (Detik ke Menit dan Jam)**:
   Jika durasi sebuah video adalah 125 detik:
   - Menit = `125 / 60` (didapat 2 menit bulat).
   - Sisa Detik = `125 % 60` (didapat sisa 5 detik).
   - Jadi durasinya adalah 2 menit 5 detik.
3. **Mewarnai Baris Tabel Selang-Seling (Zebra Pattern)**:
   Baris dengan nomor urut `indeks % 2 === 0` diberi warna abu-abu muda, sedangkan baris lainnya putih.

## 3. Urutan Prioritas Perhitungan (KABATAKU / PEMDAS)

Sama seperti matematika di sekolah, komputer mengeksekusi operasi aritmatika berdasarkan aturan hierarki yang ketat:

1. **Kurung `()`**: Operasi di dalam tanda kurung selalu dikerjakan paling awal.
2. **Pangkat `**`**: Dikerjakan berikutnya.
3. **Perkalian `*`, Pembagian `/`, dan Modulus `%`**: Memiliki tingkat prioritas yang sama, dieksekusi berurutan dari kiri ke kanan.
4. **Penjumlahan `+` dan Pengurangan `-`**: Dikerjakan paling akhir.

Perhatikan contoh berikut:
```text
Perhitungan: 5 + 2 * 3
```
- **Cara yang Salah**: `5 + 2 = 7`, lalu `7 * 3 = 21` (Salah!).
- **Cara Komputer Bekerja**: Komputer mendahulukan perkalian `2 * 3 = 6`, baru menambahkan `5 + 6 = 11` (Benar!).

Jika Anda ingin penjumlahan dikerjakan lebih dulu, gunakan tanda kurung:
```text
Perhitungan: (5 + 2) * 3 = 7 * 3 = 21
```

> [!TIP] Praktik Terbaik Pemula
> Jika Anda ragu mengenai urutan mana yang akan dieksekusi lebih dulu oleh komputer, selalu gunakan tanda kurung `()` secara eksplisit. Hal ini membuat niat kode Anda sangat jelas dan mencegah terjadinya bug perhitungan yang tersembunyi.

## 4. Operator Singkat (Shorthand Assignment)

Dalam pemrograman, kita sangat sering mengubah nilai variabel berdasarkan nilai lamanya sendiri, misalnya menambah skor pemain saat mendapatkan koin:

```javascript
// Cara panjang:
skor = skor + 10;

// Cara singkat (Shorthand):
skor += 10;
```

Tersedia shorthand serupa untuk seluruh operator:
- `x += 5` (artinya `x = x + 5`)
- `x -= 3` (artinya `x = x - 3`)
- `x *= 2` (artinya `x = x * 2`)
- `x /= 4` (artinya `x = x / 4`)
- `x++` atau `++x` (menambah nilai variabel sebanyak 1, sering digunakan pada perulangan)
- `x--` atau `--x` (mengurangi nilai variabel sebanyak 1)
