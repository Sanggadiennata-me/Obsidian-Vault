#programming 

Salah satu keunggulan terbesar komputer dibanding manusia adalah kemampuannya melakukan pekerjaan yang sama persis ribuan bahkan jutaan kali dengan kecepatan luar biasa tanpa pernah merasa lelah, bosan, atau kehilangan ketelitian.

**Logika Perulangan (Looping)** adalah mekanisme dalam pemrograman yang menginstruksikan komputer untuk menjalankan suatu blok kode secara berulang-ulang selama suatu kondisi tertentu masih terpenuhi.

![Diagram Alir Perulangan](image/perulangan.png)

## 1. Mengapa Kita Membutuhkan Perulangan?

Bayangkan Anda diminta menulis teks *"Saya berjanji akan belajar dengan tekun"* sebanyak 100 kali.

Tanpa perulangan, Anda harus mengetik perintah cetak sebanyak 100 baris secara manual:
```javascript
// Cara yang Sangat Melelahkan dan Tidak Efisien:
console.log("Saya berjanji akan belajar dengan tekun");
console.log("Saya berjanji akan belajar dengan tekun");
console.log("Saya berjanji akan belajar dengan tekun");
// ... dan 97 baris lainnya ...
```

Jika jumlahnya bertambah menjadi 10.000 kali, kode Anda akan membengkak menjadi ribuan baris dan sangat rawan salah ketik.

Dengan perulangan, Anda cukup menuliskan instruksinya **sekali saja**, lalu memberi tahu komputer berapa kali proses tersebut harus diulang:

```javascript
// Cara Efisien Menggunakan Perulangan:
for (let i = 1; i <= 100; i++) {
  console.log(i + ". Saya berjanji akan belajar dengan tekun");
}
```

Komputer akan mengeksekusinya dalam hitungan milidetik.

## 2. Tiga Komponen Wajib dalam Setiap Perulangan

Agar sebuah perulangan dapat berjalan dengan selamat dan teratur, harus ada tiga elemen penting:

1. **Titik Awal (Inisialisasi)**: Menentukan dari angka berapa hitungan dimulai (misalnya `i = 1`).
2. **Kondisi Berhenti (Kondisi Evaluasi)**: Syarat batas yang diperiksa sebelum setiap putaran dimulai. Selama syarat ini bernilai `true`, perulangan lanjut berjalan. Jika berubah menjadi `false`, perulangan berhenti (misalnya `i <= 100`).
3. **Pembaruan Nilai (Step / Increment / Decrement)**: Perubahan angka hitungan di setiap akhir putaran agar hitungan semakin mendekati batas berhenti (misalnya `i++` yang menambah nilai `i` sebesar 1).

## 3. Dua Jenis Utama Perulangan

### A. Perulangan For (For Loop)
Digunakan ketika Anda **sudah mengetahui secara pasti jumlah putaran** yang ingin dilakukan sejak awal.

```javascript
// Contoh: Menghitung mundur peluncuran roket dari 5 ke 1
for (let hitungan = 5; hitungan >= 1; hitungan--) {
  console.log("Hitungan: " + hitungan);
}
console.log("Roket Meluncur!");
```

### B. Perulangan While (While Loop)
Digunakan ketika Anda **belum tahu pasti berapa kali putaran akan terjadi**, karena perulangan bergantung pada situasi dinamis atau tindakan pengguna.

Analogi di kehidupan nyata: *"Makanlah selama piring Anda belum kosong"* atau *"Teruslah mengocok dadu sampai Anda mendapatkan angka 6"*.

```javascript
let nyawaPemain = 3;

while (nyawaPemain > 0) {
  console.log("Permainan sedang berlangsung. Sisa nyawa: " + nyawaPemain);
  // Simulasikan pemain terkena rintangan
  nyawaPemain--;
}

console.log("Game Over! Seluruh nyawa pemain telah habis.");
```

## 4. Pengendali Khusus: `break` dan `continue`

Kadang kita perlu mengubah alur putaran sebelum kondisi utamanya selesai:

### `break` (Berhenti Total dan Keluar)
Menghentikan seluruh perulangan seketika dan langsung melompat keluar dari blok loop:
```javascript
// Mencari angka 7 dalam antrean, lalu langsung berhenti
for (let angka = 1; angka <= 10; angka++) {
  if (angka === 7) {
    console.log("Angka 7 ditemukan! Hentikan pencarian.");
    break; // Perulangan putaran 8, 9, 10 tidak akan pernah dijalankan
  }
  console.log("Memeriksa angka: " + angka);
}
```

### `continue` (Lewati Putaran Saat Ini)
Melewati sisa instruksi pada putaran saat ini dan langsung melompat ke putaran berikutnya:
```javascript
// Mencetak angka ganjil saja dengan melewati angka genap
for (let angka = 1; angka <= 5; angka++) {
  if (angka % 2 === 0) {
    continue; // Lewati angka genap, langsung lanjut ke angka berikutnya
  }
  console.log("Angka Ganjil: " + angka);
}
// Hasil cetak: 1, 3, 5
```

## 5. Bahaya Terbesar: Infinite Loop (Perulangan Tak Terhingga)

Salah satu kesalahan paling umum bagi pemula adalah lupa menambahkan pembaruan nilai (`increment`), sehingga kondisi berhenti tidak pernah tercapai (`true` selamanya):

```javascript
// CONTOH KODE BERBAHAYA (JANGAN DITIRU!):
let hitungan = 1;

while (hitungan <= 5) {
  console.log("Hitungan: " + hitungan);
  // Lupa menulis: hitungan++;
}
```

Karena nilai `hitungan` akan selalu bernilai 1 (selamanya `<= 5`), komputer akan terus berputar mencetak teks tanpa henti. Akibatnya:
- Penggunaan CPU melonjak drastis hingga 100%.
- Tab browser atau aplikasi menjadi macet (*freeze* / *hang*) dan harus dipaksa berhenti (*Force Quit*).

> [!WARNING] Aturan Emas Perulangan
> Setiap kali Anda membuat perulangan `while`, selalu pastikan ada instruksi di dalam badan perulangan yang secara bertahap mengubah kondisi menuju titik berhenti (`false`).
