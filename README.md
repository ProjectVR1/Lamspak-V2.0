# Muhasabbah FED LAMSPAK Sarjana — Assessor Ready + Status Simulation v5.0

Aplikasi statis siap **GitHub Pages** untuk evaluasi diri, review internal, dan persiapan asesmen Program Sarjana/S1 berbasis paket IAPS 2.0 Unggul Sarjana yang menjadi sumber aplikasi.

## Tujuan versi 4

Versi ini mempertahankan rubrik, bobot, indikator, tabel, dan kalkulator dari paket sebelumnya, tetapi menambah alur **assessor-ready** agar penilaian lebih mudah ditelusuri dan tidak bergantung pada satu angka ringkas.

Pemisahan konsep yang digunakan:

1. **Skor rubrik 0–2** — judgement evaluator terhadap deskriptor instrumen.
2. **Indeks kesiapan internal** — normalisasi `Σ(skor × bobot) / 282 × 100`; bukan nilai akreditasi resmi.
3. **Kematangan bukti** — status dokumentasi internal; tidak menaikkan skor rubrik.
4. **Gate verifikasi asesor** — kelengkapan prosedural dan keterlacakan bukti; bukan validitas substantif.
5. **Keputusan review internal** — Disepakati / Perlu klarifikasi / Perlu revisi bukti; bukan keputusan LAMSPAK.

## Fitur utama

- 73 indikator, 11 standar operasional pada matriks sumber, bobot total 141, maksimum berbobot 282.
- 43 tabel FED beserta formula bantu.
- Penandaan terpisah untuk:
  - batas bawah skor rubrik;
  - lima butir `SYARAT PERLU UNGGUL`;
  - butir yang memiliki catatan syarat minimum terakreditasi.
- Kalkulator deterministik untuk indikator kuantitatif yang formulanya dapat dioperasionalkan.
- **Mode Asesor Internal** dengan antrian prioritas, filter, keputusan review, dan ekspor CSV.
- **Gate verifikasi per butir** berbasis 10 unsur prosedural: skor, lokasi bukti, status bukti, pemilik, tanggal verifikasi, serta 5 checklist keterlacakan.
- **Rekonsiliasi skor** bila skor evaluator berbeda dari hasil kalkulator deterministik.
- Register bukti dengan jenis sumber, periode data, pemilik, dan checklist keterlacakan.
- Narasi hasil otomatis, narasi FED editable, rekomendasi berbasis gap, dan rencana tindak lanjut.
- Screening FED berbasis teks yang konservatif. Nilai “kecocokan tekstual” bukan probabilitas kebenaran.
- Laporan lengkap untuk cetak/Save as PDF dan ekspor Word `.docx`; bila pustaka `docx.js` tidak termuat, tersedia fallback `.doc`.
- Backup/restore JSON dan reset data.
- Footer: **Trademark @ramakertamukti**.

## Prinsip no-fake

Aplikasi tidak:

- menyatakan status akreditasi otomatis;
- menganggap dokumen asli hanya karena status `Terverifikasi` dipilih pengguna;
- mengubah skor hanya karena bukti banyak;
- menganggap teks yang tidak ditemukan sebagai skor 0;
- mengarang data, tanggal, dokumen, hasil survei, atau bukti;
- menyamakan kecocokan teks dengan validitas bukti;
- menyembunyikan perbedaan antara skor evaluator dan kalkulator.

## Gate “Siap ditelaah”

Sebuah butir diberi status **Siap ditelaah** hanya bila seluruh unsur prosedural berikut tersedia:

- skor evaluator;
- lokasi/tautan bukti;
- status bukti `Terverifikasi`;
- pemilik bukti;
- tanggal verifikasi;
- relevansi bukti dengan indikator/rubrik;
- asal/identitas sumber teridentifikasi;
- periode data sesuai;
- konsisten dengan FED/tabel/data terkait;
- dapat ditelusuri ulang.

Gate ini hanya mengukur **kelengkapan dan traceability**. Asesor tetap harus membaca dokumen asli dan menilai substansi.

## Verifikasi sumber eksternal

Pada 4 Oktober 2026, laman resmi LAMSPAK masih mencantumkan **Paket IAPS 2.0 Unggul Sarjana** pada:

`https://www.lamspak.id/akreditasi/instrumen/`

Buku B IAPS 2.0 pada domain LAMSPAK juga menjelaskan lima indikator Syarat Perlu Status Terakreditasi Unggul. Lima konsep tersebut konsisten dengan butir yang ditandai pada basis data aplikasi: 9, 16, 55, 56, dan 60.

Sebelum pengajuan resmi, pengguna tetap wajib memastikan bahwa berkas instrumen lokal sama dengan versi yang berlaku pada tanggal pengajuan.

## Instalasi GitHub Pages

1. Buat repository GitHub baru.
2. Unggah seluruh isi folder ini ke root repository.
3. Buka `Settings` → `Pages`.
4. Pilih `Deploy from a branch`.
5. Pilih branch `main` dan folder `/(root)`.
6. Simpan dan buka URL GitHub Pages.

Tidak membutuhkan server, database, Node.js, atau build step.

## Struktur berkas

- `index.html` — UI utama.
- `styles.css` — CSS inti.
- `assessor-v5.css` — UI assessor-ready.
- `lamspak-data.js` — data matriks dan 43 tabel.
- `app.js` — mesin inti v3 yang dipertahankan untuk kompatibilitas.
- `analysis.js` — screening dokumen FED.
- `assessor-v5.js` — migrasi data dan workflow assessor-ready v5.
- `ASSESSOR_GUIDE.md` — panduan asesor internal.
- `VALIDASI.md` — prinsip validasi dan batas klaim.
- `TESTING.md` / `TEST_RESULTS.md` — skenario dan hasil uji.

## Penyimpanan data

Data disimpan pada `localStorage` browser. Versi 4 mempertahankan storage key lama agar data v3 dapat dimigrasikan. Gunakan **Backup JSON** secara berkala, terutama sebelum browser/cache dibersihkan atau perangkat diganti.
