# Bagian 02: Host Discovery/Penemuan Tuan Rumah

**Lab1-Tugas1: Host discovery/Penemuan host**

- **nmap -sn -PR [IP]**
  - **-sn:** Disable port scan
  - **-PR:** ARP ping scan
- **nmap -sn -PU [IP]**
  - **-PU:** UDP ping scan
- **nmap -sn -PE [IP or IP Range]**
  - **-PE:** ICMP ECHO ping scan
- **nmap -sn -PP [IP]**
  - **-PP:** ICMP timestamp ping scan
- **nmap -sn -PM [IP]**
  - **-PM:** ICMP address mask ping scan
- **nmap -sn -PS [IP]**
  - **-PS:** TCP SYN Ping scan
- **nmap -sn -PA [IP]**
  - **-PA:** TCP ACK Ping scan
- **nmap -sn -PO [IP]**
  - **-PO:** IP Protocol Ping scanP
---------------------------------------------
atau anda bisa memahami dengan versi indonesia:

- **nmap -sn -PR [IP]**
 - **-sn:** Nonaktifkan pemindaian port
 - **-PR:** Pemindaian ping ARP
- **nmap -sn -PU [IP]**
 - **-PU:** Pemindaian ping UDP
- **nmap -sn -PE [Rentang IP atau IP]**
 - **-PE:** Pemindaian ping ICMP ECHO
- **nmap -sn -PP [IP]**
 - **-PP:** Pemindaian ping stempel waktu ICMP
- **nmap -sn -PM [IP]**
 - **-PM:** Pemindaian ping topeng alamat ICMP
- **nmap -sn -PS [IP]**
 - **-PS:** Pemindaian TCP SYN Ping
- **nmap -sn -PA [IP]**
 - **-PA:** Pemindaian TCP ACK Ping
- **nmap -sn -PO [IP]**
 - **-PO:** Pemindaian Ping Protokol IP

## Address Resolution Protocol/Protokol Resolusi Alamat (ARP)

Protokol resolusi alamat (ARP)

[Definisi](../definitions/definitions_A.md#address-solving-protocol)
