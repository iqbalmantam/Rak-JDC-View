# Rak JDC View

Peta kapasitas rak gudang JDC dalam **tampak samping**. Satu file HTML (`index.html`), tanpa server dan tanpa instalasi.

## Tampilan

- **Tampak samping**: satu strip per rak, tiap kotak satu posisi pallet, tinggi tumpukan = jumlah level. Bisa dilihat dari barat atau timur, diwarnai menurut status atau jumlah level.
- **Potongan melintang**: profil tinggi antar rak per posisi utara-selatan, atau siluet tertinggi.
- **3D isometrik**: gambaran umum (pelengkap).
- **Rekap PP**: PP existing, PP baru, dan pembanding dengan tabel PP di sheet.

Kotak abu-abu di Excel dibaca sebagai racking baru.

## Memakai file Excel sendiri

Klik **Muat file Excel** atau seret file `.xlsx` ke halaman. Sheet yang namanya memuat "exist" dipakai lebih dulu; kalau tidak ada, sheet pertama.

Aplikasi membaca kode rak (A01-D09) di baris 11 dan 49, angka level di baris 15-88, dan warna sel untuk menandai racking baru. Layout file harus sama dengan `Rak_JDC.xlsx`. Pembaca Excel (ExcelJS) dimuat dari internet saat file diunggah.

Halaman terbuka dengan data contoh dari `Rak_JDC.xlsx` (sheet Rak Existing).

## Membuka lewat link

**Settings → Pages**, pilih branch `main` dan folder `/ (root)`.

## Catatan data

Tabel PP di sheet cocok dengan hitungan sel untuk Row A dan B. Pada Row C ada selisih 28-50 PP per rak; cek di tab Rekap PP.
