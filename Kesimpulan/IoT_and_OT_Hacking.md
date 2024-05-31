# Peretasan Perangkat IoT dan OT

Peretasan perangkat IoT dan OT dilakukan untuk mengkompromi perangkat pintar seperti kamera CCTV, mobil, printer, kunci pintu, mesin cuci, dll. untuk mendapatkan akses tidak sah ke sumber daya jaringan serta perangkat IoT dan OT.

Dengan menggunakan metodologi peretasan IoT dan OT, seorang penyerang memperoleh informasi menggunakan teknik seperti pengumpulan informasi, identifikasi area serangan, dan pemindaian kerentanan, dan menggunakan informasi tersebut untuk meretas perangkat dan jaringan target.

jejak digital pada protokol MQTT, yang merupakan protokol konektivitas mesin-ke-mesin (M2M) atau "Internet of Things". Ini berguna untuk koneksi dengan lokasi terpencil di mana jejak kode kecil diperlukan dan/atau bandwidth jaringan terbatas.

Berikut adalah berbagai tahap peretasan perangkat IoT dan OT:

- Pengumpulan informasi
- Pemindaian kerentanan
- Melancarkan serangan
- Memperoleh akses jarak jauh
- Mempertahankan akses

Mengumpulkan Informasi menggunakan Alat Jejak Digital Online
- Informasi mengenai perangkat IoT dan OT target dapat diperoleh menggunakan berbagai sumber online seperti pencarian domain Whois, Google hacking lanjutan, dan mesin pencari Shodan. Informasi yang terkumpul dapat digunakan untuk memindai perangkat-perangkat tersebut untuk kerentanan dan lebih lanjut memanfaatkannya untuk melancarkan serangan.

- https://www.whois.com/whois/
- https://www.exploit-db.com/google-hacking-database jenis SCADA
- "login" intitle:"scada login"
- https://www.shodan.io/dashboard
  - port:1883
  - Cari Sistem ICS/SCADA yang Mendukung Modbus:
    - port:502
  - Cari sistem SCADA menggunakan nama PLC:
    - “Schneider Electric”
  - Cari sistem SCADA menggunakan geolokasi:
    - Negara SCADA:"US"

Gambaran Lalu Lintas IoT dan OT:

- Banyak perangkat IoT seperti kamera keamanan memiliki situs web untuk mengendalikan atau mengkonfigurasi kamera dari lokasi jarak jauh. Situs web ini sebagian besar menerapkan protokol HTTP yang tidak aman daripada protokol HTTPS yang aman dan, oleh karena itu, rentan terhadap berbagai serangan. Jika kamera menggunakan kredensial pabrik default, seorang penyerang dapat dengan mudah menangkap semua lalu lintas yang mengalir antara kamera dan aplikasi web serta mendapatkan akses ke kamera itu sendiri. Penyerang dapat menggunakan alat seperti Wireshark untuk menangkap lalu lintas tersebut dan mendekripsi kunci Wi-Fi dari jaringan target.
