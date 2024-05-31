# Penculikan Sesi
> Penculikan sesi adalah ketika seorang penyerang mengambil alih entah sesi komunikasi TCP yang valid antara dua komputer atau sesi pengguna yang valid dalam aplikasi web.

Serangan penculikan sesi mengacu pada eksploitasi mekanisme pembangkitan token sesi atau kontrol keamanan token yang memungkinkan seorang penyerang untuk membentuk koneksi yang tidak sah dengan server target. Penyerang menebak atau mencuri ID sesi yang valid (yang mengidentifikasi pengguna yang terautentikasi) dan menggunakannya untuk membentuk sesi dengan server.

- Penculikan sesi aktif: Seorang penyerang menemukan sesi aktif dan mengambil alih
- Penculikan sesi pasif: Seorang penyerang menculik sesi, dan, alih-alih mengambil alih, memantau dan mencatat semua lalu lintas dalam sesi tersebut

Penculikan sesi dapat dibagi menjadi tiga fase besar:
- Melacak Koneksi: Penyerang menggunakan alat pemantau jaringan untuk melacak korban dan host, atau menggunakan alat seperti Nmap untuk memindai jaringan mencari target dengan urutan TCP yang mudah ditebak
- Membuat Koneksi Tidak Sinkron: Sebuah keadaan tidak sinkron terjadi ketika koneksi antara target dan host telah terbentuk, atau stabil tanpa transmisi data, atau ketika nomor urut server tidak sama dengan nomor pengakuan klien (atau sebaliknya)
- Memasukkan Paket Penyerang: Begitu penyerang telah mengganggu koneksi antara server dan target, mereka dapat menyuntikkan data ke jaringan atau aktif berpartisipasi sebagai orang tengah, melewati data antara target dan server, sambil membaca dan menyuntikkan data sesuai kehendak

Ada dua metode utama yang dapat digunakan untuk mendeteksi penculikan sesi:
- Metode Manual: Melibatkan penggunaan perangkat lunak pemantauan paket seperti Wireshark dan SteelCentral Packet Analyzer untuk memonitor serangan penculikan sesi; penangkap paket menangkap paket yang ditransfer melintasi jaringan, yang kemudian dianalisis menggunakan berbagai alat penyaringan
- Metode Otomatis: Melibatkan menggunakan Sistem Deteksi Intrusi (IDS) dan Sistem Pencegahan Intrusi (IPS) untuk memantau lalu lintas jaringan masuk; jika sebuah paket cocok dengan salah satu tanda serangan dalam basis data internal, IDS menghasilkan peringatan, dan IPS memblokir lalu lintas masuk ke basis data
