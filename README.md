# 📚 SiPerpus — Sistem Perpustakaan Digital (SMK 3 Kendari)

**[ID] Deskripsi Aplikasi**
SiPerpus adalah aplikasi perpustakaan digital mandiri yang dirancang khusus untuk mempermudah siswa SMK 3 Kendari dalam mencari buku, mengajukan peminjaman, dan mengelola pengembalian secara praktis melalui ponsel pintar.

Aplikasi ini mengusung konsep koneksi tanpa login yang mengutamakan kemudahan akses bagi siswa. Integrasi sistem backend memanfaatkan Google Sheets dan Google Apps Script secara real-time. Petugas perpustakaan (Admin) dapat mengelola seluruh data persetujuan transaksi, inventaris, dan histori peminjaman langsung dari lembar kerja spreadsheet tanpa memerlukan panel admin yang rumit.

**[EN] App Description**
SiPerpus is a self-service digital library application designed specifically to help students of SMK 3 Kendari browse books, request loans, and manage returns directly from their smartphones.

Built with a no-login accessibility concept, the app prioritizes simplicity and user experience for students. The backend system is integrated in real-time with Google Sheets via Google Apps Script, allowing library admins to manage transaction approvals, catalog inventories, and borrowing histories directly within a spreadsheet without requiring a complex administration panel.

---

**⚡ Fitur Utama / Key Features**

📖 Katalog Digital Interaktif (Interactive Catalog) Menampilkan daftar buku secara dinamis lengkap dengan pengarang, penerbit, nomor ISBN, deskripsi, dan sisa stok buku fisik. Dilengkapi dengan filter kategori dan pencarian instan.

📋 Peminjaman Mandiri Tanpa Antre (Self-Service Borrowing) Siswa cukup memilih buku, memasukkan nama dan kelas melalui menu dropdown kelas yang presisi untuk menghindari salah ketik, lalu mengajukan waktu pinjam (mulai dari 1 hari hingga 1 semester).

🔍 Lacak Pinjaman Aktif ("Pinjamanku") (Real-Time Loan Tracker) Siswa dapat memeriksa riwayat transaksi mereka kapan saja hanya dengan memasukkan Nama dan Kelas mereka. Halaman ini melacak status approval, tanggal pinjam, dan batas waktu pengembalian.

🔄 Pengembalian Terintegrasi (Integrated Returns) Pengajuan pengembalian buku fisik dapat dimulai langsung dari aplikasi dengan sekali ketuk untuk merubah status menjadi antrean pengembalian.

⚡ Otomatisasi Stok & Persetujuan Admin (Auto-Inventory Trigger) Ketika admin mengubah status di Google Sheets (misal: menyetujui peminjaman atau pengembalian), sistem script di Google Sheets secara otomatis akan mengurangi atau menambah stok buku bersangkutan secara real-time.

---

**💡 Alur Cara Kerja / Workflow**

Cari & Ajukan: Siswa mencari buku di aplikasi, lalu mengetuk "Pinjam". Peminjaman tercatat di Google Sheets sebagai status pending_pinjam.
Persetujuan: Siswa membawa buku fisik ke petugas. Petugas mengubah status di spreadsheet menjadi dipinjam, dan sistem secara otomatis mengurangi stok buku di catalog.
Ajukan Kembali: Saat ingin mengembalikan buku, siswa mencari datanya di menu "Pinjamanku" pada aplikasi dan mengetuk "Kembalikan Buku" (status berubah menjadi pending_kembali).
Selesai: Siswa menyerahkan buku ke petugas. Petugas mengubah status di spreadsheet menjadi kembali, dan sistem otomatis menambahkan kembali stok buku.
