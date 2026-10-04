# Deploy ke GitHub Pages

## Cara paling sederhana

1. Buat repository GitHub baru.
2. Ekstrak paket ZIP aplikasi.
3. Unggah **seluruh isi folder** ke root repository. Pastikan `index.html` berada di root.
4. Commit ke branch `main`.
5. Buka `Settings` → `Pages`.
6. Pada `Build and deployment`, pilih `Deploy from a branch`.
7. Pilih `main` dan `/(root)`.
8. Klik `Save`.

Aplikasi tidak memerlukan Node.js, database, backend, atau build process.

## Catatan jaringan

Fungsi inti evaluasi, tabel, gate asesor, backup, dan laporan berjalan client-side. Pembacaan DOCX/PDF dan ekspor DOCX/PDF menggunakan pustaka yang dimuat dari jsDelivr CDN. Jika pustaka ekspor tidak termuat, aplikasi menyediakan fallback print/Save as PDF dan Word `.doc`.

## Privasi

Data evaluasi disimpan di `localStorage` browser. Data tidak otomatis dikirim ke server oleh aplikasi ini. Pengguna tetap bertanggung jawab atas kebijakan keamanan dokumen, hak akses repository, dan pengelolaan bukti sensitif.
