# Bagian 05: Scanning Beyond IDS and Firewall/Memindai Melampaui IDS dan Firewall

## Evasion Techniques (Routing)/Teknik Penghindaran (Routing)

Intrusion detection system (IDS)/Sistem deteksi intrusi (IDS)

[Definisi](../definitions/definitions_I.md#intrusion-detection-system)

Teknik untuk menghindari IDS/firewall adalah

- Proxy servers/Server proksi
- IP address spoofing/pemalsuan alamat IP
- Mac address spoofing/Pemalsuan alamat Mac
- Packet fragmentation/Fragmentasi paket

Packet fragmentation/Fragmentasi paket

[Definisi](../definitions/definitions_P.md#packet-fragmentation)

Source routing/Perutean sumber

[Definisi](../definitions/definitions_S.md#source-routing)

## Evasion Techniques (Spoofing)/Teknik Penghindaran (Spoofing)

Internet protocol (IP) address spoofing/spoofing alamat protokol internet (IP).

[Definisi](../definitions/definitions_I.md#internet-protocol-address-spoofing)

Media access control (MAC) address spoofing/Pemalsuan alamat kontrol akses media (MAC).

[Definisi](../definitions/definitions_M.md#media-access-control-address-spoofing)

## Evasion Techniques (Other)/Teknik Penghindaran (Lainnya)

Mengacak urutan host. Halaman manual opsi `nmap` option`--randomize-hosts` adalah

```shell
--randomize-hosts (Randomize target host order)

 Memberitahu Nmap untuk mengacak setiap grup hingga 16384 host sebelum memindainya. Hal ini dapat membuat pemindaian menjadi kurang jelas bagi berbagai sistem pemantauan jaringan, terutama saat
 Anda menggabungkannya dengan opsi waktu lambat. Jika Anda ingin mengacak ukuran grup yang lebih besar, tambah PING_GROUP_SZ di nmap.h dan kompilasi ulang. Solusi alternatifnya adalah dengan
 buat daftar IP target dengan pemindaian daftar (-sL -n -oN nama file), acak dengan skrip Perl, lalu berikan seluruh daftar ke Nmap dengan -iL.
```

Server proxy

[Definisi](../definitions/definitions_P.md#proxy-server)
