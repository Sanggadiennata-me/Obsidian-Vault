#programming 

**Abstraction (Abstraksi)** adalah proses memusatkan perhatian hanya pada informasi yang benar-benar esensial dan penting untuk menyelesaikan suatu masalah, sambil sengaja menyaring dan mengabaikan detail-detail kecil yang tidak relevan.

Di dunia nyata, setiap objek dan situasi memiliki jutaan detail informasi. Jika seorang pemrogram mencoba memasukkan semua detail tersebut ke dalam komputernya, program akan menjadi sangat rumit, lambat, dan membuang-buang memori. Abstraksi adalah seni menyederhanakan kenyataan menjadi model komputasi yang bersih dan efisien.

## 1. Analogi Kehidupan Sehari-hari: Peta Google Maps

Ketika Anda membuka aplikasi Google Maps untuk mencari rute perjalanan dari rumah ke stasiun kereta:
- **Informasi yang Ditampilkan (Esensial)**: Garis jalan raya, persimpangan, rambu belok, nama jalan utama, dan perkiraan waktu tempuh.
- **Informasi yang Sengaja Dihilangkan (Abstraksi)**: Warna cat pagar setiap rumah yang Anda lewati, jenis pohon di tepi jalan, merk aspal jalan raya, atau nama pemilik warung di pinggir gang.

Apakah Google Maps tidak tahu detail-detail tersebut? Mungkin saja tahu. Namun informasi tersebut sengaja diabaikan karena sama sekali tidak membantu Anda menemukan jalan ke stasiun. Menyertakan detail yang tidak perlu justru membuat peta sulit dibaca dan membingungkan pengguna.

## 2. Contoh Abstraksi dalam Pemrograman: Pemodelan Data Pengguna

Bayangkan Anda diminta membuat sistem informasi akademik untuk mencatat nilai rapor siswa di sekolah.

Seorang siswa di dunia nyata memiliki ratusan atribut:
- Nama lengkap
- Nomor Induk Siswa (NISN)
- Nilai ujian matematika
- Warna sepatu favorit
- Tinggi badan dalam milimeter
- Merk pasta gigi yang digunakan
- Nama kucing peliharaan di rumah

Menerapkan abstraksi berarti memilih atribut yang **hanya relevan** dengan kebutuhan sistem rapor:

```text
+------------------------------------------+
|          OBJEK DATA SISWA (RAPOR)        |
+------------------------------------------+
| [RELEVAN - DISIMPAN]                     |
| - NISN          : 202611001              |
| - Nama          : Aryanda Pratama        |
| - Kelas         : 10 IPA 1               |
| - Nilai Ujian   : 88                     |
| - Kehadiran     : 95%                    |
+------------------------------------------+
| [TIDAK RELEVAN - DIABSTRAKSIKAN/DIBUANG] |
| - Warna sepatu  (Tidak perlu)            |
| - Pasta gigi    (Tidak perlu)            |
| - Kucing        (Tidak perlu)            |
+------------------------------------------+
```

Dengan melakukan abstraksi, struktur data aplikasi menjadi sangat ringkas, hemat ruang memori, dan mudah diproses oleh database.

## 3. Abstraksi Tingkat Fungsi (Black Box Concept)

Abstraksi juga diterapkan pada cara kita menggunakan kode. Anda tidak perlu tahu cara kerja bagian dalam sebuah fungsi rumit untuk dapat menggunakannya:

```javascript
// Contoh: Menghitung akar kuadrat dari 25
let hasil = Math.sqrt(25);
console.log(hasil); // 5
```

Anda tidak perlu tahu bagaimana rumus algoritma Newton-Raphson atau manipulasi biner di dalam prosesor bekerja untuk menghitung akar kuadrat. Anda cukup tahu:
- Masukan yang diberikan adalah angka `25`.
- Keluaran yang dihasilkan adalah angka `5`.

Fungsi tersebut bertindak seperti kotak hitam (*black box*). Konsep abstraksi inilah yang memungkinkan programmer membangun aplikasi raksasa dengan memanfaatkan ribuan fungsi dan modul pustaka (*library*) yang sudah dibuat oleh programmer lain tanpa harus memahami jutaan baris kode internalnya.
