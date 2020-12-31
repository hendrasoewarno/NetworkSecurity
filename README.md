# NetworkSecurity
Mengamankan jaringan dari serangan<br>
Adapun metodologi yang sering dilakukan Hacker dalam pentest terhadap suatu jaringan adalah:<br>
1. Reconnaisance
2. Scanning
3. Vulnerability Identification
4. Exploitation
5. Post Exploitation
## Reconaisance
Upaya teknikal maupun non-teknikal untuk mendapatkan informasi awal sebanyak-banyaknya terkait dengan objek, melalui aktivitas offline maupun online. Mencoba mendapatkan informasi melalui sosial engineering (menyamar jadi customer, jasa service, menawarkan produk, dan menjalin pertemanan) sampai kepada mencari informasi dari tempat sampah, maupun web dan sosial media (Google, Facebook, dll) untuk mendapatkan informasi sebanyak-banyaknya terkait dengan teknologi, people dan proses (policy) yang dimiliki target.
## Scanning
Upaya teknikal maupun non-teknikal untuk dengan kunjungan ke objek serangan, maupun melakukan scanning ke jaringan/server untuk mendapatkan jumlah server, informasi port/layanan yang terbuka.
## Vulnerability Indentification
Pada saat Reconaisance dan scanning berusaha mengidentifikasi domain-name, subdomain, ip-address, server, versi OS, jenis Firewall, aplikasi yang terinstalasi, service provider yang digunakan. Untuk kemungkinan adanya kelemahan pada software, kesalahan rancangan, kesalahan konfigurasi, maupun kekurangan pengendalian operasional yang menyebabkan celah tersebut terbuka.
## Exploitation
Mencoba melakukan tindakan pentest dengan mengeksploitasi vulnerability yang berhasil diidentfikasi untuk mendapatkan akses seperti root level pada OS, admin level pada aplikasi, jika tidak bisa maka berusaha mendapatkan user account dan meningkatkan user account tersebut ke privilede yang lebih tinggi. Pentest juga dapat berupa tindakan DoS untuk menguji sejauh apa server dapat mendeteksi mempertahankan availbilitynya.
## Post Exploitation
Pada tindakan pentest, kegiatan lanjutan adalah membuat laporan dan dokumentasi atas temuan, membuat prove of concept terkait dengan temuan celah, dan saran bagaimana temuan tersebut dapat di mitigasi. Tetapi jika terjadi pada serangan sebenarnya, maka Hacker akan membuat upaya akses jangka panjang ke sistem, menghapus jejak forensic atas serangan, mencuri data untuk keuntungan tertentu.
