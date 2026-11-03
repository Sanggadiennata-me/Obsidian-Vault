#roadmap 

Fundamental yang harus dipelajari sebelum melangkah ke bahasa pemrograman yang lebih spesifik. Konsep-konsep dasar ini berlaku universal di semua bahasa, baik Python, JavaScript, PHP, Java, C++, Go, maupun bahasa lainnya.

## Tahap 1: Mindset & Cara Kerja Komputer
1. [Apa itu program](Apa%20itu%20program.md) : Memahami bahwa program adalah sekumpulan instruksi terstruktur untuk memecahkan masalah, bukan sekadar barisan kode acak.
2. [Apa Itu Programmer](Apa%20Itu%20Programmer.md) : Peran nyata programmer sebagai pemecah masalah (*problem solver*) yang menerjemahkan kebutuhan manusia menjadi logika komputer.
3. [Bagaimana Komputer Bekerja](Bagaimana%20Komputer%20Bekerja.md) : Membangun gambaran mental tentang bagaimana prosesor, memori RAM, dan instruksi saling berinteraksi.
4. [Input > Process > Output](Input%20%3E%20Process%20%3E%20Output.md) : Siklus IPO sebagai fondasi utama di balik setiap aplikasi dan fitur perangkat lunak di dunia.

## Tahap 2: Berpikir Komputasional & Algoritma
1. [Computational Thinking](Computational%20Thinking.md) : Metode membedah masalah besar dan rumit menjadi langkah-langkah logis yang mudah dikelola:
   - [Decomposition](Decomposition.md) : Memecah masalah besar menjadi bagian-bagian kecil yang terisolasi.
   - [Pattern Recognition](Pattern%20Recognition.md) : Menemukan kesamaan pola dari masalah sebelumnya agar tidak perlu membuat solusi dari nol.
   - [Abstraction](Abstraction.md) : Memusatkan perhatian hanya pada data esensial dan mengabaikan detail yang tidak relevan.
   - [Algorithm](Algorithm.md) : Merancang instruksi langkah demi langkah yang pasti melalui Flowchart dan Pseudocode.
   - [Evaluation](Evaluation.md) : Menguji kebenaran, efisiensi, dan ketahanan solusi terhadap berbagai skenario ekstrem (*edge cases*).
2. [Algoritma](Algoritma.md) : Lima syarat utama algoritma yang baik (Finiteness, Definiteness, Effectiveness, Input, Output) dan penerapannya dalam kehidupan nyata.

## Tahap 3: Logika Pemrograman & Gerbang Logika
1. [Logika](Logika.md) : Menjembatani cara berpikir manusia yang lentur dengan cara kerja komputer yang serba pasti (True/False):
   - [Penalaran Deduktif](Deduktif.md) : Menarik kesimpulan pasti dari aturan umum yang sudah terbukti benar.
   - [Penalaran Induktif](Induktif.md) : Mengambil kesimpulan berdasarkan pola pengamatan nyata di lapangan.
2. [Logika Aritmatika](Logika%20Aritmatika.md) : Operasi matematika dasar, rahasia operator modulus (`%`) sisa bagi, urutan prioritas KABATAKU, dan operator penugasan singkat.
3. [Logika Perbandingan](Logika%20Perbandingan.md) : Membandingkan nilai (`==`, `!=`, `>`, `<`, `>=`, `<=`), perbedaan vital antara penugasan `=` dan pengujian `==`, serta nilai Boolean.
4. [Logika Perulangan](Logika%20Perulangan.md) : Mengulang aksi otomatis menggunakan `for` dan `while`, 3 komponen perulangan, pengendali `break` / `continue`, dan pencegahan *infinite loop*.
5. [Gerbang Logika](Gerbang%20Logika.md) : Menggabungkan banyak syarat keputusan menggunakan aljabar Boolean:
   - [AND](AND.md) : Bernilai true hanya jika semua syarat bernilai benar (`&&`).
   - [OR](OR.md) : Bernilai true jika minimal salah satu syarat bernilai benar (`||`).
   - [NOT](NOT.md) : Pembalik nilai kebenaran tunggal (`!`).
   - [NAND](NAND.md) : Kebalikan dari AND (Not AND).
   - [NOR](NOR.md) : Kebalikan dari OR (Not OR).
   - [XOR](XOR.md) : Bernilai true hanya jika kedua syarat memiliki nilai yang berbeda (`^`).
   - [XNOR](XNOR.md) : Bernilai true hanya jika kedua syarat memiliki nilai yang sama persis.

## Tahap 4: Blok Bangunan Kode & Sintaksis Dasar
1. [Sintaksis dan Case Sensitive](Konsep%20Dasar/Sintaksis%20dan%20Case%20Sensitive.md) : Aturan tata bahasa kode, tanda baca titik koma, dan keharusan memperhatikan huruf kapital.
2. [Statement dan Whitespace](Konsep%20Dasar/Statement%20dan%20Whitespace.md) : Anatomi kalimat instruksi program dan perbedaan perlakuan spasi antar bahasa (C-style vs Python).
3. [Keyword dan Pseudocode](Konsep%20Dasar/Keyword%20dan%20Pseudocode.md) : Kata kunci pesanan sistem dan cara merancang alur program dalam format teks yang ramah manusia.
4. [Variabel dan Tipe Data](Variabel%20dan%20Tipe%20Data.md) : Analogi toples berlabel di memori, 4 tipe data primitif (Integer, Float, String, Boolean), dan konvensi penamaan variabel.
5. [Percabangan](Percabangan.md) : Mengambil keputusan dinamis menggunakan struktur `if`, `else if`, `else`, dan `switch-case`.
6. [Fungsi dan Modularitas](Fungsi%20dan%20Modularitas.md) : Analogi mesin blender, parameter masukan, return value, dan prinsip Don't Repeat Yourself (DRY).

## Tahap 5: Menghadapi Error & Mentalitas Pemula
1. [Tipe Error dan Debugging](Tipe%20Error%20dan%20Debugging.md) : Mengapa pesan error adalah hal normal, 3 macam error (Syntax Error, Runtime Error, Logic Error), cara membaca pesan terminal, dan seni *debugging*.
