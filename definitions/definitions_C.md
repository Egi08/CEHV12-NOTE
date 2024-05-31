# Definisi C

## Certificate Authority / Otoritas Sertifikat

Dalam kriptografi, otoritas sertifikat atau otoritas sertifikasi (CA) adalah entitas yang menyimpan, menandatangani, dan mengeluarkan sertifikat digital.
Sertifikat digital mengesahkan kepemilikan kunci publik oleh subjek sertifikat yang disebutkan.
Hal ini memungkinkan orang lain (pihak yang mengandalkan) untuk mengandalkan tanda tangan atau pernyataan yang dibuat tentang kunci privat yang sesuai dengan kunci publik bersertifikat.

Links:

- [https://en.wikipedia.org/wiki/Certificate_authority](https://en.wikipedia.org/wiki/Certificate_authority)

## CIA Triad/ Tiga Serangkai CIA

Fokus utama keamanan informasi adalah perlindungan yang seimbang terhadap kerahasiaan, integritas, dan ketersediaan data (juga dikenal sebagai triad CIA) sambil mempertahankan fokus pada implementasi kebijakan yang efisien, semuanya tanpa menghambat produktivitas organisasi.

### Confidentiality/ Kerahasiaan

Melibatkan seperangkat aturan atau janji yang biasanya dilaksanakan melalui perjanjian kerahasiaan yang membatasi akses atau menempatkan pembatasan pada jenis informasi tertentu.

### Integrity/ Integritas

Berarti memelihara dan memastikan keakuratan dan kelengkapan data selama seluruh siklus hidupnya.

### Availability/ Ketersediaan

Untuk setiap sistem informasi untuk melayani tujuannya, informasi harus tersedia ketika dibutuhkan. Ini berarti sistem komputasi yang digunakan untuk menyimpan dan memproses informasi, kontrol keamanan yang digunakan untuk melindunginya, dan saluran komunikasi yang digunakan untuk mengaksesnya harus berfungsi dengan benar.

Links:

- [https://en.wikipedia.org/wiki/Confidentiality](https://en.wikipedia.org/wiki/Confidentiality)

## Cipher

Dalam kriptografi, cipher (atau cypher) adalah algoritma untuk melakukan enkripsi atau dekripsi — serangkaian langkah yang terdefinisi dengan baik yang dapat diikuti sebagai prosedur.

### Substitution cipher/ Cipher substitusi

Dalam kriptografi, cipher substitusi adalah metode enkripsi di mana unit plaintext diganti dengan ciphertext, dengan cara yang ditentukan, dengan bantuan kunci; "Satuan" mungkin huruf tunggal (yang paling umum), pasangan huruf, kembar tiga huruf, campuran di atas, dan sebagainya. Penerima menguraikan teks dengan melakukan proses substitusi terbalik untuk mengekstrak pesan asli.

Contoh sandi substitusi adalah sandi Caesar.

### Transposition cipher/ Sandi transposisi

Dalam kriptografi, cipher transposisi adalah metode enkripsi yang mengacak posisi karakter (transposisi) tanpa mengubah karakter itu sendiri.

### Block cipher/ Blokir cipher

Dalam kriptografi, cipher blok adalah algoritma deterministik yang beroperasi pada kelompok bit dengan panjang tetap, yang disebut blok. Mereka ditentukan komponen dasar dalam desain banyak protokol kriptografi dan banyak digunakan untuk mengenkripsi sejumlah besar data, termasuk dalam protokol pertukaran data. Ini menggunakan blok sebagai transformasi yang tidak berubah.

### Stream cipher/ Streaming cipher

Stream cipher adalah cipher kunci simetris di mana digit plaintext digabungkan dengan stream digit cipher pseudorandom (keystream).

Links:

- [https://en.wikipedia.org/wiki/Cipher](https://en.wikipedia.org/wiki/Cipher)
- [https://en.wikipedia.org/wiki/Substitution_cipher](https://en.wikipedia.org/wiki/Substitution_cipher)
- [https://en.wikipedia.org/wiki/Caesar_cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
- [https://en.wikipedia.org/wiki/Transposition_cipher](https://en.wikipedia.org/wiki/Transposition_cipher)
- [https://en.wikipedia.org/wiki/Stream_cipher](https://en.wikipedia.org/wiki/Stream_cipher)

## Cipher Block Chaining/ Rantai Blok Cipher

Ehrsam, Meyer, Smith dan Tuchman menemukan mode operasi cipher block chaining (CBC) pada tahun 1976.
Dalam mode CBC, setiap blok plaintext di-XORed dengan blok ciphertext sebelumnya sebelum dienkripsi.
Dengan cara ini, setiap blok ciphertext bergantung pada semua blok plaintext yang diproses hingga saat itu.

## Clickjacking/ Pembajakan klik

Clickjacking (diklasifikasikan sebagai serangan ganti rugi antarmuka pengguna atau ganti rugi UI) adalah teknik jahat menipu pengguna agar mengklik sesuatu yang berbeda dari apa yang dirasakan pengguna, sehingga berpotensi mengungkapkan informasi rahasia atau memungkinkan orang lain mengendalikan komputer mereka sambil mengklik objek yang tampaknya tidak berbahaya, termasuk halaman web.

Links:

- [https://en.wikipedia.org/wiki/Clickjacking](https://en.wikipedia.org/wiki/Clickjacking)

## Cloud Computing/ Komputasi Awan

Cloud computing adalah ketersediaan sumber daya sistem komputer sesuai permintaan, terutama penyimpanan data (cloud storage) dan daya komputasi, tanpa manajemen aktif langsung oleh pengguna.
Awan besar sering memiliki fungsi yang didistribusikan di beberapa lokasi, yang masing-masing merupakan pusat data.

### Public cloud/ Cloud publik

Layanan cloud dianggap "publik" ketika dikirimkan melalui Internet publik, dan dapat ditawarkan sebagai langganan berbayar, atau gratis.

### Private cloud / Awan pribadi

Private cloud adalah infrastruktur cloud yang dioperasikan semata-mata untuk satu organisasi, baik dikelola secara internal atau oleh pihak ketiga, dan dihosting baik secara internal maupun eksternal.

### Hybrid cloud

Cloud hibrida adalah komposisi cloud publik dan lingkungan pribadi, seperti cloud pribadi atau sumber daya lokal,[100],[101] yang tetap menjadi entitas yang berbeda tetapi terikat bersama, menawarkan manfaat dari beberapa model penyebaran.

### Community cloud / Cloud komunitas

Cloud komunitas berbagi infrastruktur antara beberapa organisasi dari komunitas tertentu dengan masalah umum (keamanan, kepatuhan, yurisdiksi, dll.), Baik dikelola secara internal atau oleh pihak ketiga, dan dihosting secara internal atau eksternal.

### Infrastructure as a service/ Infrastruktur sebagai layanan

"Infrastruktur sebagai layanan" (IaaS) mengacu pada layanan online yang menyediakan API tingkat tinggi yang digunakan untuk mengabstraksi berbagai detail tingkat rendah dari infrastruktur jaringan yang mendasarinya seperti sumber daya komputasi fisik, lokasi, partisi data, penskalaan, keamanan, cadangan, dll.

### Platform as a service /  Platform sebagai layanan

Kemampuan yang diberikan kepada konsumen adalah untuk menyebarkan ke infrastruktur cloud aplikasi yang dibuat atau diperoleh konsumen yang dibuat menggunakan bahasa pemrograman, pustaka, layanan, dan alat yang didukung oleh penyedia.

### Software as a service/ Perangkat lunak sebagai layanan

Kemampuan yang diberikan kepada konsumen adalah menggunakan aplikasi penyedia yang berjalan pada infrastruktur cloud.

Links:

- [https://en.wikipedia.org/wiki/Cloud_computing](https://en.wikipedia.org/wiki/Cloud_computing)

## Code Review / Ulasan Kode

Code review (kadang-kadang disebut sebagai peer review) adalah kegiatan jaminan kualitas perangkat lunak di mana satu atau beberapa orang memeriksa program terutama dengan melihat dan membaca bagian-bagian dari kode sumbernya, dan mereka melakukannya setelah implementasi atau sebagai gangguan implementasi.

Links

- [https://en.wikipedia.org/wiki/Code_review](https://en.wikipedia.org/wiki/Code_review)

## Common Vulnerabilities and Exposures / Kerentanan dan eksposur umum

Sistem kerentanan dan eksposur umum (CVE) menyediakan metode referensi untuk kerentanan dan eksposur keamanan informasi yang diketahui publik.

Links:

- [https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)

## Common Vulnerability Scoring System / Sistem Penilaian Kerentanan Umum

Common Vulnerability Scoring System (CVSS) adalah standar industri bebas dan terbuka untuk menilai tingkat keparahan kerentanan keamanan sistem komputer.

Links:

- [https://en.wikipedia.org/wiki/Common_Vulnerability_Scoring_System](https://en.wikipedia.org/wiki/Common_Vulnerability_Scoring_System)

## Common Weakness Enumeration / Pencacahan Kelemahan Umum

Common Weakness Enumeration (CWE) adalah sistem kategori untuk kelemahan dan kerentanan perangkat keras dan perangkat lunak.

Links:

- [https://en.wikipedia.org/wiki/Common_Weakness_Enumeration](https://en.wikipedia.org/wiki/Common_Weakness_Enumeration)

## Command and Control / Perintah dan Kontrol

Istilah ini juga umum digunakan dalam industri keamanan komputer dan dalam konteks cyberwarfare.
Di sini istilah ini mengacu pada pengaruh penyerang terhadap sistem komputer yang dikompromikan yang mereka kendalikan.

Links:

- [https://en.wikipedia.org/wiki/Command_and_control](https://en.wikipedia.org/wiki/Command_and_control)

## Command Injection /  Injeksi Perintah

Command injection adalah serangan cyber yang melibatkan eksekusi perintah sewenang-wenang pada sistem operasi host (OS).
Biasanya, aktor ancaman menyuntikkan perintah dengan mengeksploitasi kerentanan aplikasi, seperti validasi input yang tidak memadai.

## Competitive Intelligence/  Kecerdasan Kompetitif

Competitive intelligence (CI) adalah proses dan praktik berwawasan ke depan yang digunakan dalam menghasilkan pengetahuan tentang lingkungan kompetitif untuk meningkatkan kinerja organisasi.

Links:

- [https://en.wikipedia.org/wiki/Competitive_intelligence](https://en.wikipedia.org/wiki/Competitive_intelligence)

## Concatenation / Rangkaian

Dalam teori bahasa formal dan pemrograman komputer, rangkaian string adalah operasi menggabungkan string karakter end-to-end.
Misalnya, rangkaian "salju" dan "bola" adalah "bola salju".
Dalam formalisasi tertentu dari teori penggabungan, juga disebut teori string, rangkaian string adalah gagasan primitif.

Links:

- [https://en.wikipedia.org/wiki/Concatenation](https://en.wikipedia.org/wiki/Concatenation)

## Containerization / Kontainerisasi

Kontainerisasi adalah virtualisasi tingkat sistem operasi atau virtualisasi tingkat aplikasi melalui beberapa sumber daya jaringan sehingga aplikasi perangkat lunak dapat berjalan di ruang pengguna terisolasi yang disebut kontainer di lingkungan cloud atau non-cloud apa pun, apa pun jenis atau vendornya.

Links:

- [https://en.wikipedia.org/wiki/Containerization_(computing)](https://en.wikipedia.org/wiki/Containerization_(computing))

## Content Addressable Memory Table / Tabel Memori Beralamat Konten

Tabel Content Addressable Memory (CAM) adalah konstruksi memori sistem yang digunakan oleh logika switch Ethernet yang menyimpan informasi seperti alamat MAC yang tersedia pada port fisik dengan Parameter VLAN terkait.

Links:

- [https://en.wikipedia.org/wiki/MAC_address](https://en.wikipedia.org/wiki/MAC_address)

## Content Management System / Sistem Manajemen Konten

Sistem manajemen konten (CMS) adalah perangkat lunak komputer yang digunakan untuk mengelola pembuatan dan modifikasi konten digital (manajemen konten).
CMS biasanya digunakan untuk manajemen konten perusahaan (ECM) dan manajemen konten web (WCM).

Links:

- [https://en.wikipedia.org/wiki/Content_management_system](https://en.wikipedia.org/wiki/Content_management_system)

## Cookie/ Kue

Cookie HTTP (juga disebut cookie web, cookie Internet, cookie browser, atau hanya cookie) adalah blok kecil data yang dibuat oleh server web saat pengguna menjelajahi situs web dan ditempatkan di komputer pengguna atau perangkat lain oleh browser web pengguna.

Links:

- [https://en.wikipedia.org/wiki/HTTP_cookie](https://en.wikipedia.org/wiki/HTTP_cookie)

## Credential Stuffing/ ## Credential Stuffing

Credential stuffing adalah jenis serangan cyber di mana penyerang mengumpulkan kredensial akun yang dicuri, biasanya terdiri dari daftar nama pengguna dan / atau alamat email dan kata sandi yang sesuai (seringkali dari pelanggaran data), dan kemudian menggunakan kredensial untuk mendapatkan akses tidak sah ke akun pengguna di sistem lain melalui permintaan login otomatis berskala besar yang diarahkan terhadap aplikasi web.

Links:

- [https://en.wikipedia.org/wiki/Credential_stuffing](https://en.wikipedia.org/wiki/Credential_stuffing)

## Cross Origin Resource Sharing /Berbagi Sumber Daya Lintas Asal

Cross-origin resource sharing (CORS) adalah mekanisme yang memungkinkan sumber daya terbatas pada halaman web diminta dari domain lain di luar domain tempat sumber daya pertama dilayani.

Links:

- [https://en.wikipedia.org/wiki/Cross-origin_resource_sharing](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing)

## Cross Site Request Forgery / Pemalsuan Permintaan Lintas Situs

Pemalsuan permintaan lintas situs, juga dikenal sebagai serangan sekali klik atau sesi naik dan disingkat CSRF (kadang-kadang diucapkan sea-surf) atau XSRF, adalah jenis eksploitasi berbahaya dari situs web atau aplikasi web di mana perintah tidak sah dikirimkan dari pengguna yang dipercaya aplikasi web.

Links:

- [https://en.wikipedia.org/wiki/Cross-site_request_forgery](https://en.wikipedia.org/wiki/Cross-site_request_forgery)

## Cross Site Scripting / Skrip Lintas Situs

Cross-site scripting (XSS) adalah jenis kerentanan keamanan yang dapat ditemukan di beberapa aplikasi web.
Serangan XSS memungkinkan penyerang untuk menyuntikkan skrip sisi klien ke halaman web yang dilihat oleh pengguna lain.

Links:

- [https://en.wikipedia.org/wiki/Cross-site_scripting](https://en.wikipedia.org/wiki/Cross-site_scripting)

## Cryptanalysis / Kriptoanalisis

Cryptanalysis (dari bahasa Yunani kryptós, "tersembunyi", dan analýein, "menganalisis") mengacu pada proses menganalisis sistem informasi untuk memahami aspek tersembunyi dari sistem.
Cryptanalysis digunakan untuk melanggar sistem keamanan kriptografi dan mendapatkan akses ke isi pesan terenkripsi, bahkan jika kunci kriptografi tidak diketahui.

### Linear cryptanalysis / Kriptanalisis linier

Dalam kriptografi, kriptanalisis linier adalah bentuk umum kriptanalisis berdasarkan menemukan perkiraan affine terhadap aksi sandi.
Serangan telah dikembangkan untuk cipher blok dan cipher aliran.
Kriptanalisis linier adalah salah satu dari dua serangan yang paling banyak digunakan pada cipher blok; yang lainnya adalah kriptanalisis diferensial.

### Differential cryptanalysis / Kriptanalisis diferensial

Cryptanalysis diferensial adalah bentuk umum cryptanalysis yang berlaku terutama untuk memblokir cipher, tetapi juga untuk mengalirkan cipher dan fungsi hash kriptografi.
Dalam arti luas, ini adalah studi tentang bagaimana perbedaan input informasi dapat mempengaruhi perbedaan yang dihasilkan pada output.

### Integral cryptanalysis /  Kriptanalisis integral

Dalam kriptografi, kriptanalisis integral adalah serangan kriptanalitik yang secara khusus berlaku untuk memblokir cipher berdasarkan jaringan substitusi-permutasi.
Awalnya dirancang oleh Lars Knudsen sebagai serangan khusus terhadap Square, sehingga umumnya dikenal sebagai serangan Square.

Links:

- [https://en.wikipedia.org/wiki/Cryptanalysis](https://en.wikipedia.org/wiki/Cryptanalysis)
- [https://en.wikipedia.org/wiki/Linear_cryptanalysis](https://en.wikipedia.org/wiki/Linear_cryptanalysis)
- [https://en.wikipedia.org/wiki/Differential_cryptanalysis](https://en.wikipedia.org/wiki/Differential_cryptanalysis)
- [https://en.wikipedia.org/wiki/Integral_cryptanalysis](https://en.wikipedia.org/wiki/Integral_cryptanalysis)

## Cryptography / Kriptografi

Kriptografi, atau kriptologi (dari bahasa Yunani Kuno: κρυπτός, diromanisasi: kryptós "tersembunyi, rahasia"; dan γράφειν graphein, "menulis", atau -λογία -logia, "belajar", masing-masing), adalah praktik dan studi teknik untuk komunikasi yang aman di hadapan perilaku permusuhan.

### Elliptic-curve cryptography / Kriptografi kurva elips

Elliptic-curve cryptography (ECC) adalah pendekatan kriptografi kunci publik berdasarkan struktur aljabar kurva eliptik di atas bidang hingga.
ECC memungkinkan kunci yang lebih kecil dibandingkan dengan kriptografi non-EC (berdasarkan bidang Galois biasa) untuk memberikan keamanan yang setara.

### Quantum cryptography / Kriptografi kuantum

Kriptografi kuantum adalah ilmu mengeksploitasi sifat mekanika kuantum untuk melakukan tugas kriptografi.
Contoh kriptografi kuantum yang paling terkenal adalah distribusi kunci kuantum yang menawarkan solusi aman secara teoritis informasi untuk masalah pertukaran kunci.

Links:

- [https://en.wikipedia.org/wiki/Cryptography](https://en.wikipedia.org/wiki/Cryptography)

## Cyber Kill Chain / Rantai Pembunuhan Cyber

Dikembangkan oleh Lockheed Martin, kerangka kerja Cyber Kill Chain® adalah bagian dari model Intelligence Driven Defense® untuk identifikasi dan pencegahan aktivitas intrusi cyber.
Model ini mengidentifikasi apa yang harus diselesaikan musuh untuk mencapai tujuan mereka.
Rantai:
-Pengintaian:

- Memanen alamat email, informasi   konferensi, dll.

- Persenjataan:

- Eksploitasi kopling dengan backdoor ke dalam muatan yang dapat dikirim

-Pengiriman:

-Mengirimkan bundel senjata kepada korban melalui email, web, USB, dll.

-Eksploitasi:

- Mengeksploitasi kerentanan untuk  mengeksekusi kode pada sistem korban

-Instalasi:

- Menginstal malware pada aset

- Komando dan kontrol (C2):

- Saluran komando untuk manipulasi jarak jauh korban

- Tindakan pada tujuan:

- Penyusup mencapai tujuan mereka

Links:

- [https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)

## Cyber Threat Intelligence / Inteligensi Ancaman Cyber

Intelijen ancaman dunia maya (CTI) adalah pengetahuan, keterampilan, dan informasi berbasis pengalaman mengenai terjadinya dan penilaian ancaman dunia maya dan fisik serta aktor ancaman yang dimaksudkan untuk membantu mengurangi potensi serangan dan peristiwa berbahaya yang terjadi di dunia maya.

### Cyber threat intelligence - tactical / Intelijen ancaman dunia maya - taktis

Kecerdasan teknis (termasuk Indikator Kompromi seperti alamat IP, nama file, atau hash) yang dapat digunakan untuk membantu dalam identifikasi aktor ancaman.

### Cyber threat intelligence - operational / Inteligensi ancaman dunia maya - operasional

Operasional: rincian motivasi atau kemampuan aktor ancaman, termasuk alat, teknik, dan prosedur mereka.

### Cyber threat intelligence - strategic / Inteligensi ancaman dunia maya - strategis

Strategis: intelijen tentang risiko menyeluruh yang terkait dengan ancaman dunia maya yang dapat digunakan untuk mendorong strategi organisasi tingkat tinggi.

Links:

- [https://en.wikipedia.org/wiki/Cyber_threat_intelligence](https://en.wikipedia.org/wiki/Cyber_threat_intelligence)
