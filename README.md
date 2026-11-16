# ZYY-SAVINGS v1.0

Aplikasi pencatat tabungan pribadi untuk target PC desain FTTH. Tampilan dark navy + neon blue. Semua data disimpan di `localStorage` browser yang digunakan, **bukan di rekening bank**.

## Fitur
- Target tabungan, saldo awal, dan rencana setoran bulanan yang bisa diubah.
- Catatan setoran dan penarikan serta riwayat transaksi.
- Progress, milestone, estimasi bulan mencapai target, grafik simulasi 6 bulan.
- Offline setelah dipasang melalui hosting HTTPS (service worker).
- Ekspor cadangan JSON, pemulihan JSON, dan ekspor transaksi CSV.
- Tanpa login, tanpa server, tanpa biaya langganan, tanpa koneksi rekening.

## Cara cepat membuka
Buka `index.html` di browser komputer. Untuk pencatatan yang stabil dan pemasangan di Android, disarankan hosting HTTPS.

## Cara memasang sebagai aplikasi di Android (GitHub Pages)
1. Buat repository publik GitHub, contoh `zyy-savings`.
2. Upload **isi folder** ini ke root repository: `index.html`, `manifest.webmanifest`, `sw.js`, dan folder `icons` beserta seluruh file icon.
3. Di GitHub: **Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save**.
4. Tunggu hingga GitHub Pages menampilkan URL situs, misalnya `https://USERNAME.github.io/zyy-savings/`.
5. Buka URL tersebut di **Chrome Android** → menu ⋮ → **Install app** / **Tambahkan ke layar utama**.
6. Ikon **ZYY-SAVINGS** akan muncul pada layar utama; buka seperti aplikasi biasa. Setelah situs pernah dibuka dan di-cache, aplikasi dapat digunakan offline.

**Penting:** versi ini berupa PWA (Progressive Web App), **bukan file APK asli**. Untuk menghasilkan APK native, perlu pembungkus Android/Capacitor atau Android Studio, serta proses signing dan pengujian Android.

## Data dan privasi
- Aplikasi **tidak melakukan transaksi bank** dan tidak mempunyai akses ke Bank Jago, blu, SeaBank, atau rekening lainnya.
- `localStorage` terikat pada alamat situs & browser. Membuka file yang sama melalui URL lain akan menunjukkan data yang berbeda.
- Data dapat hilang jika pengguna menghapus data situs, melakukan reset perangkat, atau berpindah browser. **Unduh cadangan JSON secara berkala** dan simpan di penyimpanan aman.
- Jangan memasukkan PIN, password bank, NIK, atau informasi keuangan yang tidak dibutuhkan.
- Input saldo awal default `Rp0`, bukan `Rp1.500.000` karena nilai itu sebelumnya berupa contoh; ubah sesuai dana yang benar-benar telah disisihkan.

## Penyimpanan
`localStorage` key: `zyy-savings-state-v1`, format JSON versi 1.

## Pengembangan berikutnya
Jika diperlukan: beberapa target sekaligus, PIN lokal yang aman, pengingat lewat notifikasi Android, Google Drive backup manual, dan APK Android.
