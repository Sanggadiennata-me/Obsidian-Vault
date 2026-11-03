# Praktek Mandiri HTML5

Folder ini berisi 2 proyek latihan mandiri untuk mempraktikkan konsep HTML5 semantik dan formulir interaktif secara langsung. Seluruh proyek menggunakan kode HTML standar W3C murni tanpa dependensi library eksternal, sehingga dapat langsung dibuka di peramban web modern.

---

## 1. Praktek 01: Website Portofolio Pribadi Semantik
- **Lokasi Berkas**: `01-personal-portfolio/index.html`
- **Konsep Kunci**:
  - Kerangka dokumen semantik penuh: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, dan `<footer>`.
  - Navigasi internal menggunakan bookmark anchor ID (`href="#tentang"`).
  - Penyajian gambar profil semantik dengan `<figure>` dan `<figcaption>`.
  - Format teks kutipan menggunakan `<blockquote>` dan penandaan penting `<strong>`, `<em>`, serta `<mark>`.
  - Format tanggal mesin yang terstandarisasi menggunakan elemen `<time datetime="...">`.
  - Tabel data riwayat pendidikan terstruktur dengan `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, dan penggabungan sel `colspan`.
  - Formulir kontak dasar dengan pembungkus `<fieldset>` dan `<legend>`.

## 2. Praktek 02: Formulir Pendaftaran Konferensi Teknologi
- **Lokasi Berkas**: `02-event-registration-form/index.html`
- **Konsep Kunci**:
  - Ragam tipe input modern HTML5: `text`, `email`, `tel`, `number`, `date`, `url`, `file`, `radio`, dan `checkbox`.
  - Fitur autocomplete daftar pilihan native peramban menggunakan `<datalist>`.
  - Menu pilihan dropdown bertingkat menggunakan `<select>` dan `<optgroup>`.
  - Validasi formulir bawaan peramban tanpa JavaScript: atribut `required`, `pattern` (ekspresi reguler), `minlength`, `maxlength`, `min`, dan `max`.
  - Elemen interaktif bawaan: blok lipat tanya-jawab `<details>` dan `<summary>`.
  - Jendela pop-up modal dialog native HTML5 menggunakan elemen `<dialog>` dengan metode `showModal()` dan `close()`.

---

## Cara Menjalankan Proyek
1. Buka pengelola berkas (File Explorer).
2. Masuk ke folder laboratorium yang ingin diuji.
3. Klik ganda pada berkas `index.html` untuk langsung melihat hasilnya di peramban web (Google Chrome, Firefox, Safari, atau Edge).
