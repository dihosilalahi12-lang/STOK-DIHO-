# DIHO PWA — Kasir & Stok Barang

## Isi folder
- `index.html`: aplikasi kasir, stok, barcode, laporan.
- `manifest.webmanifest`: metadata agar dapat dipasang sebagai aplikasi.
- `sw.js`: service worker untuk cache/offline.
- `icon-192.png` dan `icon-512.png`: ikon aplikasi.

## Cara memasang di repository GitHub Pages
1. Buat cadangan file `index.html` lama terlebih dahulu. Jangan hapus repository.
2. Buka repository `STOK-DIHO-` di GitHub melalui browser HP.
3. Pastikan branch `main` dan folder Pages `/(root)`.
4. Upload semua isi folder ini ke root repository: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, dan `icon-512.png` (semuanya di folder utama).
5. Commit changes langsung ke branch `main`.
6. Tunggu deployment selesai, lalu buka `https://dihosilalahi12-lang.github.io/STOK-DIHO-/`.
7. Di Chrome Android, tekan menu ⋮ lalu pilih **Tambahkan ke layar utama** atau **Install app**.

## Catatan penting
- Data disimpan di `localStorage` browser/perangkat, tidak otomatis sinkron ke perangkat lain.
- Ekspor cadangan JSON secara berkala.
- Offline baru berfungsi setelah website dibuka online setidaknya sekali dan service worker selesai terpasang.
- Scan kamera memerlukan HTTPS, izin kamera, dan dukungan `BarcodeDetector` di browser. Scanner Bluetooth yang bertindak sebagai keyboard atau ketik barcode tetap bisa digunakan jika deteksi kamera tidak tersedia.
- Versi ini menyimpan harga jual, tetapi belum harga modal; karena itu laporan tidak menghitung keuntungan bersih.
- Sebelum digunakan untuk transaksi nyata, uji alur tambah barang, transaksi, stok berkurang, ekspor, dan mode offline.
