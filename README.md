[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/s7OBVfDF)
| Name | NRP | Kelas |
| -------------------- | ---------- | --------------------- |
| Nuril Qolbi Zam Zami | 5025221296 | Jaringan Komputer (A) |
| Alvin Zanua Putra | 5025231064 | Jaringan Komputer (A) |

---

# INI TAMBAHAN

### LINK EXCEL

    https://docs.google.com/spreadsheets/d/1vWKrSwMVmna7snJVwqiB_1zfyTIO4V2M4wk4YMxP8Mw/edit?usp=sharing

### LINK FIGMA

    https://www.figma.com/design/t1t3tUZBNAtzaMsePE2G3R/JARKOM?node-id=0-1&t=jWHtJaTWfy8XW47i-1

# INI TAMBAHAN END

---

## Put your topology config image here!

![alt text](/assets/images/topology.jpg)

## Put your VLSM calculation here!

![alt text](/assets/images/vlsm.jpg)

<b>Tree:</b>

![alt text](/assets/images/tree.jpg)

## Put your IP route here!

### Subnetting

- Heiji

```bash
auto eth0
iface eth0 inet dhcp

#A1
auto eth1
iface eth1 inet static
address 10.6.0.1
netmask 255.255.255.252

#A6
auto eth2
iface eth2 inet static
address 10.6.0.13
netmask 255.255.255.252
```

- Agasa

```bash
auto eth0
iface eth0 inet static
address 10.6.0.2
netmask 255.255.255.252
gateway 10.6.0.1

#A2
auto eth1
iface eth1 inet static
address 10.6.0.5
netmask 255.255.255.252

#A5
auto eth2
iface eth2 inet static
address 10.6.4.1
netmask 255.255.252.0
```

- Ran

```bash
auto eth0
iface eth0 inet static
address 10.6.4.2
netmask 255.255.252.0
gateway 10.6.4.1
```

- Shinici

```bash
auto eth0
iface eth0 inet static
address 10.6.1.2
netmask 255.255.255.128
gateway 10.6.1.1
```

- Haibara

```bash
auto eth0
iface eth0 inet static
address 10.6.8.2
netmask 255.255.248.0
gateway 10.6.8.1
```

- Conan

```bash
auto eth0
iface eth0 inet static
address 10.6.1.3
netmask 255.255.255.128
gateway 10.6.1.1
```

- Megure

```bash
auto eth0
iface eth0 inet static
address 10.6.0.22
netmask 255.255.255.252
gateway 10.6.0.21
```

- Sonoko

```bash
auto eth0
iface eth0 inet static
address 10.6.0.10
netmask 255.255.255.252
gateway 10.6.0.9
```

- Kazuha

```bash
auto eth0
iface eth0 inet static
address 10.6.0.6
netmask 255.255.255.252
gateway 10.6.0.5

# A3

auto eth1
iface eth1 inet static
address 10.6.8.1
netmask 255.255.248.0

# A4

auto eth2
iface eth2 inet static
address 10.6.0.9
netmask 255.255.255.252
```

- Ayumi

```bash
auto eth0
iface eth0 inet static
address 10.6.0.14
netmask 255.255.255.252
gateway 10.6.0.13

# A7

auto eth1
iface eth1 inet static
address 10.6.1.1
netmask 255.255.255.128

# A8

auto eth2
iface eth2 inet static
address 10.6.0.17
netmask 255.255.255.252
```

- Mitshuhiko

```bash
auto eth0
iface eth0 inet static
address 10.6.0.18
netmask 255.255.255.252
gateway 10.6.0.17

# A9

auto eth1
iface eth1 inet static
address 10.6.0.21
netmask 255.255.255.252

# A10

auto eth2
iface eth2 inet static
address 10.6.2.2
netmask 255.255.255.0
```

- Kogoro

```bash
auto eth0
iface eth0 inet static
address 10.6.2.3
netmask 255.255.255.0
gateway 10.6.2.2
```

- Genta

```bash
auto eth0
iface eth0 inet static
paddress 10.6.2.2
netmask 255.255.255.0
gateway 10.6.2.2
```

### Routing (taruh bashrc)

- Kazuha

```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.6.0.5
```

- Mitsuhiko

```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.6.0.17
```

- Agasa

```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.6.0.1
route add -net 10.6.8.0 netmask 255.255.248.0 gw 10.6.0.6 #A3
route add -net 10.6.0.8 netmask 255.255.255.252 gw 10.6.0.6 #A4
```

- Ayumi

```bash
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.6.0.13
route add -net 10.6.0.20 netmask 255.255.255.252 gw 10.6.0.18 #A9
route add -net 10.6.2.0 netmask 255.255.255.0 gw 10.6.0.18 # A10
```

- Heiji

```bash
route add -net 10.6.2.0 netmask 255.255.255.0 gw 10.6.0.14 # A10
route add -net 10.6.0.16 netmask 255.255.255.252 gw 10.6.0.14 #A8
route add -net 10.6.0.20 netmask 255.255.255.252 gw 10.6.0.14 #A9
route add -net 10.6.1.0 netmask 255.255.255.128 gw 10.6.0.14 #A7
route add -net 10.6.0.4 netmask 255.255.255.252 gw 10.6.0.2 #A2
route add -net 10.6.8.0 netmask 255.255.248.0 gw 10.6.0.2 #A3
route add -net 10.6.0.8 netmask 255.255.255.252 gw 10.6.0.2 #A4
route add -net 10.6.4.0 netmask 255.255.252.0 gw 10.6.0.2 #A5
```

### Installasi

- Heiji

```bash
# DHCP relay
echo 'nameserver 192.168.122.1' > /etc/resolv.conf

apt update
apt install netcat -y
apt install isc-dhcp-relay -y

echo '
SERVERS="10.6.1.106"
INTERFACES="eth0 eth1 eth2 eth3"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

# Jangan lupa uncomment
# nano /etc/sysctl.conf
# net.ipv4.ip_forward=1

service isc-dhcp-relay restart
```

## Soal 1

> Bagaimana cara mengkonfigurasi iptables pada router bernama 'Heiji' agar memungkinkan jaringan mengakses internet melalui interface eth0 menggunakan SNAT tanpa menggunakan MASQUERADE?

> _How to configure iptables on a router named ‘Heiji’ to allow the network to access the internet through interface eth0 using SNAT without using MASQUERADE?_

**Answer:**

- Screenshot

Sebelum :

![alt text](/assets/images/NOMOR1-1.jpg)

Setelah :

- Configuration

```bash
IPETH0="$(ip -br a | grep eth0 | awk '{print $NF}' | cut -d'/' -f1)"
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source "$IPETH0" -s 10.6.0.0/20
```

- Explanation

  `Perintah ini menggunakan iptables untuk mengonfigurasi SNAT (Source Network Address Translation) agar memungkinkan perangkat dalam jaringan dengan rentang IP 10.6.0.0/20 untuk mengakses internet melalui eth0. SNAT diperlukan untuk mengubah alamat IP sumber dari perangkat di jaringan lokal menjadi alamat IP dari antarmuka eth0, yang biasanya memiliki akses ke internet. Tanpa MASQUERADE, kita spesifik mengatur IP sumber pada eth0.`

<br>

## Soal 2

> Kalian diminta untuk melakukan drop semua paket masuk TCP kecuali pada port 1744 pada node Shinichi.

> _You are asked to drop all incoming TCP packets except on port 1744 on Shinichi's node_

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
#Shinichi
iptables -A INPUT -p tcp -d 10.6.1.2 --dport 1744 -j ACCEPT
iptables -A INPUT -p tcp -j DROP
```

- Explanation

`Aturan iptables ini: Mengizinkan koneksi TCP yang datang ke port 1744. Menolak semua paket TCP lainnya. Dengan urutan ini, pengecualian port 1744 diterapkan terlebih dahulu sebelum aturan drop paket lainnya.`

<br>

## Soal 3

> Lakukan pembatasan sehingga koneksi SSH pada semua Web Server hanya dapat dilakukan oleh user yang berada pada node Ran.

> _Make restrictions so that SSH connections to all Web Servers can only be made by users who are on the Ran node._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
#Semua Web Server
iptables -A INPUT -p tcp --dport 22 -s 10.6.4.2 -j ACCEPT
iptables -A INPUT -p tcp --dport 22 -j DROP
```

- Explanation

  `Aturan ini mengizinkan hanya Ran (IP 10.6.4.2) untuk melakukan koneksi SSH (port 22) ke Web Server. Semua koneksi SSH lainnya akan ditolak.`

<br>

## Soal 4

> Semua subnet hanya dapat mengakses Web Server pada port 80 dan 443 (Conan, Sonoko, dan Megure) pada hari Senin-Jumat, pukul 07:00- 19:00.

> _All subnets can access the Web Server (Conan, Sonoko, and Megure) only on ports 80 and 443, from Monday to Friday, between 07:00-19:00._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
#Semua Web Server
iptables -A INPUT -p tcp --dport 80 -m time --weekdays Mon,Tue,Wed,Thu,Fri --timestart 07:00 --timestop 19:00 -j ACCEPT
iptables -A INPUT -p tcp --dport 443 -m time --weekdays Mon,Tue,Wed,Thu,Fri --timestart 07:00 --timestop 19:00 -j ACCEPT

iptables -A INPUT -p tcp --dport 80 -j DROP
iptables -A INPUT -p tcp --dport 443 -j DROP
```

- Explanation

  `Menggunakan modul time di iptables untuk menentukan hari dan jam spesifik ketika koneksi diizinkan. Jika permintaan datang di luar waktu tersebut, koneksi akan ditolak.`

<br>

## Soal 5

> Ternyata subnet Haibara memiliki akses tambahan, yaitu dapat mengakses Web Server pada port 80 dan 443 di luar hari Senin-Jumat (hari Sabtu dan Minggu), tanpa pembatasan waktu.

> _The Haibara subnet has additional access, allowing it to access the Web Server on ports 80 and 443 outside of Monday to Friday (on Saturday and Sunday), with no time restrictions._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
iptables -A INPUT -p tcp -s 10.6.8.0/21 --dport 80 -m time --weekdays Sat,Sun -j ACCEPT
iptables -A INPUT -p tcp -s 10.6.8.0/21 --dport 443 -m time --weekdays Sat,Sun -j ACCEPT
```

- Explanation

  `Subnet Haibara (10.6.8.0/21) diberikan izin akses tanpa pembatasan waktu pada hari Sabtu dan Minggu untuk port 80 dan 443. Aturan ini ditambahkan khusus untuk subnet tersebut, tanpa mengganggu konfigurasi lainnya.`

<br>

## Soal 6

> Akses ke Web Server Conan, Sonoko, dan Megure pada port 80 dan 443 dilarang pada hari Jumat, pukul 11:00-13:00 (maklum, Jumatan rek).

> _Access to the Web Server (Conan, Sonoko, and Megure) on ports 80 and 443 is prohibited on Fridays between 11:00-13:00 (It's Friday prayer time)._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
iptables -A INPUT -p tcp --dport 80 -m time --weekdays Fri --timestart 11:00 --timestop 13:00 -j DROP
iptables -A INPUT -p tcp --dport 443 -m time --weekdays Fri --timestart 11:00 --timestop 13:00 -j DROP
```

- Explanation

  `Modul time kembali digunakan untuk memblokir akses selama waktu tertentu, yaitu saat ibadah Jumat. Aturan ini mencegah perangkat lain mengakses port 80 dan 443 pada waktu tersebut.`

<br>

## Soal 7

> Tambahkan logging paket yang di-drop di setiap node server dan router.

> _Enable logging for dropped packets on every server node and router._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
iptables -A INPUT  -j LOG --log-level debug --log-prefix 'Package Dropped' -m limit --limit 1/second --limit-burst 10
```

- Explanation

  `Menggunakan fitur LOG dari iptables untuk mencatat informasi tentang paket yang ditolak. Parameter --log-level menentukan tingkat detail log, dan --log-prefix menambahkan teks identifikasi ke log.`

<br>

## Soal 8

> Untuk keperluan maintenance, pilih salah satu Subnet dan lakukan blokir terhadap semua request protokol ICMP (ping) dari luar subnet terhadap subnet tersebut.

> _For maintenance purposes, select one Subnet and block all ICMP (ping) protocol requests from outside the subnet to that subnet._

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
iptables -A INPUT -p icmp ! -s 10.6.2.0/23 -d 10.6.2.0/23 -j DROP
```

- Explanation

  `Dengan aturan ini, semua paket ICMP (ping) yang berasal dari luar subnet tertentu akan ditolak. Ini memastikan bahwa subnet tersebut tidak dapat di-ping dari perangkat luar selama masa pemeliharaan.`

<br>

## Soal 9

> Untuk meningkatkan keamanan, setiap Web Server harus bisa melakukan blok terhadap IP yang melakukan scanning port dalam jumlah yang tidak wajar (maksimal 10 scan port) di dalam selang waktu 1 menit.

> _To enhance security, each Web Server must be able to block IP addresses that perform an excessive number of port scans (a maximum of 10 port scans) within a 1-minute interval._

**Answer:**

- Screenshot

  `Modul recent digunakan untuk mendeteksi aktivitas port scan. Jika sebuah IP melakukan lebih dari 10 scan dalam waktu 60 detik, IP tersebut akan diblokir sementara, melindungi server dari potensi serangan.`

- Configuration

```bash
iptables -A INPUT -m recent --name portscan --update --seconds 60 --hitcount 10 -j DROP
iptables -A FORWARD -m recent --name portscan --update --seconds 60 --hitcount 10 -j DROP
iptables -A INPUT -m recent --name portscan --set -j ACCEPT
iptables -A FORWARD -m recent --name portscan --set -j ACCEPT
```

- Explanation

  `Put your explanation in here`

<br>

## Soal 10

> Akses dari client ke WebServer Conan pada port 80 akan didistribusikan bergantian antara Web Server Conan dan Web Server Sonoko. Sebaliknya akses pada Web Server Sonoko pada port 443 akan didistribusikan bergantian antara Web Server Conan dan Web Server Sonoko. Lakukan evaluasi menggunakan Jmeter terhadap berbagai metode load balancing seperti Round-Robin dan lain-lainnya.

> _Client access to the Conan Web Server on port 80 should be alternated between the Conan Web Server and the Sonoko Web Server. Conversely, access to the Sonoko Web Server on port 443 should be alternated between the Conan Web Server and the Sonoko Web Server. (Evaluate various load balancing methods, such as Round-Robin and others, using JMeter.)_

**Answer:**

- Screenshot

  `Put your screenshot in here`

- Configuration

```bash
echo '
Listen 80
Listen 443

<IfModule ssl_module>
        Listen 443
</IfModule>

<IfModule mod_gnutls.c>
        Listen 443
</IfModule>
' > /etc/apache2/ports.conf
```

```bash
#Conan
echo '# Conan
Conan' > /var/www/html/index.html
```

```bash
#Senoko
echo '# Senoko
Senoko' > /var/www/html/index.html
```

```bash
#Conan
<VirtualHost *:80>
    ServerName 10.6.0.10
    DocumentRoot /var/www/html
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
<VirtualHost *:443>
    ServerName 10.6.0.10
    DocumentRoot /var/www/html
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

- Explanation

  `Round-Robin diterapkan untuk mendistribusikan permintaan klien secara bergantian antara dua server (Conan dan Sonoko) pada port 80 dan 443. Untuk mengimplementasikan hal ini, pengaturan Apache Web Server atau mekanisme load balancer seperti HAProxy dapat digunakan. JMeter digunakan untuk mengevaluasi kinerja dan membandingkan dengan metode lainnya.`

<br>

## Problems

## Revisions (if any)

```

```
