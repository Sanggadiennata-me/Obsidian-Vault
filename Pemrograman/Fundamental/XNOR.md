#programming 

Gerbang logika **XNOR** adalah singkatan dari **Exclusive NOR** (kebalikan dari [XOR](XOR.md)). Dalam ilmu komputer, gerbang ini sering juga disebut sebagai **Gerbang Kesetaraan (Equivalence Gate)** atau pembanding identitas.

Jika gerbang XOR menghasilkan nilai benar saat masukan berbeda, maka gerbang XNOR adalah kebalikannya: **XNOR hanya menghasilkan nilai benar (`true` atau 1) apabila KEDUA MASUKANNYA MEMILIKI NILAI YANG SAMA PERSIS**.

Secara matematis, rumusnya adalah:
```text
XNOR = NOT (A XOR B) atau !(A ^ B)
```

## 1. Tabel Kebenaran (Truth Table)

| Masukan A | Masukan B | Hasil Logika XOR `(A ^ B)` | Hasil Logika XNOR `!(A ^ B)` | Penjelasan |
| :---: | :---: | :---: | :---: | :--- |
| `0` (false) | `0` (false) | `0` | **`1` (true)** | **Nilai sama (keduanya salah), hasil benar.** |
| `0` (false) | `1` (true)  | `1` | **`0` (false)** | Nilai berbeda, hasil salah. |
| `1` (true)  | `0` (false) | `1` | **`0` (false)** | Nilai berbeda, hasil salah. |
| `1` (true)  | `1` (true)  | `0` | **`1` (true)** | **Nilai sama (keduanya benar), hasil benar.** |

## 2. Analogi Kehidupan Sehari-hari

Bayangkan formulir pendaftaran akun baru pada situs web:
Untuk mencegah salah ketik, formulir meminta Anda mengisi dua kolom:
1. Kolom Kata Sandi.
2. Kolom Konfirmasi Kata Sandi.

Sistem hanya akan mengizinkan pendaftaran berhasil (XNOR bernilai `true`) jika:
- Karakter pada kolom pertama **sama persis** dengan karakter pada kolom kedua.

Jika kedua kolom berbeda, maka sistem akan menolak formulir tersebut karena tidak setara.

## 3. Contoh Penggunaan dalam Kode Pemrograman

Dalam pemrograman tingkat tinggi, logika kesetaraan XNOR pada dasarnya identik dengan operator pembanding kesetaraan langsung (`===`):

```javascript
let statusLampuKiri = true;  // Saklar A menyala
let statusLampuKanan = true; // Saklar B menyala

// Logika XNOR: Bernilai true jika kedua saklar berada pada posisi yang sama
let sinkron = (statusLampuKiri === statusLampuKanan);

if (sinkron) {
  console.log("Status kedua saklar selaras dan seimbang.");
} else {
  console.log("Status saklar tidak selaras: satu menyala dan satu padam.");
}
```

## 4. Peran XNOR dalam Perangkat Keras Komputer

Pada sirkuit prosesor komputer (ALU - Arithmetic Logic Unit), gerbang XNOR digunakan sebagai modul **Digital Comparator** (Pembanding Angka Digital). Prosesor menggunakan susunan gerbang XNOR untuk membandingkan miliaran bit data dalam sekejap mata guna mengetahui apakah dua blok data dalam memori bernilai identik atau tidak.
