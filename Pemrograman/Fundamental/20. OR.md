#programming 

Gerbang logika **OR** memiliki aturan yang jauh lebih fleksibel dibanding AND. Logika OR akan menghasilkan nilai benar (`true` atau 1) apabila **minimal salah satu dari syarat masukan bernilai benar**. Satu-satunya kondisi yang menghasilkan nilai salah (`false` atau 0) adalah ketika **seluruh masukan bernilai salah**.

Dalam kode pemrograman, logika OR umumnya disimbolkan dengan tanda `||` (garis pipa ganda) atau `|` (operator bitwise), sedangkan dalam bahasa Python dituliskan dengan kata `or`.

## 1. Tabel Kebenaran (Truth Table)

Berikut adalah tabel hasil evaluasi logika OR dengan dua masukan:

| Masukan A | Masukan B | Hasil (A OR B) | Penjelasan |
| :---: | :---: | :---: | :--- |
| `0` (false) | `0` (false) | `0` (false) | **Hanya kondisi ini yang menghasilkan salah (karena tidak ada yang benar).** |
| `0` (false) | `1` (true)  | `1` (true)  | Salah satu benar (B), maka hasil akhir benar. |
| `1` (true)  | `0` (false) | `1` (true)  | Salah satu benar (A), maka hasil akhir benar. |
| `1` (true)  | `1` (true)  | `1` (true)  | Keduanya benar, hasil akhir tetap benar. |

## 2. Analogi Kehidupan Sehari-hari

Bayangkan saat Anda ingin menonton film di bioskop:
Petugas bioskop akan mengizinkan Anda masuk ke dalam studio jika:
- Anda membawa selembar tiket cetak fisik (`true`), **ATAU**
- Anda memperlihatkan barcode e-ticket di layar aplikasi ponsel (`true`).

Jika Anda memiliki tiket fisik saja, Anda boleh masuk. Jika Anda memiliki tiket digital di HP saja, Anda juga boleh masuk. Jika Anda membawa keduanya pun tidak masalah. Anda hanya akan dilarang masuk jika **sama sekali tidak memiliki tiket fisik maupun tiket digital** (`false` keduanya).

## 3. Contoh Penggunaan dalam Kode Pemrograman

```javascript
let punyaTiketFisik = false;
let punyaTiketDigital = true;

// Logika OR: Minimal satu kondisi terpenuhi sudah cukup
if (punyaTiketFisik || punyaTiketDigital) {
  console.log("Akses diberikan: Selamat menikmati pemutaran film!");
} else {
  console.log("Akses ditolak: Anda belum memiliki tiket resmi.");
}
```

## 4. Logika OR dengan Banyak Syarat

Logika OR sangat sering digunakan pada sistem pembayaran aplikasi toko online (e-commerce):
```javascript
let bayarTransfer = false;
let bayarKartuKredit = false;
let bayarEWallet = true;

// Pengguna cukup memilih salah satu metode yang tersedia
if (bayarTransfer || bayarKartuKredit || bayarEWallet) {
  console.log("Metode pembayaran valid. Silakan selesaikan transaksi.");
}
```
Selama ada minimal satu pilihan yang bernilai `true`, pesanan dapat segera diproses.
