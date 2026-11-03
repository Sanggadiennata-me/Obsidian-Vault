#programming 

Gerbang logika **AND** adalah operasi logika yang menuntut **seluruh syarat harus bernilai benar (`true` atau 1)** agar menghasilkan keluaran benar. Jika ada satu saja syarat yang bernilai salah (`false` atau 0), maka seluruh hasil akhir seketika menjadi salah.

Dalam kode pemrograman, logika AND umumnya disimbolkan dengan tanda `&&` (operator logika) atau `&` (operator bitwise), sedangkan dalam Python dituliskan dengan kata `and`.

## 1. Tabel Kebenaran (Truth Table)

Berikut adalah tabel hasil evaluasi logika AND dengan dua masukan:

| Masukan A | Masukan B | Hasil (A AND B) | Penjelasan |
| :---: | :---: | :---: | :--- |
| `0` (false) | `0` (false) | `0` (false) | Kedua syarat salah. |
| `0` (false) | `1` (true)  | `0` (false) | Syarat A salah, syarat B benar. Hasil tetap salah. |
| `1` (true)  | `0` (false) | `0` (false) | Syarat A benar, syarat B salah. Hasil tetap salah. |
| `1` (true)  | `1` (true)  | `1` (true)  | **Hanya kondisi ini yang menghasilkan nilai benar.** |

## 2. Analogi Kehidupan Sehari-hari

Bayangkan proses penarikan uang di mesin ATM:
Mesin ATM hanya akan mengeluarkan uang tunai jika dua kondisi terpenuhi secara bersamaan:
1. Saldo rekening Anda mencukupi nominal penarikan (`true`).
2. Nomor PIN yang Anda ketikkan sesuai dengan data bank (`true`).

Jika saldo Anda banyak tetapi PIN salah, uang tidak akan keluar. Begitu pula jika PIN benar tetapi saldo tidak mencukupi, uang juga tidak akan keluar. Keduanya **wajib benar**.

## 3. Contoh Penggunaan dalam Kode Pemrograman

```javascript
let punyaKartuMember = true;
let totalBelanja = 150000;

// Logika AND: Kedua syarat harus terpenuhi untuk mendapat promo
if (punyaKartuMember === true && totalBelanja >= 100000) {
  console.log("Selamat! Anda berhak mendapatkan diskon 20%.");
} else {
  console.log("Maaf, syarat diskon belum terpenuhi sepenuhnya.");
}
```

## 4. Logika AND dengan Lebih dari Dua Syarat

Logika AND dapat menggabungkan banyak kondisi sekaligus:
```javascript
let syaratKTP = true;
let syaratSKCK = true;
let syaratTesKesehatan = true;

if (syaratKTP && syaratSKCK && syaratTesKesehatan) {
  console.log("Berkas lamaran kerja lengkap dan lolos verifikasi.");
}
```
Jika ada satu saja syarat yang bernilai `false`, maka seluruh pernyataan di atas akan bernilai `false`.
