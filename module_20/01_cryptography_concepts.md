# Bagian 01: Cryptography Concepts/Konsep Kriptografi

**Modul 20: Cryptography*/Kriptografi**

**Lab1-Tugas2: Calculate MD5 Hashes using MD5 Calculator*/Menghitung Hash MD5 menggunakan Kalkulator MD5**

- Tidak ada yang spesial

**Lab4-Task1: Perform Disk Encryption using VeraCrypt*/Melakukan Enkripsi Disk menggunakan VeraCrypt**

- Click VeraCrypt
- Create Volumn
- Create an encrypted file container
- Specify a path and file name
- Set password
- Select NAT
- Move the mouse randomly for some seconds, and click Format
- Exit
- Select a drive, select file, open, mount
- Input password
- Dismount
- Exit

------------------------------------

- Klik VeraCrypt
- Buat Volume
- Buat wadah file terenkripsi
- Tentukan jalur dan nama file
- Tetapkan kata sandi
- Pilih NAT
- Gerakkan mouse secara acak selama beberapa detik, lalu klik Format
- KELUAR
- Pilih drive, pilih file, buka, mount
- Masukkan kata sandi
- Turun
- KELUAR

**Lampiran Modul: Covered Tools*/Alat Tercakup**


- **Nmap**
  - Multiple Labs
- **Hydra**
  - Module 13: Lab2-Task1
- **Sqlmap**
  - Module 15: Lab1-Task2
- **WPScan**
  - Module 14: Lab2-Task5
  - wpscan –-url http://10.10.10.10 -t 50 -U admin -P rockyou.txt
- **Nikto**
  - [https://zhuanlan.zhihu.com/p/124246499](https://zhuanlan.zhihu.com/p/124246499%20)
- **John**
  - Module 06: Lab1-Task1
- **Hashcat**
  - **Crack MD5 passwords with a wordlist:**
  - hashcat hash.txt -m 0 -a 0 hash.txt /usr/share/wordlists/rockyou.txt
  - **Crack MD5 passwords in a certain format:**
  - hashcat -m 0 -a 3 ./hash.txt &#39;SKY-HQNT-?d?d?d?d&#39;
  - [https://xz.aliyun.com/t/4008](https://xz.aliyun.com/t/4008)
  - [https://tools.kali.org/password-attacks/hashcat](https://tools.kali.org/password-attacks/hashcat)
- **Metasploit**
  - Module 14: Lab2-Task5
- **Responder LLMNR**
  - Module 06: Lab1-Task1
- **Wireshark or Tcpdump**
  - Multiple Labs
- **Steghide**
  - **Hide**
  - steghide embed -cf [img file] -ef [file to be hide]
  - steghide embed -cf 1.jpg -ef 1.txt
  - Enter password or skip
  - **Extract**
  - steghide info 1.jpg
  - steghide extract -sf 1.jpg
  - Enter password if it does exist
- **OpenStego**
  - [https://www.openstego.com/](https://www.openstego.com/)
- **QuickStego**
  - Module 06: Lab0-Task1
- **Dirb (Web content scanner)**
  - [https://medium.com/tech-zoom/dirb-a-web-content-scanner-bc9cba624c86](https://medium.com/tech-zoom/dirb-a-web-content-scanner-bc9cba624c86)
  - [https://blog.csdn.net/weixin\_44912169/article/details/105655195](https://blog.csdn.net/weixin_44912169/article/details/105655195)
- **Searchsploit (Exploit-DB)**
  - [https://www.hackingarticles.in/comprehensive-guide-on-searchsploit/](https://www.hackingarticles.in/comprehensive-guide-on-searchsploit/)
- **Crunch (wordlist generator)**
  - [https://www.cnblogs.com/wpjamer/p/9913380.html](https://www.cnblogs.com/wpjamer/p/9913380.html)
- **Cewl (URL spider)**
  - [https://www.freebuf.com/articles/network/190128.html](https://www.freebuf.com/articles/network/190128.html)
- **Veracrypt**
  - Module 20: Lab4-Task1
- **Hashcalc**
  - Module 20: Lab1-Task1 (Nothing special)
- **Rainbow Crack**
  - Module 06: Lab0-Task0
- **Windows SMB**
  - smbclient -L [IP]
  - smbclient \\ip\\sharename
  - nmap -p 445 -sV –script smb-enum-services [IP]
- **Run Nmap at the beginning **
  - nmap -sn -PR  192.168.1.1/24 -oN ip.txt
  - nmap -A -T4 -vv -iL ip.txt -oN nmap.txt 
  - nmap -sU -sV -A -T4 -v -oN udp.txt 
 - **Snow**
  - ./snow -C -p "magic" output.txt  
  - snow -C -m "Secret Text Goes Here!" -p "magic" readme.txt readme2.txt
    • -m → Set your message
    • -p → Set your password
- **Rainbowcrack**
  - Use Winrtgen to generate a rainbow table
  - Launch RainbowCrack
  - File->Load NTLM Hashes from PWDUMP File
  - Rainbow Table->Search Rainbow Table
  - Use the generated rainbow table
  - RainbowCrack automatically starts to crack the hashes
**QuickStego**
  - Launch QuickStego
  - Open Image, and select target .jpg file
  - Open Text, and select a txt file
  - Hide text, save image file
  - Re-launch, Open Image
  - Select stego file
  - Hidden text shows up
--------------------------------------------------------------

mungkin saya harus menulkan dalam bahasa indoneisa angar dapat di pahami:

- **Peta**
 - Beberapa Lab
- **Hidra**
 - Modul 13: Lab2-Tugas1
- **Peta SQL**
 - Modul 15: Lab1-Tugas2
- **Pemindaian WPS**
 - Modul 14: Lab2-Tugas5
 - wpscan –-url http://10.10.10.10 -t 50 -U admin -P rockyou.txt
- **Nikto**
 - [https://zhuanlan.zhihu.com/p/124246499](https://zhuanlan.zhihu.com/p/124246499%20)
- **John**
 - Modul 06: Lab1-Tugas1
- **hashcat**
 - **Retak kata sandi MD5 dengan daftar kata:**
 - hashcat hash.txt -m 0 -a 0 hash.txt /usr/share/wordlists/rockyou.txt
 - **Retak kata sandi MD5 dalam format tertentu:**
 - hashcat -m 0 -a 3 ./hash.txt 'SKY-HQNT-?d?d?d?d&#39;
 - [https://xz.aliyun.com/t/4008](https://xz.aliyun.com/t/4008)
 - [https://tools.kali.org/password-actions/hashcat](https://tools.kali.org/password-actions/hashcat)
- **Metasploitasi**
 - Modul 14: Lab2-Tugas5
- **Respon LLMNR**
 - Modul 06: Lab1-Tugas1
- **Wireshark atau Tcpdump**
 - Beberapa Lab
- **Steghid**
 - **Bersembunyi**
 - steghide embed -cf [file img] -ef [file yang akan disembunyikan]
 - penyematan steghide -cf 1.jpg -ef 1.txt
 - Masukkan kata sandi atau lewati
 - **Ekstrak**
 - info steghide 1.jpg
 - ekstrak steghide -sf 1.jpg
 - Masukkan kata sandi jika memang ada
- **OpenStego**
 - [https://www.openstego.com/](https://www.openstego.com/)
- **QuickStego**
 - Modul 06: Lab0-Tugas1
- **Dirb (pemindai konten web)**
 - [https://medium.com/tech-zoom/dirb-a-web-content-scanner-bc9cba624c86](https://medium.com/tech-zoom/dirb-a-web-content-scanner-bc9cba624c86 )
 - [https://blog.csdn.net/weixin\_44912169/article/details/105655195](https://blog.csdn.net/weixin_44912169/article/details/105655195)
- **Eksploitasi Pencarian (Eksploitasi-DB)**
 - [https://www.hackingarticles.in/comprehensive-guide-on-searchsploit/](https://www.hackingarticles.in/comprehensive-guide-on-searchsploit/)
- **Crunch (pembuat daftar kata)**
 - [https://www.cnblogs.com/wpjamer/p/9913380.html](https://www.cnblogs.com/wpjamer/p/9913380.html)
- **Cewl (laba-laba URL)**
 - [https://www.freebuf.com/articles/network/190128.html](https://www.freebuf.com/articles/network/190128.html)
- **Verakript**
 - Modul 20: Lab4-Tugas1
- **Hashkalkulasi**
 - Modul 20: Lab1-Task1 (Tidak ada yang istimewa)
- **Retak Pelangi**
 - Modul 06: Lab0-Tugas0
- **Windows UKM**
 - klien smb -L [IP]
 - klien smb \\ip\\namaberbagi
 - nmap -p 445 -sV –script smb-enum-services [IP]
- **Jalankan Nmap di awal **
 - nmap -sn -PR 192.168.1.1/24 -oN ip.txt
 - nmap -A -T4 -vv -iL ip.txt -oN nmap.txt
 - nmap -sU -sV -A -T4 -v -on udp.txt
 - **Salju**
 - ./snow -C -p keluaran "ajaib".txt
 - snow -C -m "Teks Rahasia Ada di Sini!" -p "ajaib" readme.txt readme2.txt
 • -m → Atur pesan Anda
 • -p → Tetapkan kata sandi Anda
- **Retakan Pelangi**
 - Gunakan Winrtgen untuk menghasilkan tabel pelangi
 - Luncurkan RainbowCrack
 - File->Muat Hash NTLM dari File PWDUMP
 - Tabel Pelangi->Cari Tabel Pelangi
 - Gunakan tabel pelangi yang dihasilkan
 - RainbowCrack secara otomatis mulai memecahkan hash
**Stego Cepat**
 - Luncurkan QuickStego
 - Buka Gambar, dan pilih file .jpg target
 - Buka Teks, dan pilih file txt
 - Sembunyikan teks, simpan file gambar
 - Luncurkan kembali, Buka Gambar
 - Pilih file stego
 - Teks tersembunyi muncul
 
--------------------------------------------------- ------------

## Konsep

Cryptography/Kriptografi

[Definisi](../definitions/definitions_C.md#cryptography)

Non-repudiation/Non-penyangkalan

[Definisi](../definitions/definitions_N.md#non-repudiation)

Encryption/Enkripsi

[Definisi](../definitions/definitions_E.md#encryption)

Key disclosure law / Government access to keys (GAK)/Undang-undang pengungkapan kunci / Akses pemerintah terhadap kunci (GAK)

[Definisi](../definitions/definitions_K.md#key-disclosure-laws)
