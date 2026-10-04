# Checklist Pengujian v5

## Integritas data

- [ ] 73 indikator termuat.
- [ ] 43 tabel termuat.
- [ ] 11 standar termuat.
- [ ] bobot total = 141.
- [ ] maksimum berbobot = 282.
- [ ] syarat perlu Unggul = butir 9, 16, 55, 56, 60.

## Mode Asesor

- [ ] Mode Asesor menampilkan 73 baris saat tanpa filter.
- [ ] Butir tanpa skor/bukti berstatus `Belum siap`.
- [ ] Butir dengan seluruh 10 unsur gate lengkap berstatus `Siap ditelaah`.
- [ ] Bila keputusan `Disepakati` dan gate lengkap, status menjadi `Selesai review`.
- [ ] Bila kalkulator berbeda dari skor evaluator, status menjadi `Perlu rekonsiliasi` sampai centang rekonsiliasi diisi.
- [ ] Filter klarifikasi, rekonsiliasi, belum siap, dan syarat Unggul bekerja.
- [ ] CSV antrian asesor dapat diunduh.

## Bukti

- [ ] Jenis sumber, periode, pemilik, lokasi, dan tanggal verifikasi tersimpan.
- [ ] Lima checklist bukti tersimpan.
- [ ] Status bukti tidak mengubah skor rubrik.

## Ekspor dan penyimpanan

- [ ] Backup JSON versi 4 dapat diunduh.
- [ ] Backup v3 dapat dipulihkan dan dimigrasikan ke field v5.
- [ ] Word export memuat gate dan keputusan review.
- [ ] PDF export memuat ringkasan asesor dan rincian indikator.
- [ ] Print/Save as PDF menampilkan view laporan.
- [ ] Reset menghapus data lokal setelah konfirmasi.

## Regression

- [ ] Screening FED tetap konservatif.
- [ ] 43 tabel dan formula tetap berjalan.
- [ ] Kalkulator indikator tetap bekerja.
- [ ] Tidak ada JavaScript page error pada uji browser.
