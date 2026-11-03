#Terms 

_Hash_ (atau fungsi _hashing_) adalah proses matematika yang mengubah data dalam bentuk apa pun (teks, berkas dokumen, gambar) menjadi deretan karakter acak berpanjang tetap yang bekerja searah dan tidak dapat dikembalikan ke wujud aslinya.

## **Cara Kerja Sederhana**:

Bayangkan sidik jari manusia atau sebuah mesin blender buah. Anda memasukkan sebutir apel utuh ke dalam blender, dan hasilnya adalah segelas jus apel cair halus. Jus tersebut mewakili apel asli Anda. Namun, betapa pun canggihnya teknologi, Anda tidak akan pernah bisa memutar balik waktu untuk merangkai jus apel tadi kembali menjadi sebutir apel utuh. Jika apel diganti dengan melon, rasa dan warna jusnya akan langsung berubah drastis.

**Contoh di Kehidupan Nyata**

- **Penyimpanan Password Aman:** Website yang baik tidak pernah menyimpan password asli Anda (misal `rahasia123`) di databasenya, melainkan menyimpan kode hash-nya. Saat Anda login, sistem hanya mencocokkan hasil hash-nya.
    
- **Integritas Berkas Download:** Saat mengunduh aplikasi besar dari internet, pembuat aplikasi menyediakan kode hash (misal SHA-256). Anda bisa memeriksa apakah berkas yang terunduh sudah disusupi virus atau rusak saat perjalanan.
    
- **Tanda Tangan Digital & Bukti Hukum:** Di dunia digital forensik, hasil hash membuktikan bahwa barang bukti hard disk korban tidak pernah diubah atau dimanipulasi sama sekali oleh penyelidik.
