#programming 

Jika sebuah program hanya bisa menjalankan perintah lurus dari atas ke bawah tanpa pernah mengambil keputusan, maka program tersebut akan sangat kaku dan tidak berguna di dunia nyata.

**Percabangan (Conditional Branching / Decision Making)** adalah struktur kendali logika yang memungkinkan komputer memilih jalur eksekusi kode yang berbeda berdasarkan terpenuhi atau tidaknya suatu kondisi tertentu.

Analogi di dunia nyata adalah persimpangan jalan:
*"Jika lampu menyala hijau, silakan jalan terus; namun jika lampu menyala merah, Anda wajib berhenti."*

## 1. Tiga Bentuk Utama Percabangan `If`

### A. Percabangan Tunggal (`if`)
Digunakan ketika kita hanya ingin menjalankan suatu aksi jika syaratnya terpenuhi, dan tidak melakukan apa pun jika syaratnya tidak terpenuhi:

```javascript
let totalBelanja = 150000;

// Jika belanja di atas 100 ribu, berikan bonus stiker
if (totalBelanja >= 100000) {
  console.log("Selamat, Anda mendapatkan bonus 1 buah stiker koleksi!");
}

console.log("Terima kasih telah berbelanja.");
```

Jika `totalBelanja` hanya 50.000, komputer langsung melompati blok `if` dan langsung mencetak ucapan terima kasih.

### B. Percabangan Dua Jalur (`if - else`)
Digunakan ketika ada dua skenario alternatif yang saling bertolak belakang: jika syarat benar lakukan A, jika syarat salah lakukan B:

```javascript
let nilaiUjian = 68;
let batasLulus = 75;

if (nilaiUjian >= batasLulus) {
  console.log("Status: LULUS! Pertahankan prestasi Anda.");
} else {
  console.log("Status: TIDAK LULUS. Silakan mendaftar ujian perbaikan.");
}
```

Komputer menjamin bahwa hanya satu dari dua blok di atas yang akan dieksekusi.

### C. Percabangan Bertingkat Banyak Jalur (`if - else if - else`)
Digunakan ketika ada lebih dari dua kemungkinan pilihan kondisi yang harus diuji secara bertahap:

```javascript
let skor = 82;

if (skor >= 85) {
  console.log("Predikat: A (Sangat Memuaskan)");
} else if (skor >= 70) {
  console.log("Predikat: B (Baik)");
} else if (skor >= 60) {
  console.log("Predikat: C (Cukup)");
} else {
  console.log("Predikat: D (Perlu Pendampingan Khusus)");
}
```

Komputer akan memeriksa kondisi dari atas ke bawah:
- Pertama, mengecek apakah `82 >= 85`? (`false`).
- Kedua, mengecek cabang berikutnya: apakah `82 >= 70`? (`true`).
- Begitu menemukan kondisi yang bernilai `true`, komputer langsung mengeksekusi blok Predikat B, dan secara cerdas **mengabaikan seluruh cabang `else if` di bawahnya**.

## 2. Percabangan Pilihan Tetap (`switch - case`)

Ketika Anda memiliki banyak sekali cabang pilihan yang menguji satu variabel dengan nilai-nilai pasti (seperti menu tombol mesin ATM), struktur `switch - case` sering kali lebih rapi dan nyaman dibaca dibanding rentetan `if - else if` yang panjang:

```javascript
let pilihanMenu = 2;

switch (pilihanMenu) {
  case 1:
    console.log("Menampilkan Saldo Rekening Anda...");
    break;
  case 2:
    console.log("Membuka Menu Penarikan Uang Tunai...");
    break;
  case 3:
    console.log("Membuka Menu Transfer Antarbank...");
    break;
  default:
    console.log("Nomor menu yang Anda pilih tidak tersedia di mesin ini.");
}
```

> [!IMPORTANT] Jangan Lupakan Kata Kunci `break`
> Pada struktur `switch - case`, kata kunci `break` berfungsi sebagai rem penahan. Jika Anda lupa menulis `break`, komputer akan mengalami kondisi yang disebut *fall-through*, yaitu mengeksekusi seluruh baris case di bawahnya tanpa memeriksa kondisi lagi.

## 3. Percabangan Bersarang (Nested If)

Sebuah blok percabangan juga dapat diletakkan di dalam blok percabangan lainnya:

```javascript
let punyaTiket = true;
let usia = 15;

if (punyaTiket === true) {
  // Pengecekan tingkat kedua di dalam
  if (usia >= 17) {
    console.log("Boleh masuk ke studio film kategori dewasa.");
  } else {
    console.log("Tiket valid, namun usia Anda belum mencukupi untuk film kategori ini.");
  }
} else {
  console.log("Silakan membeli tiket di loket terlebih dahulu.");
}
```

Gunakan percabangan bersarang dengan bijak. Terlalu banyak lapisan sarang (misalnya 4 atau 5 tingkat ke dalam) akan membuat kode menjadi sulit dibaca dan rawan membingungkan pengembang lain.
