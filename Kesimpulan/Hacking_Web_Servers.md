# Membobol Server Web

> Sebuah server web adalah sistem komputer yang menyimpan, memproses, dan mengirimkan halaman web kepada klien global melalui protokol HTTP. Serangan terhadap server web umumnya melibatkan aktivitas yang direncanakan sebelumnya, disebut sebagai metodologi serangan, yang dilakukan oleh penyerang untuk mencapai tujuan mereka dalam meretas keamanan server web target.

Ikhtisar Server Web:

- Sebagian besar orang berpikir bahwa server web hanya berupa perangkat keras, namun sebuah server web juga mencakup aplikasi perangkat lunak. Secara umum, sebuah klien memulai proses komunikasi melalui permintaan HTTP. Ketika seorang klien ingin mengakses sumber daya seperti halaman web, foto, atau video, maka browser klien akan menghasilkan permintaan HTTP ke server web. Bergantung pada permintaan tersebut, server web mengumpulkan informasi atau konten yang diminta dari penyimpanan data atau server aplikasi dan memberikan respons kepada permintaan klien dengan respons HTTP yang sesuai. Jika server web tidak dapat menemukan informasi yang diminta, maka server tersebut akan menghasilkan pesan kesalahan.

Jejak Server Web:

- Dengan melakukan jejak server web, dimungkinkan untuk mengumpulkan data tingkat sistem yang berharga seperti detail akun, OS, versi perangkat lunak, nama server, dan detail skema database. Gunakan utilitas Telnet untuk melakukan jejak pada server web dan mengumpulkan informasi seperti nama server, jenis server, sistem operasi, dan aplikasi yang berjalan. Gunakan alat jejak seperti Netcraft, ID Serve, dan httprecon untuk melakukan jejak server web. Alat jejak server web seperti Netcraft, ID Serve, dan httprecon dapat mengekstrak informasi dari server target. Mari kita lihat fitur dan jenis informasi apa yang dapat dikumpulkan oleh alat-alat ini dari server target.

Pengumpulan Informasi menggunakan Ghost Eye:

- Ghost Eye adalah alat pengumpulan informasi yang ditulis dalam Python 3. Untuk dijalankan, Ghost Eye hanya memerlukan domain atau IP. Ghost Eye dapat berfungsi dengan distro Linux apa pun jika mendukung Python 3.
- Ghost Eye mengumpulkan informasi seperti pencarian Whois, pencarian DNS, EtherApe, pemindaian port Nmap, pengambil header HTTP, tes Clickjacking, pemindai Robots.txt, pengambil link, penemuan lokasi IP, dan traceroute.

Lakukan Pencarian Server Web menggunakan Skipfish:

- Skipfish adalah alat pengintaian keamanan aplikasi web aktif (dipasang di server web). Ini membuat peta situs interaktif untuk situs yang ditargetkan dengan melakukan penggelaran merangkak rekursif dan penyelidikan berbasis kamus. Peta yang dihasilkan kemudian dianotasi dengan output dari sejumlah pemeriksaan keamanan aktif (tetapi semoga tidak mengganggu). Laporan akhir yang dihasilkan oleh alat ini dimaksudkan untuk menjadi dasar untuk penilaian keamanan aplikasi web profesional.

Jejak Server Web menggunakan Alat httprecon:

- Aplikasi web dapat mempublikasikan informasi, berinteraksi dengan pengguna Internet, dan membentuk kehadiran e-commerce atau e-government. Namun, jika sebuah organisasi tidak tegas dalam mengkonfigurasi dan mengoperasikan situs web publiknya, maka organisasi tersebut rentan terhadap berbagai ancaman keamanan. Meskipun ancaman di dunia maya sebagian besar tetap sama seperti di dunia fisik (penipuan, pencurian, vandalisme, dan terorisme), mereka jauh lebih berbahaya. Organisasi dapat menghadapi kerugian finansial, kerusakan reputasi, dan tindakan hukum jika seorang penyusup berhasil melanggar kerahasiaan data mereka.
- httprecon adalah alat untuk jejak lanjutan pada server web. Alat ini melakukan serangan pengambil banner, enumerasi kode status, dan analisis pemesanan header pada server web target.

Retas Kredensial FTP menggunakan Serangan Kamus:

- Sebuah kamus atau daftar kata-kata berisi ribuan kata yang digunakan oleh alat pemecah sandi untuk membobol sistem yang dilindungi kata sandi. Seorang penyerang dapat entah secara manual membobol kata sandi dengan menebaknya atau menggunakan alat dan teknik otomatis seperti metode kamus. Sebagian besar teknik pembobolan kata sandi berhasil, karena kata sandi yang lemah atau mudah ditebak.
- hydra -L /home/attacker/Desktop/Wordlists/Usernames.txt -P /home/attacker/Desktop/Wordlists/Passwords.txt ftp://[Alamat IP Windows 11]
