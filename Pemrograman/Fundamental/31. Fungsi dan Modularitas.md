#programming 

Saat Anda mulai menulis program yang berukuran ratusan hingga ribuan baris, Anda akan sering menemui situasi di mana Anda harus melakukan pekerjaan yang sama persis di berbagai tempat berbeda. Menulis ulang rangkaian baris kode yang sama berulang-ulang bukan hanya melelahkan, tetapi juga menjadi sumber malapetaka ketika di kemudian hari rumus tersebut perlu diubah.

Untuk mengatasi masalah ini, programmer menggunakan konsep **Fungsi (Function)** dan **Modularitas**.

## 1. Apa Itu Fungsi? (Analogi Mesin Blender)

Bayangkan sebuah mesin blender di dapur Anda:
- Blender adalah sebuah alat khusus yang dirancang untuk satu tugas spesifik: membuat jus buah.
- **Input (Parameter / Argumen)**: Anda memasukkan potongan buah mangga, es batu, dan sedikit air ke dalam blender.
- **Proses (Badan Fungsi)**: Anda menekan tombol daya. Pisau blender berputar cepat menghancurkan buah di dalam wadah tertutup. Anda tidak perlu memikirkan bagaimana sirkuit dinamo motor berputar.
- **Output (Return Value / Nilai Balik)**: Dari corong blender mengalir segelas jus mangga yang lembut dan segar, siap diminum atau diolah lebih lanjut.

Kapan pun Anda atau anggota keluarga Anda ingin membuat jus apel, jus jeruk, atau jus alpukat, Anda **tidak perlu merakit blender baru dari nol**. Anda cukup menggunakan blender yang sama, cukup ganti bahan buah yang dimasukkan ke dalamnya.

Itulah fungsi di dalam pemrograman: **sebuah blok kode mandiri yang diberi nama, dirancang untuk menyelesaikan tugas tertentu, dan dapat dipanggil berkali-kali kapan pun dibutuhkan**.

## 2. Anatomi Dasar Sebuah Fungsi

Berikut adalah struktur pembuatan dan pemanggilan fungsi sederhana dalam JavaScript:

```javascript
// 1. MEMBUAT FUNGSI (Deklarasi)
function hitungTotalBayar(hargaBarang, jumlahBeli, persenDiskon) {
  let subtotal = hargaBarang * jumlahBeli;
  let potongan = subtotal * (persenDiskon / 100);
  let totalAkhir = subtotal - potongan;

  // Mengembalikan hasil perhitungan keluar
  return totalAkhir; 
}

// 2. MENGGUNAKAN FUNGSI (Pemanggilan / Invocation)
let belanjaanAryanda = hitungTotalBayar(50000, 2, 10);
console.log("Total Belanja Aryanda : Rp " + belanjaanAryanda); 
// Hasil: Rp 90000 (100.000 diskon 10.000)

let belanjaanBudi = hitungTotalBayar(100000, 3, 20);
console.log("Total Belanja Budi    : Rp " + belanjaanBudi); 
// Hasil: Rp 240000 (300.000 diskon 60.000)
```

Empat komponen dalam kode di atas:
1. **Nama Fungsi (`hitungTotalBayar`)**: Label pengenal agar fungsi bisa dipanggil kembali.
2. **Parameter (`hargaBarang`, `jumlahBeli`, `persenDiskon`)**: Variabel wadah penampung masukan yang dibutuhkan oleh fungsi.
3. **Badan Fungsi (Statement di dalam kurung `{}`)**: Rumus logika pemrosesan data.
4. **Return Value (`return totalAkhir`)**: Perintah khusus yang melempar hasil akhir keluar agar dapat disimpan ke dalam variabel atau dicetak.

## 3. Fungsi dengan Return Value vs Fungsi Prosedur (Tanpa Return)

- **Fungsi dengan Return Value**: Menghitung sesuatu dan **menyerahkan hasilnya kembali** kepada pemanggilnya agar bisa diolah lebih lanjut (seperti contoh fungsi hitung total belanja di atas).
- **Fungsi Prosedur (Tanpa Return)**: Hanya menjalankan serangkaian tindakan tanpa mengembalikan nilai (misalnya fungsi untuk sekadar menampilkan pesan sambutan di layar):

```javascript
function sapaPengguna(namaPengguna) {
  console.log("====================================");
  console.log("Halo, " + namaPengguna + "! Selamat datang kembali.");
  console.log("====================================");
}

// Panggil kapan pun ada pengguna baru yang membuka dasbor
sapaPengguna("Aryanda");
sapaPengguna("Siti");
```

## 4. Prinsip Emas DRY: Don't Repeat Yourself

Salah satu moto paling terkenal di dunia rekayasa perangkat lunak adalah **DRY (Don't Repeat Yourself)**, yang berarti: *"Jangan pernah mengulang-ulang penulisan kode yang sama di berbagai tempat"*.

### Mengapa Mengulang Kode Itu Berbahaya?
Bayangkan Anda menulis rumus perhitungan pajak 11% secara manual di 20 berkas program yang berbeda:
- Suatu hari, pemerintah mengubah tarif pajak dari 11% menjadi 12%.
- Anda terpaksa membuka satu per satu ke-20 berkas tersebut, mencari barisnya, dan mengubah angkanya secara manual.
- Jika Anda melewatkan satu berkas saja karena lupa, aplikasi Anda akan menghasilkan data keuangan yang korup dan tidak sinkron.

### Solusi dengan Modularitas:
Buatlah **satu fungsi terpusat**:
```javascript
function hitungPajak(nominal) {
  return nominal * 0.12; // Cukup ubah angka di satu tempat ini saja!
}
```
Seluruh 20 berkas cukup memanggil fungsi `hitungPajak()`. Ketika tarif berubah di masa depan, Anda cukup mengubah satu baris di dalam fungsi tersebut, dan seluruh 20 berkas akan otomatis terperbarui secara instan.
