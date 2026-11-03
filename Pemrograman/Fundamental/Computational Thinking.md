#programming 

**Computational Thinking (Berpikir Komputasional)** adalah cara berpikir terstruktur untuk merumuskan masalah dan solusinya sedemikian rupa sehingga solusi tersebut dapat dijalankan secara efektif oleh komputer maupun manusia.

Banyak pemula salah mengira bahwa belajar pemrograman berarti langsung menghafal kode dan sintaksis bahasa tertentu. Padahal, sebelum mengetik satu baris kode pun, keterampilan paling berharga dari seorang programmer adalah **bagaimana membedah masalah besar yang rumit menjadi langkah-langkah logis yang sederhana**.

## 1. Lima Pilar Utama Computational Thinking

Computational Thinking terdiri dari 5 metode berpikir yang saling melengkapi dalam menyelesaikan suatu masalah:

```text
                               +-----------------------------+
                               |     MASALAH BESAR RUMIT     |
                               +-----------------------------+
                                              |
        +-------------------------------------+-------------------------------------+
        |                                                                           |
        v                                                                           v
+------------------------+                                             +------------------------+
| 1. DECOMPOSITION       |                                             | 2. PATTERN RECOGNITION |
| Memecah masalah besar  |                                             | Menemukan kesamaan     |
| menjadi bagian kecil   |                                             | pola dari pengalaman   |
+------------------------+                                             +------------------------+
        |                                                                           |
        +-------------------------------------+-------------------------------------+
                                              |
                                              v
                               +-----------------------------+
                               | 3. ABSTRACTION              |
                               | Menyaring data penting dan  |
                               | membuang detail tak relevan |
                               +-----------------------------+
                                              |
                                              v
                               +-----------------------------+
                               | 4. ALGORITHM DESIGN         |
                               | Merancang instruksi langkah |
                               | demi langkah yang teratur   |
                               +-----------------------------+
                                              |
                                              v
                               +-----------------------------+
                               | 5. EVALUATION               |
                               | Menguji, mencari bug, dan   |
                               | memastikan solusi efektif   |
                               +-----------------------------+
```

1. **[Decomposition (Dekomposisi)](Decomposition.md)**: Memecah suatu masalah besar atau sistem yang rumit menjadi potongan-potongan tugas kecil yang jauh lebih mudah dikelola.
2. **[Pattern Recognition (Pengenalan Pola)](Pattern%20Recognition.md)**: Mengamati keteraturan, kemiripan, atau kesamaan antara masalah saat ini dengan masalah lain yang pernah diselesaikan sebelumnya.
3. **[Abstraction (Abstraksi)](Abstraction.md)**: Memusatkan perhatian hanya pada informasi yang benar-benar esensial dan relevan bagi pemecahan masalah, serta sengaja mengabaikan detail kecil yang tidak berpengaruh.
4. **[Algorithm Design (Perancangan Algoritma)](Algorithm.md)**: Menyusun serangkaian langkah instruksi logis yang berurutan, pasti, dan tidak ambigu untuk menyelesaikan masalah.
5. **[Evaluation (Evaluasi Solusi)](Evaluation.md)**: Menguji apakah solusi yang dibuat sudah benar, efisien, aman dari kesalahan (*bug*), dan mampu menangani skenario batas (*edge cases*).

## 2. Contoh Kasus Terpadu: Merancang Aplikasi Pemesanan Makanan Online

Agar lebih mudah dibayangkan, mari kita terapkan kelima pilar ini untuk merancang aplikasi pemesanan makanan:

- **Dekomposisi**: Masalah "membuat aplikasi pesan makanan" dipecah menjadi: sistem daftar menu, sistem keranjang belanja, modul perhitungan ongkir, dan modul pembayaran.
- **Pengenalan Pola**: Proses pembayaran di aplikasi makanan memiliki pola yang persis sama dengan pembayaran di aplikasi belanja toko online (ada total bayar, pilihan rekening, dan bukti transfer).
- **Abstraksi**: Untuk menampilkan daftar restoran di layar ponsel, kita hanya perlu menampilkan nama restoran, foto menu utama, harga, dan rating. Kita tidak perlu memusingkan warna seragam koki di dapur restoran atau merk kompor yang dipakai, karena detail tersebut tidak relevan bagi pembeli.
- **Algoritma**: Alur proses dibuat runtut: 1. Pilih menu -> 2. Tambah ke keranjang -> 3. Hitung jarak alamat -> 4. Tampilkan total biaya -> 5. Bayar -> 6. Notifikasi pesanan ke dapur restoran.
- **Evaluasi**: Sebelum aplikasi dirilis ke publik, diuji coba: apa yang terjadi jika pembeli memesan saat restoran sedang tutup? Apa yang terjadi jika saldo pembeli kurang?

Pelajari penjelasan mendalam dari setiap metode pada catatan khusus berikut:
- [Decomposition (Dekomposisi)](Decomposition.md)
- [Pattern Recognition (Pengenalan Pola)](Pattern%20Recognition.md)
- [Abstraction (Abstraksi)](Abstraction.md)
- [Algorithm (Algoritma)](Algorithm.md)
- [Evaluation (Evaluasi)](Evaluation.md)
