# Bagian 06: SMTP and DNS enumeration/Pencacahan SMTP dan DNS

## SMTP

Simple mail transfer protocol (SMTP)/Protokol transfer surat sederhana (SMTP)

[Definisi](../definitions/definitions_S.md#simple-mail-transfer-protocol)

Post office protocol (POP)/Protokol kantor pos (POP)

[Definisi](../definitions/definitions_P.md#post-office-protocol)

nmap

[Definisi](../definitions/definitions_N.md#nmap)

`smtp-enum-users` (nmap)/`smtp-enum-pengguna` (nmap)

Mencoba menghitung pengguna di server SMTP dengan mengeluarkan perintah VRFY, EXPN, atau RCPT TO.
Tujuan dari skrip ini adalah untuk menemukan semua akun pengguna di sistem jarak jauh.

Dig/Menggali

[Definisi](../definitions/definitions_D.md#dig)

Nslookup/Pencarian

[Definisi](../definitions/definitions_N.md#nslookup)

DNS security extensions (DNSSEC)/Ekstensi keamanan DNS (DNSSEC)

[Definisi](../definitions/definitions_D.md#nama-domain-sistem-keamanan-ekstensi)

`broadcast-dns-service-discovery` (nmap)/`penyiaran-dns-layanan-penemuan` (nmap)

Upaya menemukan layanan host menggunakan protokol Penemuan Layanan DNS.
Ia mengirimkan kueri DNS-SD multicast dan mengumpulkan semua respons.

Tautan

- [https://nmap.org/nsedoc/scripts/smtp-enum-users.html](https://nmap.org/nsedoc/scripts/smtp-enum-users.html)
- [https://nmap.org/nsedoc/scripts/broadcast-dns-service-discovery.html](https://nmap.org/nsedoc/scripts/broadcast-dns-service-discovery.html)