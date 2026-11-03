#programming 

Bagi orang yang baru pertama kali belajar pemrograman, melihat layar komputer dipenuhi teks merah berisi pesan kesalahan (*error message*) sering kali memicu rasa cemas, panik, atau bahkan membuat seseorang merasa tidak berbakat menjadi programmer.

Hal pertama yang harus Anda tanamkan di dalam pikiran Anda adalah:

> **Mendapatkan pesan error adalah hal yang 100% normal dan merupakan bagian tak terpisahkan dari aktivitas setiap programmer di dunia.**

Bahkan programmer paling senior di perusahaan teknologi raksasa seperti Google, Apple, atau Netflix pun melihat puluhan pesan error setiap hari. Pesan error bukanlah vonis bahwa Anda gagal, melainkan **petunjuk jujur dari komputer** yang memberi tahu Anda secara presisi di baris mana letak ketidaksesuaian instruksi yang Anda berikan.

## 1. Tiga Kategori Utama Error dalam Pemrograman

Tidak semua error itu sama. Secara umum, kesalahan dalam kode terbagi menjadi tiga jenis:

```text
+------------------------------------------------------------------------+
|                          TIGA MACAM ERROR KODE                         |
+-------------------+----------------------------------------------------+
| 1. Syntax Error   | Pelanggaran tata bahasa kode (typo, tanda kurung)  |
|                   | -> Program langsung mogok sebelum sempat berjalan. |
+-------------------+----------------------------------------------------+
| 2. Runtime Error  | Macet di tengah jalan saat program dieksekusi      |
|                   | -> Terjadi saat membagi dengan nol / data hilang.  |
+-------------------+----------------------------------------------------+
| 3. Logic Error    | Program lancar tanpa pesan merah, tapi hasil salah |
| (Bug Tersembunyi) | -> Rumus terbalik, operator logika salah.          |
+-------------------+----------------------------------------------------+
```

### A. Syntax Error (Kesalahan Tata Bahasa)
Terjadi ketika Anda melanggar aturan baku penulisan bahasa pemrograman, seperti salah ketik kata kunci (*typo*), lupa menutup tanda petik teks, atau tanda kurung kurawal yang kurang satu pasang.

- *Contoh di Python*:
  ```python
  # KESALAHAN: Lupa tanda titik dua (:) di akhir pernyataan if
  if nilai >= 75
      print("Lulus")
  ```
  Komputer akan langsung menolak menjalankan berkas dengan pesan: `SyntaxError: expected ':'`.

### B. Runtime Error (Kesalahan Waktu Berjalan)
Kode Anda secara tata bahasa sudah benar, sehingga komputer berhasil mulai menjalankannya. Namun di tengah-tengah proses eksekusi, komputer menabrak kondisi yang mustahil dilakukan sehingga aplikasi seketika berhenti mendadak (*crash*).

- *Contoh Kasus*:
  - Mencoba membagi angka dengan nol (`10 / 0`).
  - Mengakses variabel yang nilainya belum pernah dibuat (*null* atau *undefined*).
  - Mencoba membuka berkas dokumen yang ternyata sudah dihapus dari harddisk.
  - Sambungan koneksi internet tiba-tiba terputus saat mengambil data.

### C. Logic Error (Kesalahan Logika / Bug Tersembunyi)
Ini adalah jenis error yang paling berbahaya dan paling menantang untuk ditemukan. Mengapa? Karena **komputer sama sekali tidak memunculkan pesan error apa pun**. Program berjalan mulus dari awal sampai akhir, namun **hasil keluarannya salah**.

- *Contoh Kasus*:
  ```javascript
  let harga = 100000;
  let diskon = 10000;

  // KESALAHAN LOGIKA: Harusnya dikurangi (-), tapi programmer salah ketik (+)
  let totalBayar = harga + diskon; 

  console.log("Total yang harus dibayar: Rp " + totalBayar);
  // Hasil: Rp 110.000 (Malah bertambah mahal!)
  ```
  Komputer tidak tahu bahwa niat Anda adalah memberikan diskon. Komputer hanya patuh menjumlahkan kedua angka tersebut.

## 2. Cara Membaca Pesan Error Tanpa Panik

Ketika terminal atau konsol browser Anda memunculkan pesan error panjang berwarna merah, jangan langsung menutup layar. Bacalah secara tenang dengan mencari dua informasi kunci:

1. **Nama dan Tipe Error**: Biasanya terletak di baris paling atas atau paling bawah (misalnya `TypeError: Cannot read property 'nama' of undefined`).
2. **Lokasi Berkas dan Nomor Baris**: Carilah baris teks yang menyebutkan nama berkas Anda, misalnya `at main.js:14:5`. Angka `14` memberi tahu Anda bahwa masalah terjadi tepat di **baris ke-14**.

Cukup buka berkas tersebut, arahkan kursor ke baris 14, dan periksa variabel atau tanda baca di sekitar baris itu.

## 3. Tiga Teknik Debugging Sederhana untuk Pemula

**Debugging** adalah seni mencari akar penyebab masalah dalam kode dan memperbaikinya.

### A. Print Debugging (Metode Paling Populer)
Gunakan perintah cetak (`console.log()` di JavaScript atau `print()` di Python) di beberapa titik strategis dalam kode Anda untuk mengintip isi variabel saat program sedang berjalan:

```javascript
console.log("Nilai variabel harga saat ini: ", harga);
console.log("Apakah kondisi if berhasil dimasuki? Ya!");
```
Dengan melihat teks apa saja yang muncul di layar, Anda bisa melacak sampai di titik mana kode Anda masih berjalan normal dan di titik mana perhitungannya mulai kacau.

### B. Membaca Ulang Alur Baris Demi Baris
Jadilah layaknya komputer: baca kode Anda secara perlahan dari baris pertama ke bawah. Tuliskan di secarik kertas nilai setiap variabel di setiap putaran loop untuk melihat apakah perubahannya sudah sesuai rencana.

### C. Rubber Duck Debugging (Metode Bebek Karet)
Teknik psikologis legendaris di kalangan insinyur perangkat lunak:
- Letakkan sebuah benda mati di meja Anda (misalnya boneka bebek karet, cangkir kopi, atau miniatur mainan).
- Jelaskan kepada benda mati tersebut kalimat demi kalimat tentang apa yang ingin dilakukan oleh kode Anda dan bagaimana alurnya berjalan.
- Sering kali, saat Anda sedang berusaha menjelaskan alur tersebut dengan kata-kata sederhana, otak Anda tiba-tiba akan menyadari: *"Tunggu sebentar... kenapa di baris 8 saya malah mengubah nilai variabel ini? Pantas saja hasilnya salah!"*.
