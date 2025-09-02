# Fullscreen Slider Web (HTML/CSS/JS)

Slider fullscreen ringan dengan animasi halus, thumbnail sinkron, dan kontrol Next/Prev. Dibangun tanpa framework untuk kemudahan kustomisasi dan performa cepat.

## Fitur
- Animasi transisi next/prev berbasis CSS.
- Thumbnail sinkron dengan slide aktif.
- Struktur HTML sederhana, mudah menambah slide.
- Responsif dasar dan dukungan `prefers-reduced-motion`.
- Tanpa dependensi pihak ketiga.

## Struktur Proyek
├─ index.html
├─ style.css
├─ reset.css
├─ script.js
└─ img/

## Penggunaan
### Menambah Slide Baru (konten utama)
Tambahkan blok berikut ke dalam `.slider .list` di `index.html`:
### Menambah Thumbnail
Tambahkan elemen berikut ke `.slider .thumbnail`:
Pastikan urutan item di `.list` dan `.thumbnail` konsisten, karena JavaScript memutar keduanya secara sinkron saat navigasi.

## Cara Kerja Singkat
- HTML:
  - `.slider` berisi `.list` (slide utama), `.thumbnail` (kumpulan thumbnail), tombol navigasi `#prev` dan `#next`, serta indikator `.loading-bar`.
- CSS:
  - `reset.css` melakukan normalisasi gaya, termasuk dukungan `prefers-reduced-motion`.
  - `style.css` mengatur layout fullscreen, tipografi, dan animasi transisi (keyframes untuk next/prev, show/hide detail, dan pergerakan thumbnail).
- JavaScript (`script.js`):
  - Tombol `#next` memanggil `initSlider("next")`: memindahkan item pertama ke akhir (`appendChild`).
  - Tombol `#prev` memanggil `initSlider("prev")`: memindahkan item terakhir ke awal (`prepend`).
  - Menambahkan class `.slider.next`/`.slider.prev` untuk memicu animasi CSS, lalu melepasnya setelah durasi transisi.

## Kredit
- Desain/implementasi: @kevinwahyu

