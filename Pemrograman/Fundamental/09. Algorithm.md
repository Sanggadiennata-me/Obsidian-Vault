#programming 

**Algorithm (Perancangan Algoritma)** adalah tahap dalam berpikir komputasional di mana kita menyusun serangkaian langkah instruksi logis, terurut, pasti, dan tidak ambigu untuk menyelesaikan suatu tugas atau memecahkan permasalahan dari awal hingga selesai.

Setelah sebuah masalah didekomposisi, polanya dikenali, dan informasinya diabstraksikan, langkah selanjutnya adalah merancang instruksi kerja yang dapat dieksekusi oleh komputer secara otomatis.

## 1. Lima Syarat Wajib Algoritma yang Baik (Kriteria Knuth)

Ilmuwan komputer legendaris Donald Knuth menetapkan lima kriteria utama yang harus dipenuhi oleh setiap algoritma yang valid:

1. **Input (Masukan)**: Algoritma memiliki nol atau lebih data masukan yang diberikan dari luar sebelum proses dimulai.
2. **Output (Keluaran)**: Algoritma harus menghasilkan minimal satu keluaran yang merupakan solusi dari masalah yang dikerjakan.
3. **Definiteness (Kepastian & Tidak Ambigu)**: Setiap instruksi langkah harus jelas, terdefinisi secara presisi, dan tidak menimbulkan multitafsir. Instruksi seperti *"tambahkan sedikit garam"* adalah instruksi ambigu; instruksi *"tambahkan 5 gram garam"* adalah instruksi yang pasti.
4. **Finiteness (Keterbatasan / Titik Henti)**: Algoritma harus memiliki titik awal dan titik akhir. Setelah menjalankan sejumlah langkah yang terhingga, algoritma **harus berhenti**, bukan berputar tanpa henti (*infinite loop*).
5. **Effectiveness (Efektivitas)**: Setiap langkah yang ditulis harus cukup sederhana sehingga benar-benar mungkin dikerjakan dan diselesaikan dalam batas waktu yang wajar.

## 2. Dua Cara Menyajikan Algoritma

Sebelum menuliskan algoritma ke dalam bahasa pemrograman nyata, ada dua teknik utama yang digunakan programmer untuk merancang dan mendiskusikan alur logika:

### A. Diagram Alir Visual (Flowchart)
Flowchart menggambarkan urutan proses menggunakan bagan visual dengan simbol-simbol standar internasional:
- **Kapsul Oval (Terminator)**: Menandai titik `Mulai (Start)` dan titik `Selesai (End)`.
- **Persegi Panjang (Process)**: Menandai tindakan pemrosesan atau perhitungan nilai matematika (misal: `hitung total = harga * jumlah`).
- **Jajar Genjang (Input / Output)**: Menandai pembacaan data masukan atau penampilan hasil ke layar.
- **Belah Ketupat (Decision / Keputusan)**: Menandai titik percabangan kondisi dengan dua jalur panah keluar: `Ya (True)` atau `Tidak (False)`.
- **Garis Panah (Flowline)**: Menunjukkan arah aliran langkah demi langkah.

### B. Kode Semu (Pseudocode)
Pseudocode adalah cara menuliskan algoritma menggunakan bahasa manusia (bahasa Indonesia atau Inggris) yang disusun menyerupai struktur kode pemrograman tanpa terikat aturan titik koma atau sintaksis bahasa tertentu.

Contoh Pseudocode Menentukan Kelulusan Siswa:
```text
ALGORITMA CekKelulusan:
  INPUT nilaiSiswa DARI pengguna

  IF nilaiSiswa >= 75 THEN
    OUTPUT "Selamat, Anda Dinyatakan Lulus!"
  ELSE
    OUTPUT "Maaf, Anda Harus Mengikuti Ujian Remedial."
  END IF
SELESAI
```

Keunggulan pseudocode adalah siapapun bisa membacanya dan memahaminya secara instan, baik programmer Python, programmer JavaScript, maupun orang awam yang bukan programmer sekalipun.

## 3. Mengapa Komputer Membutuhkan Algoritma yang Presisi?

Manusia memiliki akal sehat (*common sense*) untuk mengisi celah informasi yang kurang. Jika Anda menyuruh teman Anda: *"Tolong belikan nasi goreng di warung depan"*, teman Anda otomatis tahu bahwa dia harus memakai sandal, membawa uang, menyeberang jalan dengan hati-hati, memesan, membayar, dan membawa pulang bungkusan nasi tersebut.

Komputer tidak memiliki akal sehat. Jika Anda tidak menginstruksikan langkah memeriksa saldo atau langkah menyimpan data, komputer tidak akan melakukannya secara ajaib. Setiap detail langkah harus didefinisikan secara sadar di dalam algoritma Anda.
