#roadmap 

### Bagian 1: Fundamental & Sistem Kolom
1. [01. Pengenalan Bulma CSS](01.%20Pengenalan%20Bulma%20CSS.md) : Filosofi CSS-only murni, perbandingan dengan Bootstrap & Tailwind, dan sintaks manusiawi `is-*` / `has-*`.
2. [02. Instalasi dan Setup](02.%20Instalasi%20dan%20Setup.md) : Integrasi via CDN resmi jsDelivr, package manager NPM, dan keterikatan Font Awesome.
3. [03. Sistem Kolom Flexbox (Columns)](03.%20Sistem%20Kolom%20Flexbox%20(Columns).md) : Kolom alami Flexbox `.columns` & `.column`, ukuran pecahan (`is-half`, `is-one-third`), sistem 12 kolom, dan perataan vertikal `is-vcentered`.

### Bagian 2: Tipografi, Form, & Tata Letak Dasar
4. [04. Modifiers, Warna, dan Tipografi](04.%20Modifiers,%20Warna,%20dan%20Tipografi.md) : Spektrum warna semantik (`is-primary`, `is-info`, `is-light`), pasangan `title` dan `subtitle`, serta utilitas perataan teks.
5. [05. Elemen UI Inti (Buttons, Tags, Boxes, dan Notifications)](05.%20Elemen%20UI%20Inti%20(Buttons,%20Tags,%20Boxes,%20dan%20Notifications).md) : Tombol melengkung `is-rounded`, status putar `is-loading`, kotak kartu putih `.box`, lencana `.tag`, dan kotak pengumuman `.notification`.
6. [06. Formulir dan Kontrol Input](06.%20Formulir%20dan%20Kontrol%20Input.md) : Struktur hierarki `.field`, `.label`, `.control`, input berikon (`has-icons-left`), grup tombol gabung (`has-addons`), dan dropdown `.select`.
7. [07. Tata Letak Panggung (Hero, Section, dan Container)](07.%20Tata%20Letak%20Panggung%20(Hero,%20Section,%20dan%20Container).md) : Spanduk utama `.hero.is-medium`, pembungkus konten `.section`, pembatas layar `.container`, dan penutup halaman `.footer`.

### Bagian 3: Komponen Lanjutan & Kustomisasi Modern
8. [08. Komponen Kompleks (Navbar, Card, dan Media Object)](08.%20Komponen%20Kompleks%20(Navbar,%20Card,%20dan%20Media%20Object).md) : Navigasi responsif dengan skrip burger vanilla JS, struktur lengkap `.card`, dan pola avatar `.media`.
9. [09. Komponen Interaktif CSS-Only (Modal, Dropdown, dan Tabs)](09.%20Komponen%20Interaktif%20CSS-Only%20(Modal,%20Dropdown,%20dan%20Tabs).md) : Mengendalikan modal dialog via class `.is-active`, dropdown murni hover (`is-hoverable`), dan navigasi tab.
10. [10. Kustomisasi Tema dengan Sass dan CSS Variables](10.%20Kustomisasi%20Tema%20dengan%20Sass%20dan%20CSS%20Variables.md) : Fitur Bulma v1.0 dengan variabel CSS asli (`--bulma-*`), dark mode bawaan (`data-theme="dark"`), dan kompilasi SCSS modular.
11. [11. Arsitektur Komponen dan Best Practices](11.%20Arsitektur%20Komponen%20dan%20Best%20Practices.md) : Memadukan Bulma dengan React/Vue/Blade, memisahkan logika JavaScript, dan optimasi bundle produksi.

---

### Bagian 4: Proyek Praktikum Mandiri (Hands-on Labs)
Seluruh proyek dapat langsung dibuka di browser tanpa perlu proses build terpisah:

1. [Praktek 01: Startup Landing Page](praktek/01-startup-landing-page/index.html) : Halaman depan perusahaan rintisan dengan hero banner mencolok, navbar interaktif, 3 kartu layanan flexbox, dan newsletter box.
2. [Praktek 02: SaaS Admin Panel](praktek/02-saas-dashboard/index.html) : Panel dashboard modern dengan kartu ringkasan level, tabel data interaktif, jendela modal tambah data, dan dropdown hover.
