#programming 

Setiap elemen HTML memiliki perilaku tampilan bawaan yang terbagi menjadi dua kategori utama, yaitu **block element** dan **inline element**. Pemahaman terhadap perilaku ini sangat penting agar kita dapat mengatur bagaimana elemen berinteraksi dengan elemen di sekitarnya.

---

## 1. Perbedaan Mendasar Elemen Block dan Inline

| Karakteristik | Inline Element (Contoh: `<span>`, `<a>`, `<strong>`) | Block Element (Contoh: `<div>`, `<p>`, `<h1>`, `<ul>`) |
| :--- | :--- | :--- |
| **Baris Baru** | Tidak membuat baris baru. Elemen mengalir berdampingan secara horizontal. | Selalu memulai baris baru. Elemen berikutnya otomatis berada di bawahnya. |
| **Lebar (*Width*)** | Sebesar konten teks di dalamnya saja. Tidak bisa diatur dengan `width`. | Melebar 100% memenuhi lebar container induknya secara default. |
| **Tinggi (*Height*)** | Sebesar tinggi teks di dalamnya. Tidak bisa diatur dengan `height`. | Mengikuti tinggi konten, atau dapat ditentukan bebas dengan `height`. |
| **Margin & Padding** | Hanya mempengaruhi jarak horizontal (kiri dan kanan). Nilai vertikal tidak mendorong elemen lain. | Berfungsi penuh pada keempat sisi (atas, kanan, bawah, dan kiri). |

---

## 2. Nilai Properti `display`

Dengan properti `display`, kita dapat mengubah perilaku bawaan elemen sesuai kebutuhan desain antarmuka:

### A. `display: block`
Mengubah elemen inline agar berperilaku seperti block. Sangat berguna misalnya untuk mengubah tautan `<a>` menjadi tombol lebar penuh yang mudah disentuh di layar ponsel.

```css
a.tombol-lebar {
  display: block;
  width: 100%;
  padding: 12px;
  text-align: center;
}
```

### B. `display: inline`
Mengubah elemen block agar mengalir sejajar dengan teks atau elemen lainnya.

```css
li {
  display: inline;
  margin-right: 15px;
}
```

Output:
![](image/displayrole.png)

### C. `display: inline-block` (Jembatan Solusi Terbaik)
Elemen `inline` murni memiliki kelemahan: tidak bisa diatur nilai `width`, `height`, serta `margin-top` / `margin-bottom`-nya. Di sisi lain, elemen `block` selalu memaksa baris baru.

Solusinya adalah **`display: inline-block`**:
- Elemen tetap berjejer horizontal dalam satu baris (seperti inline).
- Elemen dapat diberi ukuran `width`, `height`, serta `margin` dan `padding` vertikal secara leluasa (seperti block).

```css
.nav-badge {
  display: inline-block;
  width: 80px;
  height: 32px;
  padding: 6px;
  text-align: center;
}
```

---

## 3. Menyembunyikan Elemen: `display: none` vs Alternatifnya

Ada tiga cara menyembunyikan elemen di CSS dengan karakteristik yang berbeda:

1. **`display: none`**:
   Elemen dicabut sepenuhnya dari tampilan dan ruang tata letak. Seolah-olah elemen tersebut tidak pernah ada di dalam HTML. Elemen di bawahnya akan naik mengisi tempatnya.
2. **`visibility: hidden`**:
   Elemen menjadi tidak terlihat (transparan), tetapi **ruang fisiknya tetap dipertahankan** di halaman web. Elemen lain tidak akan bergeser.
3. **`opacity: 0`**:
   Elemen menjadi tembus pandang 100%, ruang fisiknya tetap ada, dan elemen tersebut **tetap bisa diklik** atau menerima interaksi kursor mouse.

```css
/* Hilang total tanpa sisa ruang */
.sembunyi-total {
  display: none;
}

/* Transparan tapi ruang tetap ada */
.transparan-beruang {
  visibility: hidden;
}
```

---

## 4. Nilai Modern: `display: flex` dan `display: grid`

Di era CSS modern, penataan tata letak navigasi dan kartu tidak lagi mengandalkan `inline-block` manual karena adanya model layout yang jauh lebih kuat:
- **`display: flex`**: Layout 1 dimensi untuk mendistribusikan item secara fleksibel (dibahas mendalam di [Flexbox](Flexbox.md)).
- **`display: grid`**: Layout 2 dimensi untuk baris dan kolom sekaligus.
