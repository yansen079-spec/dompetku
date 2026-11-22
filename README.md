# DompetKu V2 — Money Tracker

Website money tracker pribadi yang responsif untuk laptop dan HP.

## Fitur
- Dashboard saldo total, pemasukan, pengeluaran, grafik enam bulan.
- Tambah, edit, hapus transaksi; cari berdasarkan kategori/catatan, filter bulan dan jenis.
- Dompet Tunai/Bank/E-Wallet, tambah dompet baru, edit nama serta saldo awal.
- Anggaran kategori dan ringkasan bulanan.
- Ekspor CSV transaksi, backup dan impor JSON.
- PWA dengan manifest dan service worker (saat dipasang di HTTPS).

## Jalankan di laptop
Ekstrak ZIP, buka `index.html` lewat Chrome/Edge. Alternatif: di folder project jalankan `python -m http.server 8080` dan kunjungi `http://localhost:8080`.

## Instal di HP
Unggah isi folder ke hosting HTTPS (misalnya GitHub Pages atau Netlify), kunjungi URL dari Chrome Android, pilih **Install app/Tambahkan ke Layar Utama**. Ini PWA, **bukan APK native**.

## Penting
- Data hanya disimpan lokal di browser masing-masing menggunakan `localStorage`. **Tidak tersinkron otomatis antar HP/laptop.**
- Versi ini menggunakan key penyimpanan yang sama dengan DompetKu V1 (`dompetku_v1`), jadi data lama di browser dan asal situs yang sama tetap terbaca. Jika membuka V2 melalui URL/domain/protokol berbeda, data tidak otomatis muncul. Gunakan ekspor/impor JSON untuk memindahkannya.
- Backup JSON secara rutin. Jangan simpan catatan finansial sensitif pada perangkat bersama.
- Saldo negatif dapat terjadi jika ada pengeluaran tetapi saldo awal dompet nol. Atur melalui Dompet → Edit saldo awal.
- Belum ada login/cloud, koneksi rekening otomatis, dan APK native. Untuk sinkronisasi multi-perangkat diperlukan backend dan autentikasi.
