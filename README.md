
# Konfigurasi Nginx Untuk Wordpress

Template konfigurasi web server Nginx untuk CMS Wordpress versi terbaru dengan fitur yang teroptimasi untuk melengkapi tutorial di [ITKoding](https://itkoding.com/).

## Fitur

+ Protokol HTTP/2 terbaru.
+ Web HTTPS dengan SSL / LetsEncrypt / Certbot.
+ TLSv1.3 terbaru.
+ Redirect dari non-www ke www dan http ke https.
+ Teroptimasi sesuai rekomendasi PageSpeed Insights Google. Browser cache static files, kompres dan nextgen image WebP.
+ Penggunaan `if` yang tepat untuk menghindari [ifisevil](https://www.nginx.com/resources/wiki/start/topics/depth/ifisevil/).
+ Beberapa contoh template server block.
+ Support plugin WP Fastest Cache.
+ Support plugin EWWW untuk WebP.
+ Support plugin Yoast.
+ SSL Stapling.

## Template Server Block yang Tersedia

+ Virtualhost/Server block dengan cache aktif (plugin WP Fastest Cache)
+ Virtualhost/Server block sementara untuk aktivasi letsencrypt.

## Keamanan

+ TLSv1 dan protokol lama yang tidak aman dinonaktifkan.
+ Mitigasi HTTPoxy vulnerability.
+ Support HSTS.
+ Keamanan header HTTP.
+ Semua hidden file penting tidak diizinkan akses.
+ Menonaktifkan xmlrpc untuk menghindari scanner.
+ Nilai A+ pada SSLLabs.

## Kompatibilitas

Telah di test pada:
+ Nginx 1.18.0
+ Ubuntu Server 20.04 LTS

## Cara Penggunaan

Langkah #1 - Install Wordpress dengan Nginx, PHP7.4-FPM dan MariaDB (LEMP).

Untuk cara lengkapnya silahkan baca pada tutorial yang saya tulis dengan tema [Cara Install Wordpress di VPS Ubuntu](https://itkoding.com/cara-install-wordpress-di-vps-ubuntu/).

Langkah #2 - Copy dan Paste semua file konfigurasi di Repo ini.

Copy semua file beserta folder dari repositori di Github ini lalu tempatkan pada /etc/nginx/.

Langkah #3 - Sesuaikan konfigurasi dengan nama domain dan SSL anda.

Ubah nama domain dan direktori root pada contoh template server block di /sites-available/. Ubah juga lokasi SSL anda yang tertulis di snippets/ssl/filessl_namadomain.conf


## Source

Konfigurasi ini menggunakan struktur konfigurasi pada repo milik [pothi](https://github.com/pothi/wordpress-nginx) yang kami perbarui sesuai dengan teknologi dan versi terbaru.