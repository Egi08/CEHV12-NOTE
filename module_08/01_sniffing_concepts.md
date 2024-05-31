# Bagian 01: Sniffing Concepts/Mengendus Konsep

**Lab2-Task1: Password Sniffing using Wireshark/Mengendus Kata Sandi menggunakan Wireshark**


- **Attacker**
  - Wireshark
- **Target**
  - [www.moviescope.com](http://www.moviescope.com/)
  - Login
- **Attacker**
  - Stop capture
  - File-\&gt;Save as
  - Filter: **http.request.method==POST**
  - RDP log in Target
  - service
  - start Remote Packet Capture Protocol v.0 (experimental)
  - Log off Target
  - Wireshark-\&gt;Capture options-\&gt;Manage Interface-\&gt;Remote Interfaces
  - Add a remote host and its interface
  - Fill info
- **Target**
  - Log in
  - Browse website and log in
- **Attacker**
  - Get packets
---------------------------------------------------------------
atau perlu saya tulis dalam bahasa indonesia agar bisa di pahami:

- **Penyerang**
 - Wireshark
- **Target**
 - [www.moviescope.com](http://www.moviescope.com/)
 - Gabung
- **Penyerang**
 - Hentikan penangkapan
 - File-\&gt;Simpan sebagai
 - Filter: **http.request.method==POST**
 - RDP masuk Target
 - melayani
 - mulai Remote Packet Capture Protocol v.0 (eksperimental)
 - Keluar dari Target
 - Wireshark-\&gt;Opsi pengambilan-\&gt;Kelola Antarmuka-\&gt;Antarmuka Jarak Jauh
 - Tambahkan host jarak jauh dan antarmukanya
 - Isi informasi
- **Target**
 - Gabung
 - Jelajahi situs web dan masuk
- **Penyerang**
 - Dapatkan paket
--------------------------------------------------- -------------

## Sniffing Concepts/Konsep Mengendus
Open systems interconnection (OSI) model/Model interkoneksi sistem terbuka (OSI).

[Definisi](../definitions/definitions_O.md#open-systems-interconnection-model)

Media access control (MAC) address/Alamat kontrol akses media (MAC).

[Definisi](../definitions/definitions_M.md#media-access-control-address)

Network switch/Peralihan jaringan

[Definisi](../definitions/definitions_S.md#switch)

Network interface card/Kartu antarmuka jaringan

[Definisi](../definitions/definitions_N.md#network-interface-card)

Address resolution protocol (ARP) spoofing/Pemalsuan protokol resolusi alamat (ARP).

[Definisi](../definitions/definitions_A.md#address-resolusi-protokol-spoofing)

Media access control (MAC) flooding/Kontrol akses media (MAC) banjir

[Definisi](../definitions/definitions_M.md#media-access-control-address-flooding)

Network sniffing attack/Serangan mengendus jaringan

[Definisi](../definitions/definitions_N.md#network-sniffing-action)

Protocol analyzer/Penganalisis protokol

[Definisi](../definitions/definitions_P.md#protocol-analyzer)

Wiretapping/Penyadapan

[Definisi](../definitions/definitions_W.md#penyadapan)

Lawful interception/Intersepsi yang sah

[Definisi](../definitions/definitions_L.md#lawful-interception)
