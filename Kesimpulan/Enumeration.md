# Enumerasi
> Enumerasi adalah proses mengekstrak nama pengguna, nama mesin, sumber daya jaringan, bagian bersama, dan layanan dari suatu sistem atau jaringan.

<br>

Enumerasi NetBIOS:
> NetBIOS singkatan dari Network Basic Input Output System. Windows menggunakan NetBIOS untuk berbagi file dan printer. Nama NetBIOS adalah nama komputer unik yang diberikan kepada sistem Windows, terdiri dari string ASCII 16 karakter yang mengidentifikasi perangkat jaringan melalui TCP/IP. Lima belas karakter pertama digunakan untuk nama perangkat, dan karakter ke-16 disimpan untuk jenis layanan atau catatan nama.

- nbtstat -a [alamat IP mesin remote]
- Dalam perintah ini, -a menampilkan tabel nama NetBIOS dari komputer remote.
- nbtstat -c
- Dalam perintah ini, -c mencantumkan isi cache nama NetBIOS komputer remote.
- nmap -sV -v --script nbstat.nse [Alamat IP Target]
- -sV mendeteksi versi layanan, -v mengaktifkan output verbose (yaitu, mencakup semua host dan port dalam output), dan --script nbstat.nse melakukan enumerasi NetBIOS.
- nmap -sU -p 137 --script nbstat.nse

Ikhtisar Enumerasi SNMP:

> SNMP (Simple Network Management Protocol) adalah protokol lapisan aplikasi yang berjalan pada UDP (User Datagram Protocol) dan memelihara serta mengelola router, hub, dan switch pada jaringan IP. Agen SNMP berjalan pada perangkat jaringan pada jaringan Windows dan UNIX.

> Enumerasi SNMP menggunakan SNMP untuk membuat daftar akun pengguna dan perangkat pada komputer target. SNMP menggunakan dua jenis komponen perangkat lunak untuk komunikasi: agen SNMP dan stasiun manajemen SNMP. Agen SNMP terletak pada perangkat jaringan, dan stasiun manajemen SNMP berkomunikasi dengan agen.

SNMP menggunakan port 161:

- nmap -sU -p 161 [Alamat IP Target]
- snmp-check [Alamat IP Target]
- SnmpWalk:

> SnmpWalk adalah alat baris perintah yang memindai banyak simpul SNMP secara instan dan mengidentifikasi serangkaian variabel yang tersedia untuk mengakses jaringan target. Ini dikeluarkan ke node root sehingga informasi dari semua sub node seperti router dan switch dapat diambil.

- snmpwalk -v1 -c public [IP target]
- –v: menentukan nomor versi SNMP (1 atau 2c atau 3) dan –c: mengatur string komunitas.
- snmpwalk -v2c -c public [Alamat IP Target]
- –v: menentukan versi SNMP (di sini, dipilih 2c) dan –c: mengatur string komunitas.

- nmap -sU -p 161 --script=snmp-sysdescr [Alamat IP Target]
- -sU: menentukan pemindaian UDP, -p: menentukan port yang akan dipindai, dan -–script: adalah argumen yang digunakan untuk menjalankan skrip tertentu (di sini, snmp-sysdescr).
- nmap -sU -p 161 --script=snmp-processes [Alamat IP Target]
- nmap -sU -p 161 --script=snmp-win32-software [Alamat IP Target]
- nmap -sU -p 161 --script=snmp-interfaces [Alamat IP Target]

Enumerasi LDAP:

> LDAP (Lightweight Directory Access Protocol) adalah protokol Internet untuk mengakses layanan direktori terdistribusi melalui jaringan. LDAP menggunakan DNS (Domain Name System) untuk pencarian cepat dan resolusi cepat dari kueri. Klien memulai sesi LDAP dengan terhubung ke DSA (Directory System Agent), biasanya pada port TCP 389, dan mengirim permintaan operasi ke DSA, yang kemudian menanggapi. BER (Basic Encoding Rules) digunakan untuk mentransmisikan informasi antara klien dan server. Seseorang dapat secara anonim melakukan kueri layanan LDAP untuk informasi sensitif seperti nama pengguna, alamat, detail departemen, dan nama server.

- nmap -sU -p 389 [Alamat IP Target]
- nmap -p 389 --script ldap-brute --script-args ldap.base='"cn=users,dc=CEH,dc=com"' [Alamat IP Target]
- ldapsearch
- ldapsearch adalah antarmuka yang dapat diakses melalui shell ke panggilan pustaka ldap_search_ext(3). ldapsearch membuka koneksi ke server LDAP, mengikat koneksi, dan melakukan pencarian menggunakan parameter yang ditentukan. Filter harus sesuai dengan representasi string untuk filter pencarian seperti yang didefinisikan dalam RFC 4515. Jika tidak disediakan, filter default, (objectClass=*), digunakan.
- ldapsearch -h [Alamat IP Target] -x -s base namingcontexts
- -x: menentukan otentikasi sederhana, -h: menentukan host, dan -s: menentukan cakupan.
- ldapsearch -h [Alamat IP Target] -x -b “DC=CEH,DC=com”
- -x: menentukan otentikasi sederhana, -h: menentukan host, dan -b: menentukan DN dasar untuk pencarian.
- ldapsearch -x -h [Alamat IP Target] -b "DC=CEH,DC=com" "objectclass=*" 
- -x: menentukan otentikasi sederhana, -h: menentukan host, dan -b: menentukan DN dasar untuk pencarian.

Enumerasi NFS:
> NFS (Network File System) adalah jenis sistem file yang memungkinkan pengguna komputer untuk mengakses, melihat, menyimpan, dan memperbarui file melalui server remote. Data remote ini dapat diakses oleh komputer klien dengan cara yang sama seperti diakses pada sistem lokal.

- nmap -p 2049 [Alamat IP Target]
- https://github.com/p4pentest/SuperEnum
- https://github.com/hegusung/RPCScan

Enumerasi DNS:
> Teknik enumerasi DNS digunakan untuk mendapatkan informasi tentang server DNS dan infrastruktur jaringan organisasi target. Enumerasi DNS dapat dilakukan menggunakan teknik berikut:

- dig ns [Domain Target]
- Dalam perintah ini, ns mengembalikan server nama dalam hasil.
- dig @[NamaServer] [Domain Target]

axfr

- (dalam contoh ini, nama server adalah ns1.bluehost.com dan domain target adalah www.certifiedhacker.com); tekan Enter.

- Dalam perintah ini, axfr mengambil informasi zona.

DNSSEC Zone Walking:
> DNSSEC zone walking adalah teknik enumerasi DNS yang digunakan untuk mendapatkan rekaman internal dari server DNS target jika zona DNS tidak dikonfigurasi dengan benar. Informasi zona yang dienumerasi dapat membantu Anda membangun peta jaringan host.

- ./dnsrecon.py -d [Domain Target] -z
- Dalam perintah ini, -d menentukan domain target dan -z menentukan bahwa pencarian zona DNSSEC dilakukan dengan enumerasi standar.

- nmap --script=broadcast-dns-service-discovery [Domain Target]
- nmap -T4 -p 53 --script dns-brute [Domain Target]
- -T4: menentukan templat waktu, -p: menentukan port target.
- nmap --script dns-srv-enum --script-args "dns-srv-enum.domain='[Domain Target]'”

Enumerasi SMTP:
> Protokol Transfer Surat Sederhana (SMTP) adalah protokol komunikasi berbasis standar internet untuk transmisi surat elektronik. Sistem surat umumnya menggunakan SMTP dengan POP3 dan IMAP, yang memungkinkan pengguna menyimpan pesan di kotak surat server dan mengunduhnya dari server bila diperlukan. SMTP menggunakan server pertukaran surat (MX) untuk mengarahkan surat melalui DNS. Ini berjalan pada port TCP 25, 2525, atau 587.

- nmap -p 25 --script=smtp-enum-users [Alamat IP Target]
- nmap -p 25 --script=smtp-open-relay [Alamat IP Target]
- nmap -p 25 --script=smtp-commands [Alamat IP Target]

Enumerasi RPC: Mengekstrak endpoint RPC memungkinkan identifikasi layanan rentan pada port layanan ini

Enumerasi SMB: Mengekstrak layanan SMB memungkinkan pengambilan banner, yang mendapatkan informasi seperti detail OS dan versi layanan yang berjalan

Enumerasi FTP: Mengekstrak layanan FTP menghasilkan informasi tentang port 21 dan layanan FTP yang berjalan; informasi ini dapat digunakan untuk meluncurkan berbagai serangan seperti loncatan FTP, brute force FTP, dan penyadapan paket

Mengekstrak Informasi dari Host Windows dan Samba menggunakan Enum4linux:

- Enum4linux adalah alat untuk mengekstrak informasi dari sistem Windows dan Samba. Ini digunakan untuk enumerasi berbagi, pengambilan kebijakan sandi, identifikasi OS remote, mendeteksi apakah host berada di grup kerja atau domain, daftar pengguna di host, daftar informasi keanggotaan grup, dll.
- enum4linux -u martin -p apple -n [Alamat IP Target]
- enum4linux -u martin -p apple -U [Alamat IP Target]
  - Dalam perintah ini, -u pengguna menentukan nama pengguna yang akan digunakan, -p pass menentukan kata sandi, dan -U mengambil daftar pengguna.
  - -P mengambil informasi kebijakan sandi.
  - -o mengambil informasi OS.
  - -G mengambil daftar grup dan anggota.
  - -S mengambil daftar berbagi.
