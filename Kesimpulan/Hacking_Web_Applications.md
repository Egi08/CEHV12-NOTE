# Peretasan Aplikasi Web
> Peretasan aplikasi web merujuk pada mendapatkan akses tanpa izin ke sebuah situs web atau data yang terkait dengannya.

Ikhtisar Aplikasi Web:
- Aplikasi web menyediakan antarmuka antara pengguna akhir dan server web melalui serangkaian halaman web yang dihasilkan di ujung server atau yang mengandung kode skrip untuk dieksekusi secara dinamis di browser Web klien.
- Aplikasi web berjalan di browser web dan menggunakan sekelompok skrip sisi server (seperti ASP dan PHP) dan skrip sisi klien (seperti HTML dan JavaScript) untuk menjalankan aplikasi tersebut. Kerja dari aplikasi web tergantung pada arsitekturnya, yang mencakup perangkat keras dan perangkat lunak yang melakukan tugas seperti membaca permintaan, mencari, mengumpulkan, dan menampilkan data yang dibutuhkan.

Jejak infrastruktur web memungkinkan penyerang untuk melakukan tugas-tugas berikut:
- Penemuan Server: Penyerang mencoba menemukan server fisik yang menghosting sebuah aplikasi web menggunakan teknik seperti Whois Lookup, Interogasi DNS, dan Pemindaian Port.
- Penemuan Layanan: Penyerang menemukan layanan yang berjalan di server web untuk menentukan apakah mereka dapat menggunakan beberapa di antaranya sebagai jalur serangan untuk meretas sebuah aplikasi web.
- Identifikasi Server: Penyerang menggunakan banner-grabbing untuk mendapatkan banner server; ini membantu mengidentifikasi pembuat dan versi perangkat lunak server web.
- Penemuan Konten Tersembunyi: Jejak juga memungkinkan penyerang untuk mengekstrak konten dan fungsionalitas yang tidak langsung terhubung atau dapat dijangkau dari konten utama yang terlihat.

Lakukan Rekognisi Aplikasi Web menggunakan WhatWeb:
- WhatWeb mengidentifikasi situs web dan mengenali teknologi web, termasuk sistem manajemen konten (CMS), platform blogging, paket statistik dan analitik, perpustakaan JavaScript, server web, dan perangkat tersemat. Ini juga mengidentifikasi nomor versi, alamat email, ID akun, modul kerangka kerja web, kesalahan SQL, dan lainnya.

Lakukan Web Spidering menggunakan OWASP ZAP:
- OWASP Zed Attack Proxy (ZAP) adalah alat pengujian penetrasi terintegrasi untuk menemukan kerentanan dalam aplikasi web. Ini menawarkan pemindai otomatis serta sekelompok alat yang memungkinkan Anda menemukan kerentanan keamanan secara manual. ZAP menyediakan fungsionalitas untuk berbagai tingkat keterampilan - dari pengembang hingga tester baru dalam pengujian keamanan, hingga spesialis pengujian keamanan.

Deteksi Load Balancer menggunakan Berbagai Alat:
- Organisasi menggunakan load balancer untuk mendistribusikan beban server web ke beberapa server dan meningkatkan produktivitas dan keandalan aplikasi web. Umumnya, ada dua jenis load balancer, yaitu, load balancer DNS (Layer 4 load balancer) dan load balancer http (layer 7 load balancer). Anda dapat menggunakan berbagai alat seperti dig dan load balancing detector (lbd) untuk mendeteksi load balancer dari organisasi target beserta alamat IP asli mereka.

`gobuster dir -u [Situs Web Target] -w /home/penyerang/Desktop/common.txt`

`python3 dirsearch.py -u http://www.moviescope.com`

Identifikasi Kerentanan XSS dalam Aplikasi Web menggunakan PwnXSS:
- PwnXSS adalah pemindai XSS sumber terbuka yang digunakan untuk mendeteksi kerentanan scripting lintas situs (XSS) dalam situs web. Ini adalah alat multiprocessing dan dapat disesuaikan yang ditulis dalam bahasa Python.
- ` python3 pwnxss.py -u http://testphp.vulnweb.com `

Lakukan Serangan Pemalsuan Permintaan Lintas Situs (CSRF):
- CSRF, juga dikenal sebagai serangan satu klik, terjadi ketika seorang peretas menginstruksikan browser web pengguna untuk mengirim permintaan ke situs web yang rentan melalui halaman web berbahaya. Situs web keuangan umumnya mengandung kerentanan CSRF. Biasanya, penyerang luar tidak dapat mengakses intranet perusahaan, jadi CSRF adalah salah satu metode yang digunakan untuk memasuki jaringan ini. Ketidakmampuan aplikasi web untuk membedakan permintaan yang dibuat menggunakan kode berbahaya dari permintaan yang asli mengungkapkannya pada serangan CSRF. Serangan-serangan ini mengeksploitasi kerentanan halaman web yang memungkinkan penyerang memaksa browser pengguna yang tidak curiga untuk mengirim permintaan berbahaya yang tidak mereka maksudkan.

`wpscan --api-token [Token API] --url http://10.10.1.22:8080/CEH --plugins-detection aggressive --enumerate vp `

- --enumerate vp: menentukan enumerasi plugin yang rentan.
