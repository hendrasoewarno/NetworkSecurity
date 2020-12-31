# Network Security
Sebelum mengalami serangan oleh Hacker, alangkah baiknya setiap Admin melakukan Pentest terhadap server/jaringan masing-masing<br>
Adapun metodologi yang sering dilakukan Hacker dalam serangan terhadap suatu jaringan adalah:<br>
1. Reconnaisance
2. Scanning
3. Vulnerability Identification
4. Exploitation
5. Post Exploitation</br>
Sehingga kita perlu melakukan pendekatan yang sama dengan apa yang Hacker untuk mengamankan server/jaringan.
## Beberapa istilah
1. Vulnerability, suatu kelemahan pada sistem yang memperbolehkan penyerang untuk melakukan tindakan eksploit.
2. Exploit, tindakan atau koding yang memungkinkan penyerang merealisasikan vulnerability dari sistem yang ditemukan.
3. Payload, kode yang dikirim setelah eksploit berhasil direalisasikan, payload dijalankan pada sistem untuk ekploitasi lanjutan seperti Shell Code.
4. Encoder, metode untuk mengacak payload sehingga terhindar dari deteksi oleh IDS.
## Reconaisance
Upaya teknikal maupun non-teknikal untuk mendapatkan informasi awal sebanyak-banyaknya terkait dengan objek, melalui aktivitas offline maupun online. Mencoba mendapatkan informasi melalui sosial engineering (menyamar jadi customer, jasa service, menawarkan produk, dan menjalin pertemanan) seperti pertukaran kartu nama, sampai kepada mencari informasi dari tempat sampah, maupun web dan sosial media (Google, Facebook, dll) untuk mendapatkan informasi sebanyak-banyaknya terkait dengan teknologi, people dan proses (policy) yang dimiliki target seperti ip address, network topology, domain dan sub-domain name, account login seperti firstname, lastname, dan account email, OS dan Software, security policy, sistem keamanan fisik, lokasi hangout karyawan untuk mendapatkan badge name, sampai kepada tindakan Phising dan Reverse Shell.
### Contoh upaya Reconaisance secara online
Search pada Google dengan keyword
```
site: <target domain>
link: <target domain>
related: <nama perusahaan>
```
Menggunakan WHOIS dan dig untuk mendapatkan informasi terkait dengan target Domain seperti A, MX, NS, CNAME, SOA, SRV, RP, PTR, TXT, HINFO (misalkan https://pentest-tools.com/information-gathering/find-domains-owned-by-company#, https://pentest-tools.com/information-gathering/find-subdomains-of-domain#)
## Scanning
Upaya teknikal maupun non-teknikal untuk dengan kunjungan ke objek serangan, maupun melakukan scanning ke jaringan/server untuk mendapatkan jumlah server, informasi port/layanan yang terbuka (misalkan: https://pentest-tools.com/network-vulnerability-scanning/tcp-port-scanner-online-nmap#, https://pentest-tools.com/information-gathering/website-reconnaissance-discover-web-application-technologies)
## Vulnerability Indentification
Pada saat Reconaisance dan scanning berusaha mengidentifikasi domain-name, subdomain, ip-address, server, versi OS, jenis Firewall, aplikasi yang terinstalasi, service provider yang digunakan. Untuk kemungkinan adanya kelemahan pada software, kesalahan rancangan, kesalahan konfigurasi, maupun kekurangan pengendalian operasional yang menyebabkan celah tersebut terbuka.
## Exploitation
Mencoba melakukan tindakan pentest dengan mengeksploitasi vulnerability yang berhasil diidentfikasi untuk mendapatkan akses seperti root level pada OS, admin level pada aplikasi, jika tidak bisa maka berusaha mendapatkan user account dan meningkatkan user account tersebut ke privilede yang lebih tinggi. Pentest juga dapat berupa tindakan DoS untuk menguji sejauh apa server dapat mendeteksi mempertahankan availabitity. Contoh eksploitasi pada Windows:
1. Awalnya eksploit dikirim ke target untuk memungkinkan remote execution
2. Eksploit yang dikirim adalah suatu payload kecil yang menyebabkan target melakukan koneksi balik ke server yang telah disiapkan penyerang diinternet.
3. Setelah koneksi, payload akan mendownload payload yang lebih besar untuk eksplotasi lanjutan
4. Suatu DLL injection dilakukan, dan menginstalasi Metapreter untuk suatu server DLL
5. Dan server diinternet dan target berkomunikasi
6. Eksploitasi dilanjutkan pada server/client lainnya yang berada dalam LAN dengan software seperti Armitage.
## Post Exploitation
Pada tindakan pentest, kegiatan lanjutan adalah membuat laporan dan dokumentasi atas temuan, membuat prove of concept terkait dengan temuan celah, dan saran bagaimana temuan tersebut dapat di mitigasi. Tetapi jika terjadi pada serangan sebenarnya, maka Hacker akan membuat upaya akses jangka panjang ke sistem dengan menanam Shell Code seperti Meterpreter ataupun Reversed Shell, dan menginstalasi trojan, menghapus jejak forensic atas serangan, mencuri data untuk keuntungan tertentu. Untuk mempertahankan akses jangka panjang, Hacker memanfaatkan fitur seperti xinitd, initd, systemmd pada Linux, maupun registry Windows yang start service, dan launchd pada OSx untuk mengaktifkan trojan, keylogger, remote proxy, maupun BOTnet yang telah diinstalasi ke sistem. Software-software tersebut dilengkapi dengan kemampuan ROOTkit pada level user maupun kernel untuk menyembunyikan diri dari user.
# Metasploit
Metasplot dikembangkan oleh H.D. Moore yang berprofesi sebagai Pentester, beliau menyadari didalam melakukan profesinya, dia sering melakukan aktifitas eksploit yang sama secara berulang, dan dia mengembangan Metasploit untuk mengotomatisasi beberapa hal sebagai framework untuk berbagai payload, dan bersifat open source sehingga memungkinkan kontribusi dari berbagai pihak diinternet.
# Netcat
Netcat dikembangkan oleh Hobbit pada maret 1996 yang dikenal sebagai Swiss Army network tools. berjalan pada platform - Linux, Windows, OS X, SunOS, Solaris, dll secara UDP maupun TCP.
# Cain and Abel
Merupakan software password recovery tools yang berjalan pada platform Windows yang memiliki kemampuan packet sniffing, password hashes dengan metode bruteforce. 
# Beberapa Web untuk Pentest
1. https://www.metasploit.com
2. http://sqlmap.org/ dan https://github.com/sqlmapproject/sqlma
3. https://github.com/sullo/nikto
4. https://pentest-tools.com/home
