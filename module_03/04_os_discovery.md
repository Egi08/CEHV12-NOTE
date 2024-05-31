# Bagian 04: OS Discovery/Penemuan OS

**Lab3-Tugas2: OS Discovery/Penemuan OS**

- **nmap -A -v [IP]**
  - **-A:** Aggressive scan
- **nmap -O -v [IP]**
  - **-O:** OS discovery
- **nmap –script smb-os-discovery.nse [IP]**
  - **-–script:** Specify the customized script
  - **smb-os-discovery.nse:** Determine the OS, computer name, domain, workgroup, and current time over the SMB protocol (Port 445 or 139)
  ---------------------------------------
  atau anda mungkin bisa memahami jika versi indonesia:

- **nmap -A -v [IP]**
 - **-A:** Pemindaian agresif
- **npeta -O -v [IP]**
 - **-O:** Penemuan OS
- **nmap –skrip smb-os-discovery.nse [IP]**
 - **-–script:** Tentukan skrip yang disesuaikan
 - **smb-os-discovery.nse:** Tentukan OS, nama komputer, domain, grup kerja, dan waktu saat ini melalui protokol SMB (Port 445 atau 139)
 --------------------------------------------------- --------

## Banner Grabbing/Pengambilan Spanduk
Meraih Branner

[Definisi](../definitions/definitions_B.md#banner-grabbing)

## Identifying Target OS/Mengidentifikasi OS Sasaran

Wireshark/hiu kabel

[Definisi](../definitions/definitions_W.md#wireshark)

Penemuan menggunakan `nmap`

```shell
nmap -O 10.10.10.10
```

### nmap script engine/mesin skrip nmap
> Nmap Scripting Engine (NSE) adalah salah satu fitur Nmap yang paling kuat dan fleksibel.
> Memungkinkan pengguna untuk menulis (dan berbagi) skrip sederhana untuk mengotomatisasi berbagai tugas jaringan.
> Script tersebut kemudian dieksekusi secara paralel dengan kecepatan dan efisiensi yang Anda harapkan dari Nmap.
> Pengguna dapat mengandalkan rangkaian skrip yang berkembang dan beragam yang didistribusikan dengan Nmap, atau menulis skrip mereka sendiri untuk memenuhi kebutuhan khusus.

nmap IPv6

```shell
nmap -6 -O 10.10.10.10
```

- [https://nmap.org/book/nse.html](https://nmap.org/book/nse.html)
