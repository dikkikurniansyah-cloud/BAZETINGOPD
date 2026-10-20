PANDUAN PASANG - Dashboard Data Bezeting (PHP)

Kebutuhan: hosting dengan PHP 7.4 atau lebih baru. Tidak perlu database.

1. Upload folder "bezeting-php" ke hosting (misalnya ke public_html/bezeting).
2. Buka file config.php, ganti 'ganti-password-ini' dengan password admin milikmu.
   Password ini hanya dipakai untuk menghapus link bukti dukung.
3. Pastikan folder "data" bisa ditulis oleh PHP (di cPanel: klik kanan folder, Change Permissions, 755 atau 775).
4. Buka alamatnya di browser, contoh: https://domainmu.go.id/bezeting/
5. Coba simpan satu link, lalu cek folder "data": harus muncul file links.json.

Catatan
- Petugas OPD tidak perlu akun. Mereka cukup membuka alamatnya, memilih OPD, menempel link Drive, lalu klik Simpan link.
- Kalau OPD salah memasukkan link, cukup simpan link yang benar. Yang tampil selalu link terbaru.
- Folder "data" dilindungi .htaccess (khusus Apache). Kalau hosting memakai Nginx, tambahkan aturan: location ^~ /bezeting/data/ { deny all; }
- Cadangkan file data/links.json secara berkala, karena semua link tersimpan di sana.
- Link Drive di dalam aplikasi harus dibagikan dengan akses "Siapa saja yang memiliki link" agar tombol Download berfungsi.
