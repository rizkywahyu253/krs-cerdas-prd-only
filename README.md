# KRS Cerdas — PRD Only

Dokumen PRD dan prototype pemrograman KRS untuk mahasiswa aktif Universitas Muhammadiyah Malang.

## Latar belakang dan bukti
UX Detective menemukan masalah jadwal bentrok, sulit membedakan mata kuliah peminatan, jadwal tidak terurut, keterangan waktu “jam ke-X”, dan keterbatasan pembayaran. Prototype ini berfokus pada alur pemilihan kelas. Tiga wawancara menguatkan kebutuhan untuk mengetahui bentrok lebih awal, melihat label penjurusan, dan menemukan alternatif kelas. Bukti berasal dari sampel kualitatif kecil dan perlu divalidasi dengan riset lebih lanjut.

## Problem statement
Mahasiswa aktif UMM membutuhkan sistem pemilihan kelas yang mendeteksi dan menandai jadwal berbenturan secara langsung karena bentrok sering diketahui di akhir proses ketika kuota alternatif dapat habis dan pemeriksaan jadwal masih manual.

## Pengguna utama
Mahasiswa aktif UMM yang menyusun KRS untuk semester berikutnya, termasuk pengguna ponsel selama periode pemilihan dengan kuota kelas terbatas.

## Tujuan produk
- Mencegah pengguna memilih kelas dengan jadwal berbenturan.
- Menampilkan informasi yang diperlukan di halaman pemilihan.
- Memudahkan pemulihan dengan pilihan kelas yang masih tersedia.

## Ruang lingkup MVP dan acceptance criteria
1. Bandingkan hari dan rentang waktu kelas kandidat dengan jadwal terpilih.
2. Tandai bentrok sebelum kelas dipilih. Tampilkan alasan dan kelas penyebab; nonaktifkan aksi pilih pada kelas yang bertabrakan.
3. Tampilkan penjurusan, waktu aktual, ruang, pengajar, dan sisa kuota pada kartu kelas.
4. Perbarui jumlah mata kuliah, total SKS, dan ringkasan jadwal setelah tambah atau hapus kelas.
5. Tampilkan alternatif yang tidak bentrok pada daftar kelas yang sama.
6. Buat alur utama tetap terbaca dan dapat dioperasikan di layar ponsel.

## Prioritas kebutuhan
- **Must:** indikator bentrok saat memilih (UX-01), alternatif kelas tersedia (UX-04).
- **Should:** label penjurusan (UX-02), waktu aktual (UX-03), jadwal terurut dan status bentrok (UX-05).
- **Could:** pengajuan pindah kelas di sistem (UX-06), menunggu kejelasan kebijakan kampus.

## Di luar cakupan
Login, integrasi My UMM, data akademik/kuota real-time, pembayaran, persetujuan KRS, dan layanan pindah kelas. Aplikasi adalah prototype data contoh dan tidak mengirim atau menyimpan data mahasiswa.

## Validasi
Target usulan dari Worksheet 8: pengguna mengenali kelas bentrok dalam ≤3 detik tanpa catatan manual. Ini target uji yang belum diukur. Validasi alur pemilihan, pemahaman alasan bentrok, penemuan kelas alternatif, dan keterbacaan mobile melalui usability test.

## Menjalankan aplikasi
```bash
cd apps/web
npm install
npm run dev
```
Build produksi: `npm run build`. Workflow GitHub Pages tersedia di `.github/workflows/deploy.yml`; setelah repository di-push dan Pages diatur ke GitHub Actions, setiap perubahan pada `apps/web` dapat dideploy otomatis.

## Struktur repo
- `apps/web`: prototype web berbasis Vite.
- `.github/workflows/deploy.yml`: build dan deployment ke GitHub Pages.
- `CHANGELOG.md`: riwayat perubahan.
