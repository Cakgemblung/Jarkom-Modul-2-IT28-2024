# Jarkom-Modul-2-IT28-2024

|Nama  | NRP |
|--    | --  |
| Muhammad Hildan Adiwena  | 5027231077 |
| Syela Zeruya Tandi Lalong  | 5027231076 |

## Topologi

![WhatsApp Image 2024-10-03 at 21 07 51](https://github.com/user-attachments/assets/6b8124d0-9f93-4927-9147-6492b892a102)

## No. 1
Untuk mempersiapkan peperangan World War MMXXIV (Iya sebanyak itu), Sriwijaya membuat dua kotanya menjadi web server yaitu Tanjungkulai, dan Bedahulu, serta Sriwijaya sendiri akan menjadi DNS Master. Kemudian karena merasa terdesak, Majapahit memberikan bantuan dan menjadikan kerajaannya (Majapahit) menjadi DNS Slave. 

### Setup
Menambahkan `nameserver 192.168.122.1` pada semua client

### Testing
- Mulawarman
![mulawarman](https://github.com/user-attachments/assets/df441e8f-023d-4acf-aee7-c8b138740cee)
- Samaratungga
![samaratungga](https://github.com/user-attachments/assets/afc7b301-cfc4-453d-897d-c40397b180cf)
- Balaraja
![balaraja](https://github.com/user-attachments/assets/3fa63415-26ce-4606-ba1f-f99f5e008752)
- Alexandervolta
![alexandervolta](https://github.com/user-attachments/assets/85db5996-1f4b-4e7e-b613-399d198f7b75)


## No. 2
Karena para pasukan membutuhkan koordinasi untuk melancarkan serangannya, maka buatlah sebuah domain yang mengarah ke Solok dengan alamat sudarsana.xxxx.com dengan alias www.sudarsana.xxxx.com, dimana xxxx merupakan kode kelompok. Contoh: sudarsana.it01.com.

### Sriwijaya
Isi dari file kami `123.sh`:

```
apt update
apt install bind9 -y

echo 'zone "sudarsana.it28.com" {
	type master;
	file "/etc/bind/it28/sudarsana.it28.com";
};' > /etc/bind/named.conf.local

mkdir /etc/bind/it28

cp /etc/bind/db.local /etc/bind/it28/sudarsana.it28.com

echo '
;
; BIND data file for local loopback interface
;
$TTL    604800
@       IN      SOA     sudarsana.it28.com. root.sudarsana.it28.com. (
                        2024100104      ; Serial
                         604800         ; Refresh
                          86400         ; Retry
                        2419200         ; Expire
                         604800 )       ; Negative Cache TTL
;
@       IN      NS      sudarsana.it28.com.
@       IN      A       192.247.1.3     ; IP Solok
www     IN      CNAME   sudarsana.it28.com.' > /etc/bind/it28/sudarsana.it28.com

service bind9 restart
```




## No. 3
Para pasukan juga perlu mengetahui mana titik yang akan diserang, sehingga dibutuhkan domain lain yaitu pasopati.xxxx.com dengan alias www.pasopati.xxxx.com yang mengarah ke Kotalingga.

### Sriwijaya
Isi dari file kami `321.sh`:

```
apt update
apt install bind9 -y

echo 'zone "pasopati.it28.com" {
	type master;
	file "/etc/bind/it28/pasopati.it28.com";
};' > /etc/bind/named.conf.local

mkdir /etc/bind/it28

cp /etc/bind/db.local /etc/bind/it28/pasopati.it28.com

echo '
;
; BIND data file for local loopback interface
;
$TTL    604800
@       IN      SOA     pasopati.it28.com. root.pasopati.it28.com. (
                        2024100104      ; Serial
                         604800         ; Refresh
                          86400         ; Retry
                        2419200         ; Expire
                         604800 )       ; Negative Cache TTL
;
@       IN      NS      pasopati.it28.com.
@       IN      A       192.247.3.6     ; IP Kotalingga
www     IN      CNAME   pasopati.it28.com.' > /etc/bind/it28/pasopati.it28.com

service bind9 restart
```


## No. 4
Markas pusat meminta dibuatnya domain khusus untuk menaruh informasi persenjataan dan suplai yang tersebar. Informasi dan suplai meme terbaru tersebut mengarah ke Tanjungkulai dan domain yang ingin digunakan adalah rujapala.xxxx.com dengan alias www.rujapala.xxxx.com.

### Sriwijaya
Isi dari file kami `456.sh`:

```
apt update
apt install bind9 -y

echo 'zone "rujapala.it28.com" {
	type master;
	file "/etc/bind/it28/rujapala.it28.com";
};' > /etc/bind/named.conf.local

mkdir /etc/bind/it28

cp /etc/bind/db.local /etc/bind/it28/rujapala.it28.com

echo '
;
; BIND data file for local loopback interface
;
$TTL    604800
@       IN      SOA     rujapala.it28.com. root.rujapala.it28.com. (
                        2024100104      ; Serial
                         604800         ; Refresh
                          86400         ; Retry
                        2419200         ; Expire
                         604800 )       ; Negative Cache TTL
;
@       IN      NS      rujapala.it28.com.
@       IN      A       192.247.2.3     ; IP Tanjungkulai
www     IN      CNAME   rujapala.it28.com.' > /etc/bind/it28/rujapala.it28.com

service bind9 restart
```


## No. 5
Pastikan domain-domain tersebut dapat diakses oleh seluruh komputer (client) yang berada di Nusantara.
![WhatsApp Image 2024-10-04 at 02 05 09](https://github.com/user-attachments/assets/bd0ffb76-341a-4dfc-8631-0cbe081a1a42)
![WhatsApp Image 2024-10-04 at 02 06 27](https://github.com/user-attachments/assets/220dbce3-0704-4cc7-82d2-827c01ea24a9)
![WhatsApp Image 2024-10-04 at 02 07 05](https://github.com/user-attachments/assets/be417677-8c17-45a7-a62b-d37fc9b817ba)
![WhatsApp Image 2024-10-04 at 02 08 23](https://github.com/user-attachments/assets/20abb06d-e7c6-4153-9cb2-79be60036d2d)



