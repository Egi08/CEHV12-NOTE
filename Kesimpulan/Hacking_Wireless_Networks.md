# Peretasan Jaringan Nirkabel
> Jaringan nirkabel adalah sistem komunikasi data yang tidak terbatas yang menggunakan teknologi radio frekuensi untuk berkomunikasi dengan perangkat dan mendapatkan data. Melalui teknologi radio frekuensi, Wi-Fi memungkinkan perangkat untuk mengakses jaringan nirkabel tanpa kabel dari mana saja dalam jangkauan titik akses. Jaringan nirkabel dapat rentan terhadap berbagai jenis serangan, termasuk serangan kontrol akses, serangan integritas, serangan kerahasiaan, serangan ketersediaan, dan serangan otentikasi.


Ikhtisar Jaringan Nirkabel:
- Dalam jaringan nirkabel, komunikasi terjadi melalui transmisi gelombang radio, yang biasanya terjadi pada lapisan fisik struktur jaringan. Berkat revolusi komunikasi nirkabel, terjadi perubahan mendasar dalam jaringan data dan telekomunikasi. Ini berarti Anda perlu mengetahui dan memahami beberapa jenis jaringan nirkabel. Ini termasuk:
  - Perluasan ke jaringan kabel: Jaringan kabel diperluas dengan memperkenalkan titik akses antara jaringan kabel dan perangkat nirkabel
  - Titik akses multipel: Titik akses multipel menghubungkan komputer secara nirkabel
  - Jaringan nirkabel LAN-ke-LAN: Semua titik akses perangkat keras memiliki kemampuan untuk saling terhubung dengan titik akses perangkat keras lainnya
  - Hotspot 3G/4G: Perangkat seluler membagikan data seluler secara nirkabel dengan perangkat yang dilengkapi Wi-Fi seperti pemutar MP3, notebook, tablet, kamera, PDA, dan netbook


Ikhtisar Analisis Lalu Lintas Nirkabel:
- Analisis lalu lintas nirkabel membantu dalam menentukan strategi yang tepat untuk serangan yang berhasil. Protokol Wi-Fi unik pada Layer 2, dan lalu lintas udara tidak diserialkan, yang membuatnya mudah untuk menangkap dan menganalisis paket nirkabel. Anda dapat menggunakan berbagai alat sniffing paket Wi-Fi untuk menangkap dan menganalisis lalu lintas jaringan nirkabel target.


Ada beberapa jenis serangan Wi-Fi yang berbeda yang digunakan oleh penyerang untuk menyadap koneksi jaringan nirkabel untuk mendapatkan informasi sensitif seperti kata sandi, kredensial perbankan, dan catatan medis, serta untuk menyebarkan malware.

Ini termasuk:
- Serangan fragmentasi: Ketika berhasil, serangan seperti ini dapat memperoleh 1.500 byte PRGA (algoritma generasi pseudo acak)
- Serangan pemalsuan MAC: Penyerang mengubah alamat MAC mereka menjadi milik pengguna yang terotentikasi untuk melewati konfigurasi filtrasi MAC titik akses
- Serangan putus hubungan: Penyerang membuat korban tidak tersedia bagi perangkat nirkabel lainnya dengan menghancurkan koneksi antara titik akses dan klien
- Serangan Deautentikasi: Penyerang membanjiri stasiun dengan paket deautentikasi palsu untuk memutuskan hubungan pengguna dari titik akses
- Serangan Man-in-the-middle: Serangan Internet aktif di mana penyerang mencoba untuk menyadap, membaca, atau mengubah informasi antara dua komputer
- Serangan keracunan ARP nirkabel: Teknik serangan yang mengeksploitasi kurangnya mekanisme verifikasi dalam protokol ARP dengan merusak cache ARP yang dipelihara oleh OS untuk mengaitkan alamat MAC penyerang dengan host target
- Titik akses liar: Titik akses nirkabel yang dipasang oleh penyerang di jaringan tanpa izin dan tidak berada di bawah pengelolaan administrator jaringan
- Kembar jahat: Sebuah titik akses nirkabel palsu yang berpura-pura menjadi titik akses yang sah dengan meniru nama jaringan lainnya
- Serangan Wi-Jacking: Sebuah metode yang digunakan oleh penyerang untuk mendapatkan akses ke sejumlah besar jaringan nirkabel


Retas jaringan WEP menggunakan Aircrack-ng:
- Aircrack-ng adalah suite perangkat lunak jaringan yang terdiri dari detektor, sniffer paket, retas WEP, dan alat analisis untuk jaringan nirkabel 802.11. Program ini dapat dijalankan baik di Linux maupun Windows.
- `aircrack-ng '/home/penyerang/Desktop/Sample Captures/WEPcrack-01.cap' `


Retas jaringan WPA2 menggunakan Aircrack-ng:
- WPA2 adalah peningkatan dari WPA; itu termasuk dukungan wajib untuk Mode Penghitung dengan Protokol Kode Blok Enkripsi (CCMP), protokol enkripsi berbasis AES dengan keamanan yang kuat. WPA2 memiliki dua mode operasi: WPA2-Personal dan WPA2-Enterprise. Meskipun lebih kuat dari WEP dan WPA, metode enkripsi WPA2 juga dapat diretas menggunakan berbagai teknik dan alat.

- `aircrack-ng -a2 -b [BSSID Target] -w /home/penyerang/Desktop/Wordlist/password.txt '/home/penyerang/Desktop/Sample Captures/WPA2crack-01.cap' `
  - -a adalah teknik yang digunakan untuk meretas handshake, 2=teknik WPA.
  - -b mengacu pada bssid; ganti dengan BSSID dari router target.
  - -w adalah wordlist; berikan jalur ke wordlist.


--------------------------------------

-> Mendekripsi lalu lintas wifi: Wireshark > Edit > Preferensi > Protokol > IEEE 802.11 > tambahkan kunci WPA(sandi)
