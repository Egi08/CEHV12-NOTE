# Bagian 03: Port and Service Discovery/Penemuan Pelabuhan dan Layanan

 **Lab2-Tugas3: Penemuan Pelabuhan dan Layanan**

- **nmap -sT -v [IP]**
  - **-sT:** TCP connect/full open scan
  - **-v:** Verbose output
- **nmap -sS -v [IP]**
  - **-sS:** Stealth scan/TCP hall-open scan
- **nmap -sX -v [IP]**
  - **-sX:** Xmax scan
- **nmap -sM -v [IP]**
  - **-sM:** TCP Maimon scan
- **nmap -sA -v [IP]**
  - **-sA:** ACK flag probe scan
- **nmap -sU -v [IP]**
  - **-sU:** UDP scan
- **nmap -sI -v [IP]**
  - **-sI:** IDLE/IPID Header scan
- **nmap -sY -v [IP]**
  - **-sY:** SCTP INIT Scan
- **nmap -sZ -v [IP]**
  - **-sZ:** SCTP COOKIE ECHO Scan
- **nmap -sV -v [IP]**
  - **-sV:** Detect service versions
- **nmap -A -v [IP]**
  - **-A:** Aggressive scan
-------------------------------------------
atau anda bisa memahaminya daengan bahasa indonesia:

- **nmap -sT -v [IP]**
 - **-sT:** Koneksi TCP/pemindaian terbuka penuh
 - **-v:** Keluaran verbose
- **nmap -sS -v [IP]**
 - **-sS:** Pemindaian tersembunyi/pemindaian terbuka di aula TCP
- **nmap -sX -v [IP]**
 - **-sX:** Pemindaian Xmax
- **nmap -sM -v [IP]**
 - **-sM:** Pemindaian TCP Maimon
- **nmap -sA -v [IP]**
 - **-sA:** Pemindaian pemeriksaan tanda ACK
- **nmap -sU -v [IP]**
 - **-sU:** Pemindaian UDP
- **nmap -sI -v [IP]**
 - **-sI:** Pemindaian Header IDLE/IPID
- **nmap -sY -v [IP]**
 - **-sY:** Pemindaian SCTP INIT
- **nmap -sZ -v [IP]**
 - **-sZ:** Pemindaian ECHO COOKIE SCTP
- **nmap -sV -v [IP]**
 - **-sV:** Mendeteksi versi layanan
- **nmap -A -v [IP]**
 - **-A:** Pemindaian agresif
-----------------------------------------------

## TCP Scanning/Pemindaian TCP

Pemindaian secara kasar dapat dibagi menjadi:

- Open TCP scanning/Buka pemindaian TCP
- Stealth TCP scanning/Pemindaian TCP tersembunyi
- UDP scanning/Pemindaian UDP
- SCTP scanning/Pemindaian SCTP
- IPv6 scanning/Pemindaian IPv6

## UDP Scan/Pemindaian UDP

Pemindaian UDP dilakukan menggunakan `nmap` dengan menjalankan

```shell
nmap -sU 10.10.10.10
```


## Service Version Discovery/Penemuan Versi Layanan

Sebuah port diberi layanan untuk dijalankan, dan setiap layanan memiliki versi tertentu.

Deteksi versi menggunakan `nmap`

```shell
nmap -sV
```

## nmap Reduction Techniques/Teknik Reduksi nmap

### Metode 1

Di bawah ini kami mencantumkan beberapa teknik untuk mengurangi scanning time/waktu pemindaian `nmap`.

- Batasi jumlah port (e.g. default 1000)
- Pemindaian port (`-sn`) dapat dilewati jika hanya keaktifan host yang perlu diperiksa.
- Hindari jenis pemindaian lanjutan (`--traceroute`)

### Metode 2

Mengoptimalkan parameter waktu. Pertimbangkan opsi `-T` untuk `nmap`

```shell
  -T<0-5>: Set timing template (higher is faster)
```

### Metode 3

Pisahkan pemindaian TCP dan UDP ke dalam pemindaian yang berbeda.
