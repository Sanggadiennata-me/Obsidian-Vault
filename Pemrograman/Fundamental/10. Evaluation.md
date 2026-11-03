#programming 

**Evaluation (Evaluasi Solusi)** adalah pilar kelima dari berpikir komputasional yang bertugas meninjau, menguji, dan memvalidasi apakah solusi atau program yang telah kita buat benar-benar bekerja secara tepat, efisien, aman dari kesalahan (*bug*), dan mampu menyelesaikan masalah awal secara tuntas.

Salah satu pelajaran terpenting bagi pemula adalah: **sebuah program yang dapat berjalan tanpa menampilkan pesan eror, belum tentu merupakan program yang benar**. Bisa saja kodenya berjalan lancar, namun rumus perhitungannya salah atau sistemnya menjadi sangat lambat ketika diberi data dalam jumlah besar.

## 1. Empat Kriteria Evaluasi Program yang Baik

Ketika mengevaluasi algoritma atau program yang sudah Anda buat, periksalah melalui empat tolok ukur berikut:

### A. Kebenaran Fungsional (Correctness)
Apakah program menghasilkan keluaran yang akurat untuk setiap masukan yang diberikan?
- *Contoh*: Jika program kasir menghitung belanjaan Rp100.000 dengan diskon 10%, apakah hasil akhirnya tepat Rp90.000? Jika program menghasilkan Rp110.000 (malah bertambah mahal), berarti terjadi kesalahan logika (*logic error*).

### B. Ketahanan Terhadap Kasus Ekstrem (Edge Cases & Robustness)
Pengguna aplikasi di dunia nyata sering kali melakukan tindakan yang tidak terduga. Evaluasi harus menguji bagaimana sistem merespons skenario-skenario batas:
- Apa yang terjadi jika pengguna mengisi kolom umur dengan angka negatif seperti `-5`?
- Apa yang terjadi jika pengguna mengetik huruf di kolom nomor telepon?
- Apa yang terjadi jika pengguna menekan tombol pembayaran lima kali secara bertubi-tubi dalam tempo 1 detik?
- Apa yang terjadi jika koneksi internet tiba-tiba terputus saat proses transfer bank sedang berjalan?

Program yang tangguh (*robust*) tidak akan langsung mati (*crash*) saat menghadapi kasus ekstrem, melainkan menampilkan pesan peringatan yang ramah dan memandu pengguna.

### C. Efisiensi Sumber Daya (Performance & Complexity)
Apakah solusi Anda menyelesaikan tugas dalam waktu yang wajar dan tidak membebani memori komputer?
- Dua programmer bisa saja menulis program yang hasilnya sama-sama benar. Namun program A selesai dalam 0.05 detik, sementara program B membutuhkan waktu 30 detik untuk memproses data yang sama. Di sinilah evaluasi efisiensi algoritma (analisis kompleksitas) menjadi sangat penting.

### D. Keterbacaan dan Kemudahan Perawatan (Maintainability)
Apakah kode yang Anda tulis rapi, terstruktur, dan mudah dipahami oleh rekan kerja atau bahkan oleh diri Anda sendiri enam bulan dari sekarang?
- Kode yang berantakan, tanpa spasi teratur, dan memakai nama variabel yang tidak jelas (seperti `a`, `b`, `xyz123`) akan sangat menyulitkan ketika di kemudian hari ada fitur baru yang ingin ditambahkan.

## 2. Cara Nyata Melakukan Evaluasi dalam Siklus Pemrograman

Dalam industri perangkat lunak modern, evaluasi dilakukan secara berlapis:
1. **Pengujian Unit (Unit Testing)**: Menulis kode khusus untuk menguji fungsi-fungsi kecil secara otomatis.
2. **Uji Coba Manual (Manual Testing)**: Menjalankan aplikasi secara langsung dan mencoba skenario nyata layaknya pengguna awam.
3. **Peninjauan Kode (Code Review)**: Meminta programmer senior atau rekan tim untuk membaca dan memberi masukan terhadap kode yang baru saja Anda buat.

Evaluasi bukanlah tanda kegagalan atau ketidakmampuan, melainkan bagian alami yang paling penting dari siklus rekayasa perangkat lunak untuk memastikan karya Anda siap digunakan oleh dunia dengan aman.
