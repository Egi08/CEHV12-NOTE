# Pemindaian Jaringan
> Pemindaian jaringan merujuk pada serangkaian prosedur yang dilakukan untuk mengidentifikasi host, port, dan layanan yang berjalan dalam suatu jaringan.

<br>

Penemuan Host menggunakan Nmap: `nmap -sn -PR [Alamat IP Target] `
- > -sn: menonaktifkan pemindaian port dan -PR: melakukan pemindaian ping ARP.
- > -PU: melakukan pemindaian ping UDP.
- > -PE: melakukan pemindaian ping ICMP ECHO.
- > -PP: melakukan pemindaian ping timestamp ICMP.
- Pemindaian Ping Masker Alamat ICMP: Teknik ini adalah alternatif untuk pemindaian ping ICMP ECHO tradisional, yang digunakan untuk menentukan apakah host target aktif khususnya ketika administrator memblokir ping ICMP ECHO.
  - nmap -sn -PM [alamat IP target]

- Pemindaian Ping TCP SYN: Teknik ini mengirimkan paket TCP SYN kosong ke host target, respons ACK berarti host aktif.
  - nmap -sn -PS [alamat IP target]

- Pemindaian Ping TCP ACK: Teknik ini mengirimkan paket TCP ACK kosong ke host target; respons RST berarti host aktif.

  - nmap -sn -PA [alamat IP target]
- Pemindaian Ping Protokol IP: Teknik ini mengirimkan paket probe yang berbeda dari protokol IP yang berbeda ke host target, respons apa pun dari setiap probe menunjukkan bahwa host aktif.
  - nmap -sn -PO [alamat IP target]

sx arp [Subnet Target] 
- sx arp [Subnet Target] --json | tee arp.cache
- cat arp.cache | sx tcp -p 1-65535 [Alamat IP target] 
- cat arp.cache | sx udp --json -p [Port Target] 10.10.1.11

nmap -sS -v [Alamat IP Target] 
- -sS: melakukan pemindaian stealth/TCP half-open scan dan -v: mengaktifkan output verbose (termasuk semua host dan port dalam output).
    > Pemindaian stealth melibatkan pengaturan ulang koneksi TCP antara klien dan server secara tiba-tiba sebelum penyelesaian sinyal tiga tangan, dan oleh karena itu meninggalkan koneksi setengah-terbuka. Teknik pemindaian ini dapat digunakan untuk menghindari aturan firewall, mekanisme logging, dan menyembunyikan di bawah lalu lintas jaringan.

nmap -sX -v [Alamat IP Target]
- -sX: melakukan pemindaian Xmas
    > Pemindaian Xmas mengirimkan sebuah frame TCP ke sistem target dengan pengaturan bendera FIN, URG, dan PUSH. Jika target telah membuka port, maka Anda tidak akan menerima respons dari sistem target. Jika target telah menutup port, maka Anda akan menerima balasan dari sistem target dengan RST.

- -sM: melakukan pemindaian TCP Maimon
    > Dalam pemindaian TCP Maimon, probe FIN/ACK dikirim ke target; jika tidak ada respons, maka port tersebut Open|Filtered, tetapi jika paket RST dikirim sebagai respons, maka port tersebut tertutup.

-  -sA: melakukan pemindaian probe flag ACK
    > Pemindaian probe flag ACK mengirimkan paket probe ACK dengan nomor urutan acak; tidak ada respons berarti bahwa port difilter (firewall berbasis status hadir), dan respons RST berarti bahwa port tidak difilter.

- -sU: melakukan pemindaian UDP
    > Pemindaian UDP menggunakan protokol UDP alih-alih TCP. Tidak ada tiga tahap perjanjian untuk pemindaian UDP. Ini mengirimkan paket UDP ke host target; tidak ada respons berarti bahwa port terbuka. Jika port ditutup, pesan ICMP port unreachable diterima.

- -sV: mendeteksi versi layanan.
- -A: mengaktifkan pemindaian agresif. Opsi pemindaian agresif mendukung deteksi OS (-O), pemindaian versi (-sV), pemindaian skrip (-sC), dan traceroute (--traceroute). Anda tidak boleh menggunakan -A terhadap jaringan target tanpa izin.

Banner grabbing, atau fingerprint OS, adalah metode yang digunakan untuk menentukan OS yang berjalan pada sistem target remote.

Ada dua jenis teknik penemuan OS atau banner grabbing:

- Active Banner Grabbing Paket yang dirancang khusus dikirim ke OS remote, dan respons dicatat, yang kemudian dibandingkan dengan database untuk menentukan OS. Respons dari OS yang berbeda bervariasi, karena perbedaan dalam implementasi stack TCP/IP.

- Passive Banner Grabbing Ini bergantung pada implementasi differential dari stack dan berbagai cara OS merespons paket. Passive banner grabbing termasuk banner grabbing dari pesan error, mengintip lalu lintas jaringan, dan banner grabbing dari ekstensi halaman.

Identifikasi OS sistem target dengan Time-to-Live (TTL):

![image](https://user-images.githubusercontent.com/79740895/226240083-d6fba9dd-4e9d-4490-8a0a-c9dd2c3e320c.png)

nmap --script smb-os-discovery.nse [Alamat IP Target]
> --script: menentukan skrip yang disesuaikan dan smb-os-discovery.nse: mencoba menentukan OS, nama komputer, domain, workgroup, dan waktu saat ini melalui protokol SMB (port 445 atau 139).

unicornscan [Alamat IP Target] -Iv
> Dalam perintah ini, -I menentukan mode langsung dan v menentukan mode verbose.

## Pemindaian di luar IDS dan Firewall

Sistem Deteksi Intrusi (IDS) dan firewall adalah mekanisme keamanan yang dimaksudkan untuk mencegah orang yang tidak sah mengakses jaringan. Namun, bahkan IDS dan firewall memiliki beberapa keterbatasan keamanan. Firewall dan IDS bermaksud untuk menghindari lalu lintas (pakets) jahat dari masuk ke dalam jaringan, tetapi beberapa teknik dapat digunakan untuk mengirimkan paket yang dimaksudkan ke target dan menghindari IDS/firewall.

Teknik untuk menghindari IDS/firewall:

- Fragmentasi Paket: Mengirimkan paket probe yang difragmentasikan ke target yang dimaksud, yang kemudian merakitnya setelah menerima semua fragmen
- Source Routing: Menentukan jalur routing untuk paket yang cacat agar mencapai target yang dimaksud
- Manipulasi Port

 Sumber: Memanipulasi port sumber aktual dengan port sumber umum untuk menghindari IDS/firewall
- Decoy Alamat IP: Menghasilkan atau menentukan manual alamat IP dari decoys sehingga IDS/firewall tidak dapat menentukan alamat IP aktual
- Pemalsuan Alamat IP: Mengubah alamat IP sumber sehingga serangan terlihat berasal dari orang lain
- Membuat Paket Kustom: Mengirimkan paket kustom untuk memindai target yang dimaksud di luar firewall
- Pengacakan Urutan Host: Memindai jumlah host di jaringan target dalam urutan acak untuk memindai target yang dimaksud yang terletak di luar firewall
- Mengirimkan Checksum Buruk: Mengirimkan paket dengan checksum TCP/UPD buruk atau palsu ke target yang dimaksud
- Server Proksi: Menggunakan rangkaian server proksi untuk menyembunyikan sumber sebenarnya dari pemindaian dan menghindari pembatasan tertentu IDS/firewall
- Anonimizer: Menggunakan anonimizer yang memungkinkan mereka untuk melewati sensor Internet dan menghindari aturan tertentu IDS dan firewall

nmap -f [Alamat IP Target]
- -f digunakan untuk membagi paket IP menjadi paket fragmen kecil.
    > Fragmentasi paket merujuk pada pembagian paket probe menjadi beberapa paket kecil (fragmen) saat mengirimkannya ke jaringan. Ketika paket-paket ini mencapai host, IDS dan firewall di belakang host umumnya mengantri semuanya dan memprosesnya satu per satu. Namun, karena metode pemrosesan ini melibatkan konsumsi CPU yang lebih besar serta sumber daya jaringan, konfigurasi sebagian besar IDS membuatnya melewati paket-paket yang difragmentasikan selama pemindaian port.

nmap -g 80 [Alamat IP Target]
- Dalam perintah ini, Anda dapat menggunakan opsi -g atau --source-port untuk melakukan manipulasi port sumber.
    > Manipulasi port sumber merujuk pada memanipulasi nomor port aktual dengan nomor port umum untuk menghindari IDS/firewall: ini berguna ketika firewall dikonfigurasi untuk mengizinkan paket dari port yang dikenal seperti HTTP, DNS, FTP, dll.

nmap -mtu 8 [Alamat IP Target]
- Dalam perintah ini, -mtu: menentukan jumlah Maximum Transmission Unit (MTU) (di sini, 8 byte paket).
    > Dengan menggunakan MTU, paket-paket kecil dikirimkan daripada mengirimkan satu paket lengkap sekaligus. Teknik ini menghindari mekanisme penyaringan dan deteksi yang diaktifkan di mesin target.

nmap -D RND:10 [Alamat IP Target]
- Dalam perintah ini, -D: melakukan pemindaian decoy dan RND: menghasilkan alamat IP acak dan non-reserved (di sini, 10).
    > Teknik decoy alamat IP merujuk pada menghasilkan atau menentukan manual alamat IP dari decoys untuk menghindari IDS/firewall. Teknik ini membuat sulit bagi IDS/firewall untuk menentukan IP address mana yang sebenarnya melakukan pemindaian jaringan dan IP addresses mana yang adalah decoys. Dengan menggunakan perintah ini, Nmap secara otomatis menghasilkan sejumlah decoy untuk pemindaian dan secara acak menempatkan alamat IP asli di antara alamat IP decoy.

nmap -sT -Pn --spoof-mac 0 [Alamat IP Target]
- Dalam perintah ini --spoof-mac 0 mewakili randomisasi alamat MAC, -sT: melakukan pemindaian TCP connect/full open, -Pn digunakan untuk melewati penemuan host.
    > Teknik pemalsuan alamat MAC melibatkan pemalsuan alamat MAC dengan alamat MAC pengguna yang sah di jaringan. Teknik ini memungkinkan Anda untuk mengirimkan paket permintaan ke mesin/jaringan target yang berpura-pura menjadi host yang sah.

Membuat Paket UDP dan TCP Kustom menggunakan Hping3 untuk Pemindaian di luar IDS/Firewall
> Hping3 adalah program yang dapat di-skrip yang menggunakan bahasa TCL, di mana paket dapat diterima dan dikirim melalui representasi biner atau string yang menggambarkan paket.

hping3 [Alamat IP Target] --udp --rand-source --data 500
- Di sini, --udp menentukan mengirimkan paket UDP ke host target, --rand-source mengaktifkan mode sumber acak dan --data menentukan ukuran badan paket.

hping3 -S [Alamat IP Target] -p 80 -c 5
- Di sini, -S menentukan permintaan TCP SYN pada mesin target, -p menentukan penugasan port untuk mengirimkan lalu lintas, dan -c adalah jumlah paket yang dikirim ke mesin target.

hping3 [Alamat IP Target] --flood
- --flood: melakukan banjirkan TCP.

Pindai Jaringan Target menggunakan Metasploit:
> Kerangka Metasploit adalah alat yang menyediakan informasi tentang kerentanan keamanan dalam sistem organisasi target, dan membantu dalam pengujian penetrasi dan pengembangan tanda tangan IDS. Ini memfasilitasi tugas-tugas penyerang, penulis eksploitasi, dan penulis muatan. Keuntungan utama dari kerangka tersebut adalah pendekatan modular, yaitu memungkinkan kombinasi eksploitasi apa pun dengan muatan apa pun.

```
layanan postgresql mulai
msfdb init
msfconsole 

db_status 

nmap -Pn -sS -A -oX Test 10.10.1.0/24

db_import Test

hosts 

db_services 

use auxiliary/scanner/portscan/syn

set INTERFACE eth0
set PORTS 80
set RHOSTS 10.10.1.5-23
set THREADS 50

run


use auxiliary/scanner/portscan/tcp

set RHOSTS [Alamat IP Target]

run


use auxiliary/scanner/smb/smb_version

set RHOSTS 10.10.1.5-23

set THREADS 11

```

