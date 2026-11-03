# Catatan Praktikum Tailwind CSS

Folder ini berisi kumpulan proyek antarmuka web modern menggunakan Tailwind CSS. Seluruh berkas HTML menggunakan Tailwind Play CDN sehingga Anda dapat langsung membukanya di peramban web (browser) favorit Anda tanpa perlu setup Node.js terlebih dahulu.

---

## Daftar Proyek Latihan

### 1. [01-Modern SaaS Hero Section](01-modern-hero-section/index.html)
* **Fokus Materi**:
  - Sticky header dengan efek blur kaca (`backdrop-blur-md bg-white/80`).
  - Efek teks gradasi modern (`bg-gradient-to-r bg-clip-text text-transparent`).
  - Tombol aksi dengan efek bayangan warna dan micro-interaction (`hover:-translate-y-0.5 active:scale-95`).
  - Tata letak responsif penuh (Mobile, Tablet, Desktop) menggunakan prefix `sm:`, `md:`, dan `lg:`.
* **Pratinjau Desain**:
  ![](../image/praktek_tailwind_hero.png)

---

### 2. [02-Dark Mode & Dashboard Cards](02-dark-mode-dashboard/index.html)
* **Fokus Materi**:
  - Pengaturan Tailwind Dark Mode dengan strategi class (`darkMode: 'class'`).
  - Tombol switcher JavaScript interaktif untuk mengganti tema gelap dan terang.
  - Kartu statistik modular dengan warna teks dan background adaptif (`bg-white dark:bg-slate-900`).
  - Grid responsif 4 kolom yang otomatis menyesuaikan ukuran layar (`grid-cols-1 sm:grid-cols-2 lg:grid-cols-4`).
* **Pratinjau Desain**:
  ![](../image/praktek_tailwind_dashboard.png)
