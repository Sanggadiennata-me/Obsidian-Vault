#programming 

**Decomposition (Dekomposisi)** adalah teknik berpikir komputasional dengan cara memecah masalah yang besar, kompleks, atau menakutkan menjadi bagian-bagian komponen kecil yang lebih sederhana, terisolasi, dan mudah diselesaikan satu per satu.

Bagi pemula, ketika diminta membuat sebuah program (misalnya aplikasi kasir atau game sederhana), sering kali muncul rasa bingung dan kewalahan: *"Dari mana saya harus mulai?"*. Dekomposisi adalah obat dari kebingungan tersebut.

## 1. Analogi Kehidupan Sehari-hari

Bayangkan Anda diminta membersihkan sebuah rumah besar yang sangat berantakan:
- Jika Anda memandang rumah itu sebagai satu tugas raksasa *"Bersihkan Rumah"*, Anda akan merasa lelah sebelum mulai.
- Namun jika Anda menerapkan dekomposisi, Anda memecahnya menjadi tugas-tugas kecil:
  1. Bersihkan kamar tidur (rapikan kasur, sapu lantai).
  2. Bersihkan ruang tamu (lap meja, tata bantal sofa).
  3. Bersihkan dapur (cuci piring, buang sampah).
  4. Bersihkan kamar mandi.

Dengan membaginya menjadi unit kecil, setiap tugas terasa ringan dan dapat diselesaikan dengan fokus penuh.

## 2. Contoh Dekomposisi dalam Pemrograman: Membuat Game Flappy Bird

Jika seseorang berkata *"Buatlah game Flappy Bird!"*, itu terdengar sulit. Namun mari kita dekomposisi game tersebut menjadi komponen-komponen mandiri:

```text
                           PEMBUATAN GAME FLAPPY BIRD
                                       |
    +------------------+---------------+---------------+------------------+
    |                  |                               |                  |
    v                  v                               v                  v
[1. Karakter]    [2. Pipa Halangan]              [3. Mekanika Tabrakan] [4. Sistem Skor & UI]
- Gambar burung  - Buat pipa atas & bawah        - Cek jika koordinat   - Hitung pipa dilewati
- Efek gravitasi - Celah acak di tengah            burung menyentuh     - Tampilkan angka skor
- Lompat ke atas - Gerakkan pipa ke arah kiri      pipa atau tanah      - Tampilkan Game Over
  saat spasi                                     - Jika kena, hentikan
  ditekan                                          permainan
```

Dengan memecahnya seperti di atas:
1. Hari pertama: Anda cukup fokus membuat burung bisa jatuh dan melompat.
2. Hari kedua: Anda fokus membuat pipa muncul dan bergeser.
3. Hari ketiga: Anda menghubungkan tabrakan burung dengan pipa.
4. Hari keempat: Anda memasang skor dan tampilan Game Over.

Tiba-tiba, proyek yang tadinya terasa mustahil berhasil diselesaikan dengan rapi tanpa stres.

## 3. Keuntungan Menerapkan Dekomposisi

1. **Memudahkan Pembagian Kerja Tim**: Dalam tim pengembang profesional, modul yang sudah didekomposisi dapat dikerjakan secara paralel oleh beberapa programmer sekaligus.
2. **Mempermudah Pencarian Kesalahan (Debugging)**: Jika game tidak bisa melompat, Anda tahu pasti masalahnya ada di modul gravitasi/kontrol burung, sehingga Anda tidak perlu memeriksa modul pipa atau modul skor.
3. **Kode Dapat Digunakan Kembali (Reusability)**: Komponen kecil yang sudah rapi dapat dimanfaatkan kembali untuk proyek lain di masa depan tanpa perlu menulis ulang dari nol.
