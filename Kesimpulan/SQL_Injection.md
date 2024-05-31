# Injeksi SQL
> Injeksi SQL adalah teknik yang memanfaatkan kerentanan input untuk melewati perintah SQL jahat melalui aplikasi web untuk dieksekusi oleh database backend.

Ikhtisar tentang Injeksi SQL:
- Serangan injeksi SQL dapat dilakukan menggunakan berbagai teknik untuk melihat, memanipulasi, memasukkan, dan menghapus data dari database aplikasi. Ada tiga jenis utama injeksi SQL:
  - Injeksi SQL dalam-band: Seorang penyerang menggunakan saluran komunikasi yang sama untuk melakukan serangan dan mendapatkan hasil
  - Injeksi SQL buta/inferensial: Seorang penyerang tidak memiliki pesan kesalahan dari sistem yang dapat digunakan, tetapi hanya mengirimkan kueri SQL jahat ke database
  - Injeksi SQL di luar-band: Seorang penyerang menggunakan saluran komunikasi yang berbeda (seperti fungsi email database, atau fungsi penulisan dan pemuatan file) untuk melakukan serangan dan mendapatkan hasil

Injeksi SQL dapat digunakan untuk menerapkan serangan berikut:
- Pengabaian autentikasi: Seorang penyerang masuk ke aplikasi tanpa menyediakan nama pengguna dan sandi yang valid dan mendapatkan hak administratif
- Pengabaian otorisasi: Seorang penyerang mengubah informasi otorisasi yang disimpan dalam database dengan memanfaatkan kerentanan injeksi SQL
- Pengungkapan informasi: Seorang penyerang mendapatkan informasi sensitif yang disimpan dalam database
- Integritas data terompah: Seorang penyerang mengubah tampilan sebuah halaman web, memasukkan konten jahat ke halaman web, atau mengubah isi database
- Ketersediaan data terompah: Seorang penyerang menghapus informasi tertentu, log, atau informasi audit dalam database
- Eksekusi kode jarak jauh: Seorang penyerang menjalankan potongan kode dari jarak jauh yang dapat mengorbankan sistem operasi host

sqlmap adalah alat uji penetrasi open-source yang mengotomatisasi proses mendeteksi dan mengeksploitasi kerentanan injeksi SQL serta mengambil alih server database. Ini dilengkapi dengan mesin deteksi yang kuat, banyak fitur niche, dan beragam switch—mulai dari pemetaan sidik jari database dan pengambilan data dari database hingga mengakses sistem file dasar dan menjalankan perintah pada sistem operasi melalui koneksi luar-band.

Anda dapat menggunakan sqlmap untuk melakukan injeksi SQL pada situs web target menggunakan berbagai teknik, termasuk berbasis Boolean buta, berbasis waktu buta, berbasis kesalahan, kueri UNION, kueri bertumpuk, dan injeksi SQL di luar-band.

Deteksi Kerentanan Injeksi SQL menggunakan DSSS:
- Damn Small SQLi Scanner (DSSS) adalah pemindai kerentanan injeksi SQL yang sepenuhnya fungsional yang mendukung parameter GET dan POST. DSSS memindai aplikasi web untuk berbagai kerentanan injeksi SQL.
