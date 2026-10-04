# Hasil Pengujian — Muhasabbah FED LAMSPAK Sarjana v5.0

Tanggal uji: 4 Oktober 2026.

## 1. Integritas data

Hasil pemeriksaan programatik:

- indikator: **73** — lulus;
- standar operasional pada matriks: **11** — lulus;
- total bobot: **141** — lulus;
- maksimum berbobot: **282** — lulus;
- tabel FED: **43** — lulus;
- formula tabel yang dipreservasi: **166** — terdeteksi;
- butir syarat perlu Unggul: **9, 16, 55, 56, 60** — lulus;
- butir catatan syarat minimum terakreditasi: **44, 45** — terdeteksi.

## 2. Sintaks JavaScript

`node --check` pada:

- `app.js` — lulus;
- `analysis.js` — lulus;
- `lamspak-data.js` — lulus;
- `assessor-v5.js` — lulus.

## 3. Uji browser headless

Aplikasi diuji dengan Chromium headless menggunakan HTML/CSS/JavaScript lokal yang sama dengan paket. Ketergantungan CDN sengaja tidak diperlukan untuk skenario inti.

Hasil:

- JavaScript page error: **0**;
- Mode Asesor tampil: **lulus**;
- jumlah baris Mode Asesor tanpa filter: **73**;
- jumlah criterion card: **73**;
- verification gate card: **73**;
- review box: **73**;
- footer: **Trademark @ramakertamukti** — lulus.

## 4. Uji gate verifikasi

Skenario butir 1:

- skor diisi;
- lokasi bukti diisi;
- status bukti = Terverifikasi;
- pemilik bukti dan tanggal verifikasi diisi;
- jenis sumber dan periode data diisi;
- lima checklist keterlacakan dicentang.

Hasil: **Siap ditelaah • 100%**.

Setelah reviewer diisi dan keputusan `Disepakati` diberikan, hasil: **Selesai review • 100%**.

## 5. Uji rekonsiliasi empiris

Skenario butir 9:

- evaluator memilih skor 1;
- RIPK dimasukkan = 3,25;
- kalkulator deterministik menghasilkan saran skor 2.

Hasil: butir ditandai **Perlu rekonsiliasi**. Filter `Perlu rekonsiliasi skor` menampilkan butir 9. Sistem tidak menimpa skor evaluator secara otomatis.

## 6. Uji ekspor

- CSV antrian asesor: **74 baris** termasuk header — lulus.
- backup JSON: `version = 4` dan `state.version = 4` — lulus.
- Word fallback `.doc` saat `docx.js` tidak tersedia: file terbentuk dan berisi laporan lengkap — lulus.
- Jalur `.docx` tetap tersedia saat `docx.js` termuat di GitHub Pages.
- PDF menggunakan jsPDF/AutoTable bila tersedia; bila tidak, aplikasi mengalihkan ke print/Save as PDF.

## 7. Kesimpulan uji

Uji memvalidasi integritas perangkat lunak, alur gate, penyimpanan, dan keterlacakan. Uji ini **tidak** mengesahkan aplikasi sebagai instrumen resmi LAMSPAK dan tidak membuktikan validitas substantif bukti yang dimasukkan pengguna.
