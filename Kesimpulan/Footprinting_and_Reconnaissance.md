Tentu, saya bisa membantu Anda. Berikut adalah versi dalam bahasa Indonesia dari teks yang Anda berikan:

# Pemetaan Jejak dan Rekognisi

> Pemetaan jejak merujuk pada pengumpulan sebanyak mungkin informasi tentang jaringan target dari sumber-sumber yang dapat diakses secara publik.

## Melakukan Pemetaan Jejak Melalui Mesin Pencari

https://mattw.io/youtube-metadata/
> Alat Metadata YouTube mengumpulkan detail-detail tertentu tentang sebuah video, pengunggahnya, daftar putar, serta pembuat atau saluran video tersebut.

[Pencarian Gambar Terbalik TinEye](https://tineye.com)

Mesin Pencari FTP:
- https://www.searchftps.net/
- https://www.freewareweb.com/

Mesin Pencari IoT:
- https://www.shodan.io/
- https://search.censys.io/

Domain dan Sub-domain:
- https://www.netcraft.com/tools/
- https://github.com/aboul3la/Sublist3r

theHarvester:
> Alat ini mengumpulkan surel, subdomain, host, nama karyawan, port terbuka, dan banner dari berbagai sumber publik seperti mesin pencari, server kunci PGP, dan database komputer SHODAN serta menggunakan Google, Bing, SHODAN, dll.
```
theHarvester -d eccouncil -l 200 -b linkedin
```
> -d menentukan domain atau nama perusahaan yang akan dicari (di sini, eccouncil), -l menentukan jumlah hasil yang akan diambil, dan -b menentukan sumber data sebagai LinkedIn.

Pencarian Deep Web dan Dark Web:
- [The Hidden Wiki](http://zqktlwiuavvvqqt4ybvgvi7tyo4hjl5xgfuvpdf6otjiycgwqbym2qad.onion/wiki)
- [FakeID](http://ymvhtqya23wqpez63gyc3ke4svju3mqsby2awnhd3bk2e65izt7baqad.onion) adalah situs onion untuk membuat paspor palsu
- [Cardshop](http://s57divisqlcjtsyutxjz2ww77vlbwpxgodtijcsrgsuts4js5hnxkhqd.onion) adalah situs onion yang menjual kartu dengan saldo yang baik
- [ExoneraTor](https://metrics.torproject.org)
- [Mesin Pencari OnionLand](https://onionlandsearchengine.com)

Informasi dari Berbagai Situs Jaringan Sosial:
- [Sherlock](https://github.com/sherlock-project/sherlock):
    > Sherlock adalah alat berbasis python yang digunakan untuk mengumpulkan informasi tentang seseorang target di berbagai situs jaringan sosial. Sherlock mencari sejumlah besar situs jaringan sosial untuk pengguna target yang diberikan, menemukan orang tersebut, dan menampilkan hasil bersama dengan URL lengkap terkait dengan orang target tersebut.
- [Social Searcher](https://www.social-searcher.com/)
- [Followerwonk](https://followerwonk.com/analyze)
    > Followerwonk adalah alat online yang membantu Anda menjelajahi dan mengembangkan graf sosial Anda, menggali lebih dalam ke dalam analitik Twitter; misalnya, Siapa pengikut Anda? Di mana mereka berada? Kapan mereka tweet? Ini dapat digunakan untuk mengumpulkan informasi Twitter tentang organisasi atau individu target apa pun.

Mengumpulkan Informasi tentang Sebuah Situs Web Target:
- [Photon](https://github.com/s0md3v/Photon)
   > Photon adalah skrip Python yang digunakan untuk merayapi URL target yang diberikan untuk mendapatkan informasi seperti URL (dalam dan luar jangkauan), URL dengan parameter, alamat surel, akun media sosial, file, kunci rahasia, dan subdomain. Informasi yang diekstraksi dapat diekspor lebih lanjut dalam format JSON.

- [Central Ops](https://centralops.net/co/)
    > CentralOps (centralops.net) adalah pemindai jaringan online gratis yang menyelidiki domain dan alamat IP, catatan DNS, traceroute, pencarian nslookup, whois, dll.

- https://github.com/digininja/CeWL
- https://whois.domaintools.com/

Pemetaan DNS
- nslookup
- http://www.kloth.net/services/nslookup.php
- https://dnsdumpster.com/
- https://www.broadbandsearch.net/network-tools
- https://www.yougetsignal.com/
- https://securitytrails.com/

Menemukan Rentang Jaringan

- tracert <-- windows
- traceroute <-- linux

Recon-ng:
> Recon-ng adalah kerangka kerja rekognisi web dengan modul-modul independen dan interaksi database yang menyediakan lingkungan di mana rekognisi berbasis web sumber terbuka dapat dilakukan. Di sini, kita akan menggunakan Recon-ng untuk melakukan rekognisi jaringan, mengumpulkan informasi personil, dan mengumpulkan informasi target dari situs jaringan sosial.

Maltego:
> Maltego adalah alat pemetaan jejak yang digunakan untuk mengumpulkan informasi maksimum untuk tujuan peretasan etis, forensik komputer, dan pentesting. Ini menyediakan perpustakaan transformasi untuk menemukan data dari sumber terbuka dan memvisualisasikan informasi tersebut dalam format grafik, cocok untuk analisis tautan dan penambangan data. Maltego memberi Anda antarmuka grafis yang membuat melihat hubungan-hubungan ini instan dan akurat, dan bahkan membuatnya mungkin untuk melihat koneksi-koneksi tersembunyi.

OSRFramework:
> OSRFramework adalah serangkaian perpustakaan yang digunakan untuk melakukan tugas Intelijen Sumber Terbuka. Mereka mencakup referensi ke banyak aplikasi yang berhubungan dengan pemeriksaan nama pengguna, pencarian DNS, penelitian kebocoran informasi, pencarian web dalam-dalam, ekstraksi ekspresi reguler, dan banyak lagi. Ini juga menyediakan cara membuat kueri-kueri ini secara grafis serta beberapa antarmuka untuk berinteraksi dengan seperti OSRFConsole atau antarmuka Web.

domainfy:
- `domainfy -n [Nama Domain] -t semua`
- > -n: menentukan nama panggilan atau daftar nama panggilan yang akan diperiksa. -t: menentukan daftar domain tingkat atas di mana nama panggilan akan dicari.

searchfy:
> periksa keberadaan detail pengguna yang diberikan pada platform jaringan sosial

 Situs Web Target:
- [Photon](https://github.com/s0md3v/Photon)
   > Photon adalah skrip Python yang digunakan untuk merambat URL target yang diberikan untuk memperoleh informasi seperti URL (dalam cakupan dan di luar cakupan), URL dengan parameter, alamat surel, akun media sosial, file, kunci rahasia, dan subdomain. Informasi yang diekstrak tersebut dapat diekspor lebih lanjut dalam format JSON.

- [Central Ops](https://centralops.net/co/)
    > CentralOps (centralops.net) adalah pemindai jaringan online gratis yang menyelidiki domain dan alamat IP, catatan DNS, traceroute, pencarian nslookup, whois, dll.

- https://github.com/digininja/CeWL
- https://whois.domaintools.com/

Pemetaan DNS
- nslookup 
- http://www.kloth.net/services/nslookup.php
- https://dnsdumpster.com/
- https://www.broadbandsearch.net/network-tools
- https://www.yougetsignal.com/
- https://securitytrails.com/

Menemukan Rentang Jaringan

- tracert   <-- Windows 
- traceroute    <-- Linux

Recon-ng:
> Recon-ng adalah kerangka kerja rekognisi web dengan modul-modul independen dan interaksi basis data yang menyediakan lingkungan di mana rekognisi berbasis web sumber terbuka dapat dilakukan. Di sini, kami akan menggunakan Recon-ng untuk melakukan rekognisi jaringan, mengumpulkan informasi personal, dan mengumpulkan informasi target dari situs jaringan sosial.

Maltego:
> Maltego adalah alat pemetaan jejak yang digunakan untuk mengumpulkan informasi maksimum untuk tujuan peretasan etis, forensik komputer, dan pentesting. Ini menyediakan perpustakaan transformasi untuk menemukan data dari sumber terbuka dan memvisualisasikan informasi tersebut dalam format grafik, cocok untuk analisis tautan dan penambangan data. Maltego menyediakan antarmuka grafis yang membuat melihat hubungan ini instan dan akurat, dan bahkan memungkinkan untuk melihat hubungan tersembunyi.

OSRFramework:
> OSRFramework adalah seperangkat perpustakaan yang digunakan untuk melakukan tugas Intelijen Sumber Terbuka. Mereka mencakup referensi ke banyak aplikasi yang berhubungan dengan pemeriksaan nama pengguna, pencarian DNS, penelitian kebocoran informasi, pencarian deep web, ekstraksi ekspresi reguler, dan banyak lainnya. Ini juga menyediakan cara untuk melakukan kueri-kueri ini secara grafis serta beberapa antarmuka untuk berinteraksi seperti OSRFConsole atau antarmuka Web.

domainfy :

- `domainfy -n [Nama Domain] -t semua `

- > -n: menentukan nama panggilan atau daftar nama panggilan yang akan diperiksa. -t: menentukan daftar domain tingkat atas di mana nama panggilan akan dicari.

searchfy:
> Periksa keberadaan rincian pengguna yang diberikan di berbagai platform jaringan sosial seperti Github, Instagram dan Keyserverubuntu. Ketik searchfy -q "nama pengguna atau profil target"

BillCipher:
> BillCipher adalah alat pengumpulan informasi untuk sebuah Situs Web atau alamat IP. Dengan menggunakan alat ini, Anda dapat mengumpulkan informasi seperti DNS Lookup, Whois lookup, GeoIP Lookup, Subnet Lookup, Port Scanner, Page Links, Zone Transfer, HTTP Header, dll. Di sini, kami akan menggunakan alat BillCipher untuk memetakan jejak URL situs web target.

### Kerangka Kerja OSINT

- https://osintframework.com/
