# Kriptografi

> Kriptografi adalah studi dan seni menyembunyikan informasi yang bermakna dalam format yang tidak terbaca. Sistem kriptografi dan kriptografis ("kripto") membantu dalam mengamankan data dari penyadapan dan kompromi selama transmisi online. Kriptografi memungkinkan seseorang untuk mengamankan transaksi, komunikasi, dan proses lain yang dilakukan di dunia elektronik, dan juga digunakan untuk melindungi data rahasia seperti pesan email, sesi obrolan, transaksi web, data pribadi, data perusahaan, aplikasi e-commerce, dll.

Ikhtisar Kriptografi
“Kriptografi” berasal dari kata-kata Yunani kryptos, yang berarti “tersembunyi, tersembunyi, ditutupi, rahasia, atau misterius,” dan graphia, “menulis”; dengan demikian, kriptografi adalah “seni menulis rahasia.”

Kriptografi adalah praktik menyembunyikan informasi dengan mengonversi teks biasa (format yang dapat dibaca) menjadi teks sandi (format yang tidak terbaca) menggunakan kunci atau skema enkripsi: ini adalah proses konversi data menjadi kode acak yang dikirimkan melintasi jaringan pribadi atau publik.

Ada dua jenis kriptografi, ditentukan oleh jumlah kunci yang digunakan untuk enkripsi dan dekripsi:

- **Enkripsi Simetris**: Enkripsi simetris (kunci rahasia, kunci bersama, dan kunci pribadi) menggunakan kunci yang sama untuk enkripsi seperti yang digunakan untuk dekripsi

- **Enkripsi Asimetris**: Enkripsi asimetris (kunci publik) menggunakan kunci enkripsi yang berbeda untuk enkripsi dan dekripsi; kunci-kunci ini dikenal sebagai kunci publik dan kunci pribadi

Fungsi hash menghitung representasi string bit berukuran tetap yang unik, yang disebut digest pesan, dari setiap blok informasi sembarang. Fungsi hash pesan (One-way Hash) mengkondensasikan informasi yang terkandung dalam suatu file (kecil atau besar) menjadi satu nomor dengan panjang tetap, biasanya antara 128 dan 256 bit. Jika bit tertentu dari input fungsi berubah, setiap bit output memiliki kemungkinan 50% berubah. Diberikan file input dan digest pesan yang sesuai, seharusnya hampir tidak mungkin untuk menemukan file lain dengan nilai digest pesan yang sama, karena secara komputasi tidak mungkin untuk memiliki dua file dengan nilai digest pesan yang sama.

MD2, MD4, MD5, dan MD6 adalah algoritma digest pesan yang digunakan dalam aplikasi tanda tangan digital untuk mengompresi dokumen secara aman sebelum sistem menandainya dengan kunci pribadi. Algoritma-algoritma ini dapat memiliki panjang variabel, tetapi hasil digest pesan selalu 128 bit.

Algoritma MD5 adalah fungsi hash kriptografi yang banyak digunakan yang mengambil pesan dengan panjang sembarang sebagai input dan menghasilkan sidik jari atau digest pesan 128-bit (16-byte) dari input tersebut. Algoritma MD5 digunakan dalam berbagai aplikasi kriptografi dan berguna untuk aplikasi tanda tangan digital, pemeriksaan integritas file, dan penyimpanan kata sandi.

Sertifikat yang ditandatangani sendiri secara luas digunakan untuk pengujian server. Dalam sertifikat yang ditandatangani sendiri, pengguna membuat sepasang kunci publik dan pribadi menggunakan alat pembuatan sertifikat seperti Adobe Acrobat Reader, keytool Java, Keychain Apple, dll. dan menandatangani dokumen dengan kunci publik. Penerima meminta kunci pribadi dari pengirim untuk memverifikasi sertifikat. Namun, verifikasi sertifikat jarang terjadi karena kebutuhan untuk mengungkapkan kunci pribadi: ini membuat sertifikat yang ditandatangani sendiri hanya berguna dalam lingkungan pengujian yang dikendalikan sendiri.

Enkripsi email menyembunyikan konten email dari penyadap dengan mengenkripsinya ke dalam bentuk yang tidak terbaca. Email dapat dienkripsi dan didekripsi dengan menggunakan mekanisme tanda tangan digital yang menggunakan kunci publik dan pribadi: kunci publik dibagikan, sementara kunci pribadi dijaga kerahasiaannya.

Ada banyak metode yang dapat digunakan untuk enkripsi email, termasuk:

- Tanda Tangan Digital: Menggunakan kriptografi asimetris untuk mensimulasikan sifat keamanan dari tanda tangan dalam bentuk digital, bukan tertulis
- Secure Sockets Layer (SSL): Menggunakan enkripsi asimetris RSA (kunci publik) untuk mengenkripsi data yang ditransfer melalui koneksi SSL
- Transport Layer Security (TLS): Menggunakan kunci simetris untuk enkripsi paket, kunci asimetris untuk autentikasi dan pertukaran kunci, dan kode otentikasi pesan untuk integritas pesan
- Pretty Good Privacy (PGP): Digunakan untuk mengenkripsi dan mendekripsi data yang menyediakan otentikasi dan privasi kriptografis
- GNU Privacy Guard (GPG): Pengganti perangkat lunak PGP dan implementasi gratis dari standar OpenPGP yang digunakan untuk mengenkripsi dan mendekripsi data

Ikhtisar Kriptanalisis

Kriptanalisis dapat dilakukan menggunakan berbagai metode, termasuk yang berikut:

- Kriptanalisis Linier: Serangan teks jelas yang menggunakan pendekatan linier untuk menjelaskan perilaku blok sandi
- Kriptanalisis Diferensial: Pemeriksaan perbedaan dalam sebuah input dan bagaimana ini memengaruhi perbedaan hasilnya pada output
- Kriptanalisis Integral: Serangan ini berguna terhadap sandi blok berdasarkan jaringan substitusi-permutasi dan merupakan perluasan dari kriptanalisis diferensial

Lakukan Kriptanalisis menggunakan CrypTool:

- CrypTool adalah program freeware yang memungkinkan Anda untuk menerapkan dan menganalisis mekanisme kriptografi, dan memiliki tampilan dan nuansa aplikasi Windows modern. CrypTool mencakup beragam fungsi kri

ptografi mutakhir dan memungkinkan Anda untuk belajar dan menggunakan kriptografi dalam lingkungan yang sama. CrypTool adalah aplikasi e-learning gratis dan open-source yang digunakan dalam implementasi dan analisis algoritma kriptografi.

Lakukan Kriptanalisis menggunakan AlphaPeeler:

- AlphaPeeler adalah alat yang kuat untuk belajar kriptologi. Ini dapat berguna sebagai alat bantu pengajaran instruktur dan untuk membuat tugas untuk kriptografi klasik. Anda dapat dengan mudah belajar teknik klasik seperti analisis frekuensi alfabet, substitusi mono-alfabet, sandi Caesar, sandi transposisi, sandi Vigenere, dan sandi Playfair. AlphaPeeler Professional (ditenagai oleh pustaka crypto++) juga mencakup DES, Gzip/Gunzip, MD5, SHA-1, SHA-256, RIPEMD-16, generasi kunci RSA, kriptografi RSA, tanda tangan & validasi RSA, dan pembuatan file saham rahasia.
