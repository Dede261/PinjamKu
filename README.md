# PinjamKu Android — paket sumber untuk membangun APK

Paket ini membungkus prototipe HTML PinjamKu menjadi proyek Android menggunakan Capacitor dan menyediakan workflow GitHub Actions untuk membangun APK debug di cloud.

## Cara memakai dari HP
1. Buat akun GitHub atau masuk ke https://github.com.
2. Buat repository baru bernama `PinjamKu` (Public paling mudah untuk pemula; jangan masukkan data pribadi).
3. Ekstrak ZIP ini di HP.
4. Unggah seluruh ISI folder ini ke repository, termasuk folder tersembunyi `.github/workflows`.
   Jika unggah via browser HP tidak memperlihatkan folder `.github`, buat workflow melalui tab **Actions** atau gunakan GitHub Desktop/fitur upload yang mendukung folder tersembunyi.
5. Pastikan file `package.json`, `capacitor.config.ts`, folder `www`, dan `.github/workflows/build-apk.yml` berada di root repository.
6. Buka tab **Actions**. Pilih workflow **Build PinjamKu Android APK**, lalu tekan **Run workflow** (atau tunggu workflow berjalan setelah push ke `main`).
7. Jika build berhasil, buka run terbaru, cari bagian **Artifacts**, lalu unduh `PinjamKu-debug-APK`.
8. Ekstrak hasil unduhan dan instal `app-debug.apk` di HP. Android mungkin meminta izin instal aplikasi dari sumber tersebut.

## Catatan
- Ini APK debug untuk uji coba, bukan rilis produksi yang ditandatangani dengan kunci rilis.
- APK ini berisi prototipe edukasi. Data pengajuan disimpan lokal di browser/WebView dan tidak dikirim ke server.
- Jangan gunakan data KTP atau data pribadi sungguhan.
- Untuk layanan pinjaman nyata, diperlukan backend aman, perlindungan data, serta kepatuhan terhadap aturan yang berlaku.
- Build bergantung pada kompatibilitas toolchain dan keberhasilan GitHub Actions; APK belum dibangun atau diuji pada perangkat dalam paket ini.
