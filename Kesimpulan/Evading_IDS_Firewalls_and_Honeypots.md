# Mengelabui IDS, Firewall, dan Honeypots
> Mengelabui IDS dan firewall melibatkan modifikasi serangan untuk menghindari deteksi oleh sistem keamanan organisasi, sedangkan honeypot adalah perangkap yang disiapkan untuk mendeteksi, menangkal, atau meniadakan upaya peretasan yang tidak sah.


IDS, yang memberikan lapisan keamanan tambahan bagi infrastruktur organisasi, merupakan target menarik bagi para penyerang. Penyerang mengimplementasikan berbagai teknik penyamaran IDS untuk melewati mekanisme keamanan ini dan mengompromi infrastruktur. Banyak teknik penyamaran IDS mengelak dari deteksi melalui berbagai metode dan dapat beradaptasi dengan metode terbaik untuk setiap sistem.


Firewall beroperasi berdasarkan seperangkat aturan yang telah ditentukan. Dengan pengetahuan dan keterampilan yang luas, seorang penyerang dapat melewati firewall dengan menggunakan berbagai teknik penembusan. Dengan menggunakan teknik ini, penyerang memperdaya firewall untuk tidak menyaring lalu lintas berbahaya yang dihasilkan.


 Sistem Deteksi Intrusi (IDS):
- Sistem deteksi intrusi sangat berguna karena mereka memantau kedua arus masuk dan keluar jaringan dan terus-menerus memeriksa data untuk aktivitas mencurigakan yang mungkin menunjukkan pelanggaran keamanan jaringan atau sistem. IDS memeriksa lalu lintas untuk tanda tangan yang cocok dengan pola intrusi yang diketahui dan memberikan sinyal alarm saat ada yang cocok. Ini dapat dikategorikan menjadi aktif dan pasif, tergantung pada fungsinya: IDS umumnya pasif dan digunakan untuk mendeteksi intrusi, sedangkan sistem pencegahan intrusi (IPS) dianggap sebagai IDS aktif, karena tidak hanya digunakan untuk mendeteksi intrusi di jaringan, tetapi juga mencegahnya.
- Fungsi Utama IDS:
  - Mengumpulkan dan menganalisis informasi dari dalam komputer atau jaringan, untuk mengidentifikasi pelanggaran kebijakan keamanan yang mungkin
  - Juga dikenal sebagai "packet-sniffer," yang menangkap paket yang berjalan di berbagai medium komunikasi dan protokol
  - Mengevaluasi lalu lintas untuk intrusi yang dicurigai dan memberikan sinyal alarm setelah deteksi


Deteksi Intrusi menggunakan Snort:
- Snort adalah sistem deteksi intrusi jaringan sumber terbuka, mampu melakukan analisis lalu lintas real-time dan logging paket pada jaringan IP. Ini dapat melakukan analisis protokol dan pencarian/pencocokan konten dan digunakan untuk mendeteksi berbagai serangan dan penyelidikan seperti buffer overflows, pemindaian port stealth, serangan CGI, penyelidikan SMB, dan percobaan fingerprint OS. Ini menggunakan bahasa aturan fleksibel untuk menjelaskan lalu lintas untuk dikumpulkan atau dilewatkan, serta mesin deteksi yang menggunakan arsitektur plug-in modular.
- Penggunaan Snort:
  - Sniffer paket lurus seperti tcpdump
  - Logger paket (berguna untuk debugging lalu lintas jaringan, dll.)
  - Sistem pencegahan intrusi jaringan


Deteksi Lalu Lintas Jaringan Berbahaya menggunakan ZoneAlarm FREE FIREWALL:
- ZoneAlarm FREE Firewall menghalangi penyerang dan intruder dari mengakses sistem Anda. Ini mengelola dan memantau semua lalu lintas masuk dan keluar dan melindungi jaringan dari peretas, malware, dan ancaman online lainnya yang mengancam privasi jaringan, dan memantau program-program untuk perilaku yang mencurigakan dengan mendeteksi dan menghentikan serangan baru yang melewati perlindungan antivirus tradisional. Firewall ini mencegah pencurian identitas dengan menjaga data Anda, dan menghapus jejak Anda memungkinkan Anda menjelajahi web dengan privasi lengkap. Selain itu, itu mengunci para penyerang, memblokir intrusi, dan membuat PC Anda tidak terlihat secara online. Selain itu, itu menyaring email yang mengganggu, serta berpotensi berbahaya.


Deteksi Lalu Lintas Jaringan Berbahaya menggunakan HoneyBOT:
- HoneyBOT adalah honeypot interaksi menengah untuk Windows. Sebuah honeypot menciptakan lingkungan aman untuk menangkap dan berinteraksi dengan lalu lintas yang tidak diminta di jaringan. HoneyBOT adalah solusi yang mudah digunakan yang ideal untuk penelitian keamanan jaringan atau sebagai bagian dari IDS peringatan dini.


Teknik Penyamaran Firewall:
- Sebuah firewall beroperasi berdasarkan seperangkat aturan yang telah ditentukan. Dengan pengetahuan dan keterampilan yang luas, seorang penyerang dapat melewati firewall dengan menggunakan berbagai teknik penembusan. Dengan menggunakan teknik ini, penyerang memperdaya firewall untuk tidak menyaring lalu lintas berbahaya yang dihasilkan olehnya.
- Berikut adalah beberapa teknik penembusan firewall
  - Pemindaian Port
  - Firewalking
  - Pemanggilan Banner
  - Pemalsuan Alamat IP
  - Source Routing
  - Fragmen Kecil
  - Menggunakan Alamat IP sebagai Pengganti URL
  - Menggunakan Situs Web Surfing Anonim
  - Menggunakan Server Proxy
  - ICMP Tunneling
  - ACK Tunneling
  - HTTP Tunneling
  - SSH Tunneling
  - DNS Tunneling
  - Melalui Sistem Eksternal
  - Melalui Serangan MITM
  - Melalui Konten
  - Melalui Serangan XSS


Melewati Aturan Firewall menggunakan HTTP/FTP Tunneling:
- Teknologi tunneling HTTP memungkinkan penyerang untuk melakukan berbagai tugas Internet meskipun pembatasan yang diberlakukan oleh firewall. Metode ini dapat diimplementasikan jika perusahaan target memiliki server web publik dengan port 80 yang digunakan untuk lalu lintas HTTP yang tidak difilter oleh firewall-nya. Teknologi ini mengkapsulasi data di dalam lalu lintas HTTP (port 80). Banyak firewall tidak memeriksa payload paket HTTP untuk memastikan bahwa itu sah, sehingga memungkinkan untuk menelusuri lalu lintas melalui port TCP 80.
- HTTPort memungkinkan pengguna untuk

 melewati proxy HTTP, yang memblokir akses Internet ke email, pesan instan, berbagi file P2P, ICQ, Berita, FTP, IRC, dll. Di sini, perangkat lunak Internet dikonfigurasi, sehingga terhubung ke PC lokal seolah-olah itu adalah server jarak jauh yang dibutuhkan; HTTPort kemudian menangkap koneksi itu dan menjalankannya melalui terowongan melalui proxy. HTTPort dapat berfungsi pada perangkat seperti proxy atau firewall yang memungkinkan lalu lintas HTTP. Dengan demikian, HTTPort memberikan akses ke situs web dan aplikasi Internet. HTTPort melakukan tunneling menggunakan salah satu dari dua mode: mode SSL/CONNECT dan host jarak jauh.
- Metode host jarak jauh mampu menelusuri melalui setiap proxy. HTTPort menggunakan perangkat lunak server khusus yang disebut HTTHost, yang diinstal di luar jaringan yang diblokir proxy. Ini adalah server web, dan karena itu ketika HTTPort sedang melakukan tunneling, ia mengirim serangkaian permintaan HTTP ke HTTHost. Proxy merespons seolah-olah pengguna sedang berselancar ke situs web dan dengan demikian memungkinkan pengguna untuk melakukannya. HTTHost, pada gilirannya, melakukan setengah dari tunneling dan berkomunikasi dengan server target. Mode ini jauh lebih lambat, tetapi berfungsi dalam sebagian besar kasus dan fitur enkripsi data yang kuat yang membuat logging proxy tidak berguna.


Melewati Antivirus menggunakan Template Metasploit:
- Perangkat lunak antivirus dirancang untuk mendeteksi proses atau file berbahaya dan mencegah eksekusinya di ujung. Ada berbagai teknik yang dapat digunakan untuk melewati antivirus dan menjalankan proses berbahaya di mesin target.


Melewati Firewall melalui Windows BITSAdmin:
- BITS (Background Intelligent Transfer Service) adalah komponen penting dari Windows XP dan versi Windows setelahnya. BITS digunakan oleh administrator sistem dan programmer untuk men-download file dari atau meng-upload file ke server web HTTP dan berbagi file SMB. BITSAdmin adalah alat yang digunakan untuk membuat pekerjaan download atau upload dan memantau kemajuannya.
