# Rak JDC View

Peta kapasitas rak gudang JDC dalam **tampak samping**. Satu file HTML (`index.html`), tanpa server dan tanpa instalasi.

## Tampilan

- **Tampak samping**: satu strip per rak, tiap kotak satu posisi pallet, tinggi tumpukan = jumlah level. Bisa dilihat dari barat atau timur, diwarnai menurut status atau jumlah level.
- **Potongan melintang**: profil tinggi antar rak per posisi utara-selatan, atau siluet tertinggi.
- **3D rak**: model rak seperti di gudang (tiang biru dengan penyilang, balok oranye per level, pelindung kuning, papan kode rak). Bisa diputar, diperbesar, dan dilihat setinggi mata dari lorong. Isi rak tidak digambar.
- **Rekap PP**: PP existing, PP baru, dan pembanding dengan tabel PP di sheet.

Kotak abu-abu di Excel dibaca sebagai racking baru. Data contoh diambil dari `Master_JDC_Location.xlsx` (sheet `layour JDC`).

## Memakai file Excel sendiri

Klik **Muat file Excel** atau seret file `.xlsx` ke halaman. Sheet yang namanya memuat "exist" dipakai lebih dulu; kalau tidak ada, sheet pertama (di file master: `layour JDC`).

Aplikasi membaca kode rak (A01-D09) di baris 11 (atas) dan 110 (bawah), angka level di antaranya, dan warna sel untuk menandai racking baru. Di layout master, Row B ada di utara dan Row A di selatan pada kolom yang sama; Row C dan D memanjang penuh. Layout lama (kode di baris 11 dan 49) tetap bisa dibaca. Pembaca Excel (ExcelJS) dimuat dari internet saat file diunggah. Tab 3D rak memakai WebGL2 langsung tanpa library tambahan.

Halaman terbuka dengan data contoh dari `Master_JDC_Location.xlsx`.

## Membuka lewat link

**Settings → Pages**, pilih branch `main` dan folder `/ (root)`.

## Catatan data

Sheet layout terbaru tidak punya tabel PP per rak, jadi kolom PP di tab Rekap PP kosong. Blok kecil enam baris di utara Row C belum diberi kode di Excel; aplikasi menamainya N01-N10.

## Client

Nama client (Monde, Toshiba, Daelim, dan seterusnya) dibaca dari kotak teks berwarna di atas layout Excel. Tiap posisi rak diberi client berdasarkan kotak yang menutupinya. Pilih **Warna: Client** untuk mewarnai rak per client, lalu klik nama client untuk menyorotnya. Tab Rekap PP menampilkan PP existing per client.

Batas client mengikuti posisi kotak teks di Excel, jadi sel di tepi kotak bisa bergeser satu kolom. Racking baru (abu-abu) belum punya client.
