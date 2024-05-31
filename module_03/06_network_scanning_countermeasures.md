# Bagian 06: Network Scanning Countermeasures/Penanggulangan Pemindaian Jaringan

## Ping Sweeping Countermeasures/Penanggulangan Penyapuan Ping

- Jangan izinkan koneksi mengirim lebih dari sejumlah kecil permintaan ICMP ECHO.
- Gunakan IDS dan IPS untuk mendeteksi sapuan ping
- Batasi lalu lintas ICMP dengan daftar kontrol akses (ACL)

## Port Sweeping Countermeasures/Penanggulangan Penyapuan Pelabuhan

- Gunakan IDS dan IPS untuk mendeteksi sapuan ping
- Pastikan semua router, firewall, dll menjalankan perangkat lunak versi terbaru.
- Blokir port yang tidak diinginkan.

## Banner Grabbing countermeasures/Penanggulangan Perampasan Spanduk

- Menampilkan spanduk palsu untuk menyesatkan penyerang.
- Mengaktifkan layanan yang tidak perlu pada host untuk membatasi pengungkapan informasi.
- Nonaktifkan detail vendor dan versi di spanduk.

## IP Spoofing Countermeasures/Penanggulangan Spoofing IP

Internet protocol security (IPSec)/Keamanan protokol Internet (IPSec)

[Definisi](../definitions/definitions_I.md#internet-protocol-security)

- Hindari otentikasi berdasarkan alamat IP
- Gunakan firewall dan ACL
- Gunakan enkripsi. IPSec dapat sangat mengurangi risiko spoofing IP.


## Scanning Detection Tools/Alat Deteksi Pemindaian

Splunk

[Definisi](../definitions/definitions_S.md#splunk)
