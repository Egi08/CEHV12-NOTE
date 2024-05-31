# Bagian 02: Web Applications Threats/Ancaman Aplikasi Web

## Ancaman Aplikasi Web

Open web application security project (OWASP)/Buka proyek keamanan aplikasi web (OWASP)

[Definisi](../definitions/definitions_O.md#open-web-application-security-project)

### OWASP top 10/OWASP 10 teratas

OWASP Top 10 adalah dokumen kesadaran standar untuk pengembang dan keamanan aplikasi web.
Ini mewakili konsensus luas mengenai risiko keamanan paling kritis terhadap aplikasi web.

- [A01:2021-Broken Access Control](https://owasp.org/Top10/A01_2021-Broken_Access_Control) naik dari posisi kelima; 94% aplikasi diuji untuk beberapa bentuk kontrol akses yang rusak. 34 Common Weakness Enumerations (CWEs) yang dipetakan ke Kontrol Akses Rusak memiliki lebih banyak kemunculan dalam aplikasi dibandingkan kategori lainnya.
- [A02:2021-Cryptographic Failures](https://owasp.org/Top10/A02_2021-Cryptographic_Failures) naik satu posisi ke posisi #2, yang sebelumnya dikenal sebagai Paparan Data Sensitif, yang merupakan gejala umum dan bukan penyebab utama. Fokus baru di sini adalah pada kegagalan terkait kriptografi yang sering kali menyebabkan paparan data sensitif atau gangguan sistem.
- [A03:2021-Injection](https://owasp.org/Top10/A03_2021-Injection) meluncur turun ke posisi ketiga. 94% aplikasi diuji untuk beberapa bentuk injeksi, dan 33 CWE yang dipetakan ke dalam kategori ini memiliki kemunculan terbanyak kedua dalam aplikasi. Skrip Lintas Situs kini menjadi bagian dari kategori ini di edisi ini.
- [A04:2021-Insecure Design](https://owasp.org/Top10/A04_2021-Insecure_Design) adalah kategori baru untuk tahun 2021, dengan fokus pada risiko terkait cacat desain. Jika kita benar-benar ingin “bergerak ke kiri” sebagai sebuah industri, hal ini memerlukan lebih banyak penggunaan pemodelan ancaman, pola dan prinsip desain yang aman, dan arsitektur referensi.
- [A05:2021-Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration) naik dari #6 pada edisi sebelumnya; 90% aplikasi diuji untuk beberapa bentuk kesalahan konfigurasi. Dengan semakin banyaknya peralihan ke perangkat lunak yang sangat dapat dikonfigurasi, tidak mengherankan jika kategori ini naik. Kategori sebelumnya untuk Entitas Eksternal XML (XXE) kini menjadi bagian dari kategori ini.
- [A06:2021-Vulnerable_and_Outdated_Components](https://owasp.org/Top10/A06_2021-Vulnerable_and_Outdated_Components) sebelumnya berjudul Menggunakan Komponen dengan Kerentanan yang Diketahui dan menduduki peringkat ke-2 dalam 10 survei komunitas Teratas, namun juga memiliki cukup data untuk masuk 10 Besar melalui analisis data. Kategori ini naik dari #9 pada tahun 2017 dan merupakan masalah umum yang sulit kami uji dan nilai risikonya. Ini adalah satu-satunya kategori yang tidak memiliki Kerentanan dan Eksposur Umum (CVE) yang dipetakan ke CWE yang disertakan, sehingga bobot eksploitasi dan dampak default sebesar 5,0 diperhitungkan dalam skor mereka.
- [A07:2021-Identification and Authentication Failures](https://owasp.org/Top10/A07_2021-Identification_and_Authentication_Failures) sebelumnya adalah Broken Authentication dan meluncur ke bawah dari posisi kedua, dan sekarang mencakup CWE yang lebih terkait dengan kegagalan identifikasi . Kategori ini masih merupakan bagian integral dari 10 Besar, namun peningkatan ketersediaan kerangka kerja standar tampaknya membantu.
- [A08:2021-Software and Data Integrity Failures](https://owasp.org/Top10/A08_2021-Software_and_Data_Integrity_Failures) adalah kategori baru untuk tahun 2021, dengan fokus pada pembuatan asumsi terkait pembaruan perangkat lunak, data penting, dan CI/CD saluran pipa tanpa memverifikasi integritasnya. Salah satu dampak dengan bobot tertinggi dari data Common Vulnerability and Exposures/Common Vulnerability Scoring System (CVE/CVSS) yang dipetakan ke 10 CWE dalam kategori ini. Deserialisasi Tidak Aman dari tahun 2017 kini menjadi bagian dari kategori yang lebih besar ini.
- [A09:2021-Kegagalan Logging dan Pemantauan Keamanan](https://owasp.org/Top10/A09_2021-Security_Logging_and_Monitoring_Failures) sebelumnya Logging & Monitoring Tidak Memadai dan ditambahkan dari survei industri (#3), naik dari #10 sebelumnya. Kategori ini diperluas untuk mencakup lebih banyak jenis kegagalan, sulit untuk diuji, dan tidak terwakili dengan baik dalam data CVE/CVSS. Namun, kegagalan dalam kategori ini dapat berdampak langsung pada visibilitas, peringatan insiden, dan forensik.
- [A10:2021-Server-Side Request Forgery](https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29) ditambahkan dari survei komunitas 10 Teratas (#1). Data menunjukkan tingkat kejadian yang relatif rendah dengan cakupan pengujian di atas rata-rata, serta peringkat potensi Eksploitasi dan Dampak di atas rata-rata. Kategori ini mewakili skenario di mana anggota komunitas keamanan mengatakan kepada kita bahwa hal ini penting, meskipun hal tersebut tidak diilustrasikan dalam data saat ini.

Structured query language (SQL) injection/Injeksi bahasa kueri terstruktur (SQL).

[Definisi](../definitions/definitions_S.md#struktur-query-bahasa-injeksi)

Command injection/Injeksi perintah

[Definisi](../definitions/definitions_C.md#command-injection)

Cross site scripting (XSS)/Skrip lintas situs (XSS)

[Definisi](../definitions/definitions_C.md#cross-site-scripting)

Cross site request forgery/Pemalsuan permintaan lintas situs

[Definisi](../definitions/definitions_C.md#cross-site-request-forgery)

extensible markup language (XML)/bahasa markup yang dapat diperluas (XML)

[Definisi](../definitions/definitions_E.md#extensible-markup-bahasa)

Directory traversal/Penjelajahan direktori

[Definisi](../definitions/definitions_D.md#directory-traversal)

Watering hole attack/Serangan lubang berair

[Definisi](../definitions/definitions_W.md#watering-hole-serangan)

Session poisoning/Keracunan sesi

[Definisi](../definitions/definitions_S.md#session-poisoning)

Clickjacking/Pembajakan klik

[Definisi](../definitions/definitions_C.md#clickjacking)

Pass the hash/Berikan hashnya

[Definisi](../definitions/definitions_P.md#pass-the-hash)

Tautan

- [https://owasp.org/www-project-top-ten](https://owasp.org/www-project-top-ten)
