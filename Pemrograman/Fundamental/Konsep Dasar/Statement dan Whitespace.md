#programming 

Memahami bagaimana komputer membedakan satu kalimat instruksi dengan instruksi lainnya serta bagaimana komputer memperlakukan spasi kosong (*whitespace*) adalah keterampilan dasar yang harus dikuasai oleh setiap calon programmer.

## 1. Apa Itu Statement?

Sebuah aplikasi komputer tersusun dari gabungan banyak instruksi tunggal yang saling berhubungan. Di dalam ilmu pemrograman, satu baris instruksi lengkap yang dapat dieksekusi oleh komputer disebut **Statement (Pernyataan)**.

Analogi di dunia nyata adalah instruksi dalam buku resep masakan:
- *"Panaskan minyak di atas wajan dengan api sedang."* -> Satu statement.
- *"Masukkan irisan bawang merah dan tumis hingga harum."* -> Satu statement berikutnya.
- *"Tuangkan 200 mililiter air matang."* -> Satu statement berikutnya.

Contoh statement dalam kode pemrograman:
```javascript
let harga = 25000;                     // Statement 1: Mendeklarasikan variabel harga
let jumlah = 4;                        // Statement 2: Mendeklarasikan variabel jumlah
let total = harga * jumlah;            // Statement 3: Menghitung perkalian
console.log("Total Bayar: " + total);  // Statement 4: Mencetak hasil ke layar
```

Setiap statement harus berupa instruksi yang tuntas dan jelas maksud tujuannya. Komputer mengeksekusi statement-statement ini secara berurutan, baris demi baris, dari atas ke bawah.

## 2. Mengenal Whitespace (Spasi Kosong, Tab, dan Baris Baru)

**Whitespace** adalah karakter kosong yang kita ketikkan pada keyboard namun tidak tampak sebagai huruf atau angka di layar, meliputi:
- Tombol Spasi (Spacebar).
- Tombol Tabulasi (Tab) untuk membuat indentasi menjorok ke dalam.
- Tombol Enter (Newline) untuk berpindah ke baris baru.

Bagaimana komputer memperlakukan karakter kosong ini? Jawabannya terbagi menjadi dua keluarga besar bahasa pemrograman:

### A. Bahasa Bebas Whitespace (C-Style Languages)
Pada bahasa seperti C, C++, Java, PHP, dan JavaScript, komputer pada dasarnya mengabaikan jumlah spasi dan baris baru di luar tanda petik teks. 

Sebagai contoh, ketiga gaya penulisan berikut menghasilkan eksekusi yang **100% sama persis** di mata komputer:

```javascript
// Gaya 1: Rapi dan standar dibaca manusia
let a = 10;
let b = 20;
let hasil = a + b;

// Gaya 2: Dibuat rapat dalam satu baris
let a=10;let b=20;let hasil=a+b;

// Gaya 3: Penuh spasi dan baris kosong berantakan
let      a     = 
    10;
let 
b = 20;
let hasil = a + 
       b;
```

Walaupun komputer tidak mempermasalahkan Gaya 2 atau Gaya 3, manusia yang membacanya akan merasa sangat pusing. Oleh karena itu, kita menggunakan spasi dan indentasi rapi semata-mata demi kenyamanan manusia yang membaca dan merawat kode tersebut.

### B. Bahasa Sensitif Whitespace (Contoh: Python)
Pada bahasa **Python**, whitespace **BUKAN SEKADAR HIASAN**, melainkan aturan sintaksis resmi yang sangat ketat!

Python tidak menggunakan tanda kurung kurawal `{}` untuk menandai blok kode percabangan atau perulangan, melainkan menggunakan **Indentasi (Spasi Menjorok)**:

```python
# Kode Python yang Benar:
nilai = 85

if nilai >= 75:
    print("Selamat!")            # Menjorok 4 spasi ke dalam (bagian dari blok if)
    print("Anda dinyatakan lulus") # Menjorok 4 spasi ke dalam

print("Selesai") # Rata kiri (dijalankan setelah if selesai)
```

Jika di Python Anda salah mengetik jumlah spasi, program akan langsung mogok dan mengeluarkan pesan kesalahan:
`IndentationError: unexpected indent`.

## 3. Aturan Emas Kebersihan Kode (Clean Code Formatting)

Agar kode Anda disukai oleh rekan programmer lain:
1. **Gunakan Indentasi Konsisten**: Pilihlah standar 2 spasi atau 4 spasi untuk setiap blok kode yang menjorok, dan pertahankan konsistensi tersebut di seluruh berkas proyek.
2. **Beri Spasi di Sekitar Operator**: Tulis `total = harga * jumlah` alih-alih `total=harga*jumlah`.
3. **Beri Satu Baris Kosong Antar Blok Logika**: Gunakan tombol Enter sekali untuk memisahkan bagian persiapan variabel, bagian perhitungan utama, dan bagian keluaran (*output*) agar kode tampak bernapas dan tidak sesak.
