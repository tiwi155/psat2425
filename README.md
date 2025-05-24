# Penilaian Sumatif Akhir Tahun
## Mapil DevOps XI TJKT 1 - Penilaian Praktek
### SMKN 1 Banyumas - TA. 2024 2025
#### HIKMAH NUR PRASTIWI(13)

#
# Cara mendeploy Aplikasi

## 1. Hubungkan dengan akun AWS
## -Login ke AWS terlebih dahulu
## -Start mesin dan buat 2 security group
## -Security pertama untuk database, izinkan indbound MySql (3306) from anywhereIPv4 (0.0.0.0/0)
## -Security kedua untuk web, izinkan indbound rules SSH(22), HTTP(80), HTTPS(443) from anywhereIPv4 (0.0.0.0/0)
## -Buat database di Aurora dan RDS, dengan Engine Type MySql, Templates Free Tier, isi password, untuk Public Access pilih NO (karena kita akan membuat di jarngan private(opsional)), dan pastikan security group pilih yang alllow port 3306 dari 0.0.0.0/0
## -Buat instance EC2, pilih mesin Ubuntu dan security group yang web(kedua)
## -Scroll ke bawah dan cari "advanced details"  tambahkan kode seperti di bawah ini ke dalam kotak yang ada

## KODE

## #!/bin/bash
## $ apt update -y
## $ apt install -y apache2 php php-mysql libapache2-mod-php mysql-client
## $ rm -rf /var/www/html/{*,.*}
## $ git clone https://github.com/akun githubmu/nama repository github.git /var/www/html
## $ chmod -R 777 /var/www/html
## echo DB_USER=admin > /var/www/html/.env (biarkan admin)
## echo DB_PASS=mieayam  >> /var/www/html/.env (isi dengan password yang tad diisi saat membuat RDS)
## echo DB_NAME=psat2425  >> /var/www/html/.env (Isi dengan nama repository githubmu)
## echo DB_HOST=rdstiwi.czt6n8ylfvyb.us-east-1.rds.amazonaws.com >> /var/www/html/.env (Isi dengan Endpoint RDS yang tadi sudah dibuat)
## $ apt install openssl
## $ a2enmod ssl
## $ a2ensite default-ssl.conf
## systemctl reload apache2

## -Lalu klik create, tunggu sebentar dan connect dengan memilih ip publik
## -Jalankan kode dengan perintah
## $ bash otomatis.sh
## -Salin IP Publik di bawah kiri dan ketikkan di chrome, maka webmu seharusnya sudah muncul


## 2. Jalankan 
Jalankan dengan username dan password default berikut ini
#
### username = admin
### password = 123
#

Kemudian inputkanlah data sesuai dengan datamu




