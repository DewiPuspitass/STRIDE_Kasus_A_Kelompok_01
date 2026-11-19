Kelompok 1
Anggota:
- Dewi Puspita Sari (103012680029)
- Rahman Hakim (103012680032)
- I Made Adre Udayana Putra (103012680049)

Kasus A
1. Latar belakang dan operasi sistem
Sebuah perguruan tinggi menggunakan layanan presensi berbasis web yang dapat diakses melalui browser. Dosen membuka sesi untuk kelas yang diampu. Sistem kemudian membuat QR code yang dapat ditampilkan pada layar di ruang kelas.Mahasiswa masuk dengan akun kampus, memindai QR code, kemudian aplikasi
mengirim identitas sesi dan informasi autentikasi mahasiswa ke Backend Presensi. Backend memeriksa sesi yang masih berlaku dan status mahasiswa dalam kelas. Jika memenuhi aturan, server menambahkan catatan kehadiran dalam Database Akademik. Sesi presensi memiliki masa berlaku lima menit. Dosen dapat memantau daftar hadir
untuk kelasnya dan menutup sesi sebelum waktu berakhir. Admin akademik dapat melihat rekap untuk seluruh kelas melalui antarmuka web.

2. Informasi arsitektur dan aturan bisnis
Elemen Informasi yang tersedia
Aktor: Mahasiswa, dosen pengampu; admin akademik.
Komponen: Browser/aplikasi web, Backend Presensi, layanan autentikasi kampus, Database Akademik.
Data utama: Identitas pengguna, keanggotaan kelas, jadwal, sesi, token/kode QR, catatan kehadiran.
Alur pokok: Dosen membuka sesi → QR ditampilkan → mahasiswa memindai → backend memvalidasi → kehadiran dicatat → rekap ditampilkan. 
Aturan bisnis: Hanya dosen pengampu membuka sesi kelasnya, satu mahasiswa mempunyai paling banyak satu catatan hadir per sesi, sesi berlaku lima menit.

3. Batas lingkup
Analisis mencakup pembukaan/penutupan sesi, pemindaian, validasi kehadiran, dan pembacaan rekap. Pendaftaran mata kuliah dan perubahan nilai tidak dibahas.

4. Instruksi khusus untuk model DFD
Buat DFD yang memperlihatkan perlintasan data dari perangkat mahasiswa/dosen ke layanan kampus, hubungan ke autentikasi dan database, serta proses pemuatan rekap.

5. Pertanyaan penuntun
• Apa aset yang harus dilindungi dan siapa saja yang berkepentingan terhadapnya?
• Data apa yang dikirim melalui setiap aliran, dan komponen mana yang memutuskan apakah permintaan boleh dipenuhi?
• Di bagian mana data melintasi batas kepercayaan yang berbeda?
• Kondisi apa saja yang perlu diasumsikan karena deskripsi belum menguraikannya?
