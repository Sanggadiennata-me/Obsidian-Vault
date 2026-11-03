#programming 

Dalam dunia elektronika digital, **gerbang logika (logic gate)** adalah sirkuit fisik transistor yang memproses tegangan listrik biner (0 volt mewakili nilai `0/false`, sedangkan 5 volt mewakili nilai `1/true`). 

Namun dalam dunia perangkat lunak (*software development*), kita tidak berurusan dengan kawat tembaga atau transistor. Bagi pemrogram, **gerbang logika adalah aturan kombinasi logika Boolean** yang digunakan untuk menggabungkan beberapa syarat keputusan menjadi satu kesatuan evaluasi.

## 1. Rangkuman 7 Gerbang Logika Utama

Setiap gerbang logika memiliki tabel kebenaran (*truth table*) dan karakteristik unik:

| Gerbang Logika | Simbol Kode (Logical) | Karakteristik Utama | Analogi Nyata |
| :--- | :--- | :--- | :--- |
| **[AND](AND.md)** | `&&` | Bernilai `true` HANYA jika **semua syarat bernilai true**. | Penarikan uang di ATM: kartu bank valid DAN nomor PIN harus benar. |
| **[OR](OR.md)** | `\|\|` | Bernilai `true` jika **minimal salah satu syarat bernilai true**. | Masuk konser: menunjukkan tiket fisik gelang ATAU tiket digital di ponsel. |
| **[NOT](NOT.md)** | `!` | Pembalik nilai tunggal: mengubah `true` menjadi `false`, dan sebaliknya. | Saklar pembalik: jika TIDAK sedang hujan, anak-anak boleh bermain di luar. |
| **[NAND](NAND.md)** | `!(A && B)` | Not AND: kebalikan dari AND. Bernilai `false` hanya jika semua input true. | Saklar pengaman mesin: mesin mati jika tombol aktif tetapi pelindung belum terkunci. |
| **[NOR](NOR.md)** | `!(A \|\| B)` | Not OR: kebalikan dari OR. Bernilai `true` hanya jika semua input false. | Sistem alarm gedung: gedung aman jika sensor asap 0 dan sensor panas 0. |
| **[XOR](XOR.md)** | `^` | Exclusive OR: Bernilai `true` HANYA jika **kedua syarat bernilai berbeda**. | Paket menu hemat: konsumen memilih minuman es teh ATAU es kopi (tidak boleh keduanya). |
| **[XNOR](XNOR.md)** | `!(A ^ B)` | Exclusive NOR: Bernilai `true` jika **kedua syarat bernilai sama persis**. | Verifikasi kata sandi: isi kolom password dan kolom konfirmasi password harus kembar identik. |

## 2. Operator Logika (Logical) vs Operator Bitwise (Bitwise)

Bagi pemula, penting untuk mengetahui perbedaan dua kategori operator ini pada bahasa pemrograman seperti JavaScript, C++, Java, dan PHP:

### A. Operator Logika (Logical Operators)
Bekerja pada tingkat kondisi keputusan (Boolean) dan digunakan di dalam pernyataan `if`:
- `&&` : Logika AND
- `||` : Logika OR
- `!`  : Logika NOT

```javascript
// Contoh Logika Keputusan:
if (punyaKartuMember === true && totalBelanja >= 100000) {
  console.log("Selamat, Anda berhak mendapatkan diskon khusus!");
}
```

> [!NOTE] Fitur Short-Circuit Evaluation
> Pada operator logika `&&` dan `||`, komputer menggunakan teknik evaluasi jalan pintas (*short-circuit*). Pada kondisi `A && B`, jika `A` bernilai `false`, komputer tidak akan repot-repot memeriksa `B` karena hasilnya sudah pasti `false`. Begitu juga pada `A || B`, jika `A` sudah `true`, komputer langsung memutuskan hasil `true`.

### B. Operator Bitwise (Bitwise Operators)
Bekerja langsung pada tingkat bit bilangan biner (angka 0 dan 1):
- `&` : Bitwise AND
- `|` : Bitwise OR
- `^` : Bitwise XOR
- `~` : Bitwise NOT

Pelajari pendalaman masing-masing gerbang pada catatan rincian berikut:
1. [AND](AND.md)
2. [OR](OR.md)
3. [NOT](NOT.md)
4. [NAND](NAND.md)
5. [NOR](NOR.md)
6. [XOR](XOR.md)
7. [XNOR](XNOR.md)
