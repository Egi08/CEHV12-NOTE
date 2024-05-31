# Sniffing
> Sniffing paket adalah proses pemantauan dan penangkapan semua paket data yang melewati suatu jaringan tertentu menggunakan aplikasi perangkat lunak atau perangkat keras.

Sniffing Jaringan:
- Sniffing sederhana dalam jaringan berbasis hub, karena lalu lintas pada segmen melewati semua host yang terhubung dengan segmen itu. Namun, sebagian besar jaringan saat ini menggunakan switch. Switch adalah perangkat jaringan komputer canggih. Perbedaan utama antara hub dan switch adalah bahwa hub mengirimkan data garis ke setiap port pada mesin dan tidak memiliki pemetaan garis, sedangkan switch melihat alamat Media Access Control (MAC) yang terkait dengan setiap frame yang melewati switch dan mengirimkan data ke port yang diperlukan. Alamat MAC adalah alamat perangkat keras yang secara unik mengidentifikasi setiap node dari sebuah jaringan.

- Packet sniffer digunakan untuk mengonversi NIC sistem host ke mode promiskuitas. NIC dalam mode promiskuitas kemudian dapat menangkap paket yang ditujukan ke jaringan tertentu. Ada dua jenis sniffing. Masing-masing digunakan untuk jenis jaringan yang berbeda. Dua jenis tersebut adalah:
  - **Sniffing Pasif**: Sniffing pasif melibatkan pengiriman paket. Ini hanya menangkap dan memantau paket yang mengalir dalam jaringan
  - **Sniffing Aktif**: Sniffing aktif mencari lalu lintas pada LAN yang beralih dengan secara aktif menyuntikkan lalu lintas ke LAN; ini juga merujuk pada sniffing melalui switch

Ikhtisar Sniffing Aktif:

- Sniffing aktif melibatkan pengiriman beberapa probe jaringan untuk mengidentifikasi titik akses. Berikut adalah daftar teknik sniffing aktif yang berbeda:
- Pembanjiran MAC: Melibatkan pembanjiran tabel CAM dengan pasangan alamat MAC palsu dan IP sampai penuh
- Pemalsuan DNS: Melibatkan menipu server DNS untuk percaya bahwa telah menerima informasi otentik ketika, pada kenyataannya, tidak
- Pemalsuan ARP: Melibatkan pembuatan sejumlah besar permintaan ARP palsu dan balasan untuk membebani switch
- Serangan DHCP: Melibatkan melakukan serangan kelaparan DHCP dan serangan server DHCP nakal
- Pencurian port switch: Melibatkan pembanjiran switch dengan paket ARP gratuitous palsu dengan alamat MAC target sebagai sumber
- Serangan Pemalsuan: Melibatkan melakukan pemalsuan MAC, lompatan VLAN, dan serangan STP untuk mencuri informasi sensitif

Pembanjiran MAC menggunakan macof:
- Pembanjiran MAC adalah teknik yang digunakan untuk mengompromi keamanan switch jaringan yang menghubungkan segmen jaringan atau perangkat jaringan. Penyerang menggunakan teknik pembanjiran MAC untuk memaksa switch bertindak sebagai hub, sehingga mereka dapat dengan mudah mencium lalu lintas.
- macof adalah alat Unix dan Linux yang merupakan bagian dari koleksi dsniff. Ini membanjiri jaringan lokal dengan alamat MAC dan alamat IP acak, menyebabkan beberapa switch gagal dan membuka dalam mode pengulangan, sehingga memudahkan sniffing. Alat ini membanjiri tabel CAM switch (131.000 per menit) dengan mengirimkan entri MAC palsu. Ketika tabel MAC penuh, switch mengonversi ke operasi seperti hub di mana penyerang dapat memantau data yang disiarkan.
- macof -i eth0 -d [Alamat IP Target]

Serangan Kelaparan DHCP menggunakan Yersinia:
- Dalam serangan kelaparan DHCP, seorang penyerang membanjiri server DHCP dengan mengirim sejumlah besar permintaan DHCP dan menggunakan semua alamat IP yang tersedia yang dapat dikeluarkan oleh server DHCP. Akibatnya, server tidak dapat mengeluarkan alamat IP lainnya, mengakibatkan serangan Denial-of-Service (DoS). Karena masalah ini, pengguna yang valid tidak dapat memperoleh atau memperbarui alamat IP mereka, dan dengan demikian gagal mengakses jaringan mereka. Serangan ini dapat dilakukan dengan menggunakan berbagai alat seperti Yersinia dan Hyenae.
- Yersinia adalah alat jaringan yang dirancang untuk memanfaatkan kelemahan dalam berbagai protokol jaringan seperti DHCP. Ini berpura-pura menjadi kerangka kerja yang solid untuk menganalisis dan menguji jaringan dan sistem yang diterapkan.
- yersinia -I 

Pemalsuan ARP menggunakan arpspoof:
- Pemalsuan ARP adalah metode menyerang Ethernet LAN. Pemalsuan ARP berhasil dengan mengubah alamat IP komputer penyerang ke alamat IP komputer target. Permintaan ARP dan balasan palsu menemukan tempat di cache ARP target dalam proses ini. Karena balasan ARP telah dipalsukan, komputer tujuan (target) mengirimkan frame ke komputer penyerang, di mana penyerang dapat memodifikasinya sebelum mengirimkannya ke mesin sumber (Pengguna A) dalam serangan MITM.
- arpspoof mengalihkan paket dari host target (atau semua host) di LAN yang ditujukan untuk host lain di LAN dengan memalsukan balasan ARP. Ini adalah cara yang sangat efektif untuk mencium lalu lintas pada sebuah switch.
- arpspoof -i eth0 -t 10.10.1.1 10.10.1.11 
  - Di sini, 10.10.1.11 adalah alamat IP sistem target [Windows 11], dan 10.10.1.1 adalah alamat IP titik akses atau gateway
  - -i: menentukan antarmuka jaringan dan -t: menentukan alamat IP target.


Serangan Man-in-the-Middle (MITM) menggunakan Cain & Abel:
- Seorang penyerang dapat memperoleh nama pengguna dan kata sandi menggunakan berbagai teknik atau dengan menangkap paket data. Dengan hanya menangkap cukup paket, penyerang dapat mengekstrak nama pengguna dan kata sandi target jika korban mengautentikasi diri di jaringan publik, terutama di situs web yang tidak aman. Begitu kata sandi berhasil diretas, penyerang dapat menggunakan kata sandi tersebut untuk menggang

gu akun korban seperti dengan masuk ke akun email korban, masuk ke PayPal dan menguras rekening bank korban, atau bahkan mengubah kata sandi.
- Serangan MITM digunakan untuk menyusup ke dalam koneksi yang ada antara sistem dan untuk menyadap pesan yang pertukarannya. Dengan menggunakan berbagai teknik, penyerang membagi koneksi TCP menjadi dua koneksi—koneksi klien-ke-penyerang dan koneksi penyerang-ke-server. Setelah intersepsi koneksi TCP berhasil, penyerang dapat membaca, memodifikasi, dan menyisipkan data palsu ke dalam komunikasi yang disadap.
- Serangan MITM bervariasi dan dapat dilakukan pada LAN yang beralih. Serangan MITM dapat dilakukan menggunakan berbagai alat seperti Cain & Abel.
- Cain & Abel adalah alat pemulihan kata sandi yang memungkinkan pemulihan kata sandi dengan mencium jaringan dan meretas kata sandi terenkripsi. Fitur pemalsuan ARP dari alat Cain & Abel melibatkan mengirimkan ARP palsu gratis ke korban host jaringan. ARP palsu ini dapat memudahkan untuk menyerang seorang perantara.


Pemalsuan Alamat MAC menggunakan TMAC dan SMAC:
- Serangan pemalsuan atau duplikasi MAC melibatkan mencium jaringan untuk alamat MAC dari klien sah yang terhubung ke jaringan. Dalam serangan ini, penyerang pertama-tama mendapatkan alamat MAC klien yang terhubung dengan port switch secara aktif. Kemudian, penyerang memalsukan alamat MAC mereka sendiri dengan alamat MAC klien yang sah. Begitu pemalsuan berhasil, penyerang menerima semua lalu lintas yang ditujukan ke klien. Dengan demikian, seorang penyerang dapat mengakses jaringan dan mengambil alih identitas pengguna jaringan.


Pemalsuan Alamat MAC Mesin Linux menggunakan macchanger:
- Alamat MAC adalah nomor unik yang dapat diberikan kepada setiap antarmuka jaringan, dan digunakan oleh berbagai program sistem dan protokol untuk mengidentifikasi antarmuka jaringan. Tidak mungkin untuk mengubah alamat MAC yang telah tertanam keras di NIC (kontroller antarmuka jaringan). Namun banyak driver yang memungkinkan untuk mengubah alamat MAC. Beberapa alat dapat membuat sistem operasi percaya bahwa NIC memiliki alamat MAC pilihan pengguna. Penyamaran alamat MAC dikenal sebagai pemalsuan MAC dan melibatkan mengubah identitas komputer. Pemalsuan MAC dapat dilakukan menggunakan berbagai alat.
- macchanger -a eth0
  - -a: menetapkan alamat MAC vendor acak ke antarmuka jaringan.
- macchanger -r eth0
  - atur mac secara acak

Melakukan Penciuman Kata Sandi menggunakan Wireshark:
- Wireshark adalah analisis paket jaringan yang digunakan untuk menangkap paket jaringan dan menampilkan data paket secara detail. Alat ini menggunakan Winpcap untuk menangkap paket pada jaringan yang didukungnya sendiri. Ini menangkap lalu lintas jaringan langsung dari Ethernet, IEEE 802.11, PPP/HDLC, ATM, Bluetooth, USB, Token Ring, Frame Relay, dan jaringan FDDI. File yang ditangkap dapat diedit secara terprogram melalui baris perintah. Sejumlah filter untuk tampilan data yang disesuaikan dapat disempurnakan menggunakan filter tampilan.

Menganalisis Jaringan menggunakan Analisis Protokol Jaringan Omnipeek:
- Penganalisis Jaringan OmniPeek menyediakan visibilitas real-time dan analisis ahli dari setiap bagian jaringan target. Ini melakukan analisis, mengebor, dan memperbaiki bottleneck kinerja di sejumlah segmen jaringan. Ini termasuk plug-in analitik yang menyediakan visualisasi yang ditargetkan dan kemampuan pencarian.


Mendeteksi Sniffing Jaringan:
- Sniffing jaringan melibatkan menggunakan alat sniffing yang memungkinkan pemantauan dan analisis data paket secara real-time yang mengalir melalui jaringan komputer. Sniffer jaringan ini dapat dideteksi dengan menggunakan berbagai teknik seperti:
  - Metode Ping: Mengidentifikasi apakah sistem di jaringan berjalan dalam mode promiskuitas
  - Metode DNS: Mengidentifikasi sniffers dalam jaringan dengan menganalisis peningkatan lalu lintas jaringan
  - Metode ARP: Mengirimkan ARP non-broadcast ke semua node dalam jaringan; node di jaringan yang berjalan dalam mode promiskuitas akan menyimpan cache alamat ARP lokal


Mendeteksi Pemalsuan ARP dan Mode Promiskuitas dalam Jaringan Berbasis Switch:
- Pemalsuan ARP melibatkan pemalsuan banyak permintaan ARP dan balasan untuk membebani switch. Pemalsuan cache ARP adalah metode menyerang jaringan LAN dengan memperbarui cache ARP komputer target dengan kedua permintaan ARP dan balasan ARP palsu yang dirancang untuk mengubah alamat MAC Ethernet Layer 2 (yang dari kartu jaringan) menjadi satu yang dapat dipantau oleh penyerang. Penyerang menggunakan pemalsuan ARP untuk mencium jaringan target. Penyerang dengan demikian dapat mencuri informasi sensitif, mencegah akses jaringan dan web, dan melakukan serangan DoS dan MITM.
- Mode promiskuitas memungkinkan perangkat jaringan untuk menyisipkan dan membaca setiap paket jaringan yang tiba secara utuh. Sniffer mengalihkan NIC dari suatu sistem ke mode promiskuitas, sehingga mendengarkan semua data yang ditransmisikan pada segmen tersebut. Sebuah sniffer dapat terus-menerus memantau semua lalu lintas jaringan ke komputer melalui NIC dengan mendekripsi informasi yang terenkapsulasi dalam paket data. Mode promiskuitas dalam jaringan dapat dideteksi menggunakan berbagai alat.

Analisis Jaringan Capsa:
- Capsa, alat analisis dan diagnosis kinerja jaringan yang dapat dibawa-bawa, menyediakan kemampuan tangkapan dan analisis paket dengan antarmuka yang mudah digunakan yang memungkinkan pengguna untuk melindungi dan memantau jaringan dalam lingkungan bisnis yang kritis. Ini membantu peretas etis atau pentester dalam mendeteksi dengan cepat pemalsuan ARP dan

 serangan pembanjiran ARP serta dalam menemukan sumber serangan.

Habu:
- Habu adalah toolkit pengujian penetrasi sumber terbuka yang dapat melakukan berbagai tugas seperti pemalsuan ARP, penciuman ARP, kelaparan DHCP, dan penemuan DHCP.
