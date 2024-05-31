# Penolakan Layanan

- Serangan DoS adalah jenis pelanggaran keamanan yang umumnya tidak mengakibatkan pencurian informasi. Namun, serangan-serangan ini dapat merugikan target dalam hal waktu dan sumber daya. Selain itu, kegagalan untuk melindungi terhadap serangan-serangan semacam itu bisa berarti hilangnya layanan seperti surel. Dalam skenario terburuk, serangan DoS bisa berarti penghancuran secara tidak sengaja dari file dan program jutaan orang yang sedang berselancar di Web pada saat serangan terjadi.
- Beberapa contoh jenis serangan DoS:
  - Membanjiri sistem korban dengan lalu lintas lebih dari yang dapat ditangani
  - Membanjiri suatu layanan (seperti obrolan relay internet (IRC)) dengan lebih banyak peristiwa daripada yang dapat ditangani
  - Menyebabkan kegagalan pada stack protokol kontrol transmisi (TCP)/protokol internet (IP) dengan mengirim paket yang korup
  - Menyebabkan kegagalan pada layanan dengan berinteraksi dengannya secara tidak terduga
  - Menggantungkan sebuah sistem dengan menyebabkannya masuk ke dalam loop tak berujung

Serangan DoS dan DDoS telah menjadi populer, karena mudahnya aksesibilitas rencana eksploitasi dan jumlah pemikiran yang tidak signifikan yang diperlukan saat melaksanakannya. Serangan-serangan ini bisa sangat berbahaya, karena mereka dapat dengan cepat menghabiskan host-host terbesar di Internet, menjadikannya tidak berguna. Dampak dari serangan-serangan ini termasuk kehilangan citra baik, jaringan yang dinonaktifkan, kerugian finansial, dan organisasi yang dinonaktifkan.

Serangan DoS dan DDoS:

- Serangan DDoS terutama bertujuan pada bandwidth jaringan; mereka menghabiskan sumber daya jaringan, aplikasi, atau layanan, dan dengan demikian membatasi pengguna yang sah dari mengakses sumber daya sistem atau jaringan mereka.

Secara umum, berikut adalah kategori-kategori vektor serangan DoS/DDoS:

- Serangan Volumetrik: Menghabiskan bandwidth jaringan atau layanan target
- Teknik serangan:
  - Serangan banjir UDP
  - Serangan banjir ICMP
  - Serangan ping of death dan smurf
  - Gelombang pulsa dan serangan zero-day
- Serangan Protokol: Menghabiskan sumber daya seperti tabel status koneksi yang ada pada komponen infrastruktur jaringan seperti penyeimbang beban, firewall, dan server aplikasi
- Teknik serangan:
  - Serangan banjir SYN
  - Serangan fragmentasi
  - Serangan banjir sesi palsu
  - Serangan banjir ACK

- Serangan Lapisan Aplikasi: Menghabiskan sumber daya atau layanan aplikasi, sehingga membuatnya tidak tersedia untuk pengguna sah lainnya
- Teknik serangan:
  - Serangan GET/POST HTTP
  - Serangan Slowloris
  - Serangan banjir lapisan aplikasi UDP
  - Serangan ekstorsi DDoS

Serangan DoS (Banjir SYN):

- Banjir SYN memanfaatkan kelemahan sehubungan dengan cara sebagian besar host mengimplementasikan tiga langkah jabat tangan TCP. Serangan ini terjadi ketika penyerang mengirim paket SYN (permintaan) tanpa batas ke sistem host. Proses pengiriman paket-paket tersebut lebih cepat daripada yang dapat ditangani oleh sistem. Biasanya, koneksi akan dibentuk dengan tiga langkah jabat tangan TCP, dan host akan melacak koneksi-koneksi yang sebagian terbuka sambil menunggu dalam antrian mendengarkan untuk paket ACK respons.

Melakukan Serangan DoS menggunakan Raven-storm:

- Raven-Storm adalah alat DDoS untuk pengujian penetrasi yang memiliki serangan Lapisan 3, Lapisan 4, dan Lapisan 7. Ini ditulis dalam python3 dan efektif serta kuat dalam menonaktifkan host dan server. Ini dapat digunakan untuk melakukan serangan kuat dan dapat dioptimalkan untuk target yang tidak lazim.

Melakukan Serangan DDoS menggunakan HOIC:

- HOIC (High Orbit Ion Cannon) adalah aplikasi serangan tekanan jaringan dan DoS/DDoS. Alat ini ditulis dalam bahasa BASIC. Ini dirancang untuk menyerang hingga 256 URL target secara bersamaan. Ini mengirim permintaan HTTP, POST, dan GET ke komputer yang menggunakan GUI terinspirasi lulz. Ini menawarkan Banjir HTTP multi-threading berkecepatan tinggi; sistem scripting bawaan memungkinkan implementasi "penggembira," yang merupakan skrip yang dirancang untuk menggagalkan tindakan antisipasi DDoS dan meningkatkan output DoS.

Melakukan Serangan DDoS menggunakan LOIC:

- LOIC (Low Orbit Ion Cannon) adalah aplikasi pengujian tekanan jaringan dan serangan DoS. Kita juga bisa menyebutnya sebagai serangan DoS berbasis aplikasi karena sebagian besar menargetkan aplikasi web. Kita dapat menggunakan LOIC pada situs target untuk membanjiri server dengan paket TCP, paket UDP, atau permintaan HTTP dengan tujuan mengganggu layanan dari host tertentu.

Deteksi dan Perlindungan Terhadap Serangan DDoS menggunakan Anti DDoS Guardian:

- Anti DDoS Guardian adalah alat perlindungan serangan DDoS. Ini melindungi server IIS, server Apache, server game, server Camfrog, server surel, server FTP, PBX VOIP, dan server SIP, dan sistem lainnya. Anti DDoS Guardian memonitor setiap paket masuk dan keluar secara Real-Time. Ini menampilkan alamat lokal, alamat remote, dan informasi lain dari setiap aliran jaringan. Anti DDoS Guardian membatasi jumlah aliran jaringan, bandwidth klien, jumlah koneksi TCP bersamaan klien, dan laju koneksi TCP. Ini juga membatasi bandwidth UDP, laju koneksi UDP, dan laju paket UDP.
