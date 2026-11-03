#roadmap 

Panduan komprehensif 100% lengkap menguasai Tailwind CSS dari tingkat pemula (awam), menengah, hingga mahir (advanced/master-level). Mencakup filosofi utility-first, sistem warna dan tipografi, box model, layouting flexbox dan grid, desain responsif mobile-first, dark mode, animasi, selector modern, container queries, hingga evolusi Tailwind CSS v4.

---

### Bagian 1: Fundamental & Konsep Awal (Tingkat Pemula)
1. [01. Pengenalan Tailwind CSS](01.%20Pengenalan%20Tailwind%20CSS.md) : Filosofi Utility-First vs Semantic CSS, keunggulan, dan solusi naming fatigue.
2. [02. Instalasi dan Setup](02.%20Instalasi%20dan%20Setup.md) : Integrasi via Play CDN, Tailwind CLI resmi, PostCSS, dan bundler modern Vite/Next.js.
3. [03. Konsep Utility-First](03.%20Konsep%20Utility-First.md) : Anatomi class, sistem skala jarak 4-pixel, arbitrary values `[...]`, dan modifier `!`.

### Bagian 2: Styling Komponen & Tata Letak (Tingkat Menengah)
4. [04. Typography dan Pewarnaan](04.%20Typography%20dan%20Pewarnaan.md) : Skala font, bobot, palet warna 50-950, transparansi `/`, dan teks gradasi modern.
5. [05. Spacing, Sizing, dan Box Model](05.%20Spacing,%20Sizing,%20dan%20Box%20Model.md) : Padding, margin, dimensi `w-` dan `h-`, border, rounded corner, dan shadow bertingkat.
6. [06. Layouting (Flexbox dan Grid)](06.%20Layouting%20(Flexbox%20dan%20Grid).md) : Flex direction, justify, align, spasi gap modern, dan sistem 12-kolom CSS Grid.
7. [07. State Variants dan Interaktivitas](07.%20State%20Variants%20dan%20Interaktivitas.md) : State hover, focus, active, pola parent-child `group-hover`, sibling `peer`, dan micro-interaction.

### Bagian 3: Desain Modern & Arsitektur Lanjutan (Tingkat Lanjut)
8. [08. Responsive Design (Mobile-First)](08.%20Responsive%20Design%20(Mobile-First).md) : Filosofi Mobile-First, 5 breakpoint standar, navigasi adaptif, dan jebakan umum.
9. [09. Dark Mode](09.%20Dark%20Mode.md) : Strategi class vs media query, varian `dark:`, dan skrip JavaScript switch tema.
10. [10. Kustomisasi dan Konfigurasi tailwind.config.js](10.%20Kustomisasi%20dan%20Konfigurasi%20tailwind.config.js.md) : Memperluas tema (`extend`), warna merek kustom, web font Google, dan plugin resmi.
11. [11. Arsitektur Komponen dan Best Practices](11.%20Arsitektur%20Komponen%20dan%20Best%20Practices.md) : Ekstraksi komponen template, batasan direktif `@apply`, helper `cn()`, dan urutan class.

### Bagian 4: Fitur Tingkat Mahir & Masa Depan (Tingkat Master)
12. [12. Animasi dan Transisi Kompleks](12.%20Animasi%20dan%20Transisi%20Kompleks.md) : Keyframe animations (`spin`, `pulse`, `ping`, `bounce`), easing curves, dan skeleton loading.
13. [13. Advanced Selectors dan Modern Pseudo-Classes](13.%20Advanced%20Selectors%20dan%20Modern%20Pseudo-Classes.md) : Selector induk `:has()`, arbitrary child variants `[&>th]`, data attributes, dan pseudo-elements.
14. [14. Efek Visual Lanjutan (Filters, Backdrop, dan Blend Modes)](14.%20Efek%20Visual%20Lanjutan%20(Filters,%20Backdrop,%20dan%20Blend%20Modes).md) : Glassmorphism `backdrop-blur`, perbandingan `drop-shadow` vs `box-shadow`, dan glowing blur orbs.
15. [15. Container Queries (@container)](15.%20Container%20Queries%20(@container).md) : Paradigma baru responsivitas berbasis lebar kotak induk komponen (`@container`, `@md:`).
16. [16. Evolusi Tailwind CSS v4 vs v3](16.%20Evolusi%20Tailwind%20CSS%20v4%20vs%20v3.md) : Mesin baru Oxide (Rust), konfigurasi berbasis CSS murni (`@theme`), dan strategi migrasi masa depan.

---

### Bagian 5: Proyek Praktikum Mandiri (Hands-on Labs)
Seluruh proyek dapat langsung dibuka di browser tanpa setup build tool tambahan:

1. [Praktek 01: Modern SaaS Hero Section](praktek/01-modern-hero-section/index.html) : Halaman landing page lengkap dengan teks gradasi, blur glow, dan layout responsif.
2. [Praktek 02: Dark Mode & Dashboard Cards](praktek/02-dark-mode-dashboard/index.html) : Antarmuka panel admin dengan tombol switch dark mode dan kartu statistik adaptif.
3. [Praktek 03: E-Commerce Product Card](praktek/03-ecommerce-product-card/index.html) : Kartu produk toko online dengan badge diskon berdenyut, selector warna via `:has()`, dan rating.
4. [Praktek 04: Interactive Admin Data Table](praktek/04-interactive-data-table/index.html) : Tabel data admin dengan baris bergaris selang-seling (`even:bg`), badge status, dan pagination.
