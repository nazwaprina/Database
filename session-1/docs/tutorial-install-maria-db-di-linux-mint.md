# Tutorial Install MariaDB di Linux Mint 
## Step 1: Update Sistem Terlebih Dahulu
Kita harus memastikan bahwa sistem Linux yang kita gunakan sudah yang terbaru. Buka terminal, ketik:

```
sudo apt update
``` 

```
sudo apt update -y
```

Command di atas akan mengecek dan upgrade semua package di sistem.Tunggu sebentar sampai prosesnya selesai.
## Step 2: Mulai Install MariaDB
Ketik di terminal:

``` 
sudo apt install mariadb-server mariadb-client -y
```

Tunggu sampai prosesnya selesai, dan MariaDB sudah ter-install.
## Step 3: Amankan Instalasi MariaDB
MariaDB yang baru di-install butuh sedikit pengamanan tambahan agar database tidak mudah diakses oleh orang lain. Ketik:
```
sudo mysql_secure_installation
```
Setelah command di atas dijalankan, akan muncul beberapa pertanyaan. Ikuti panduan berikut:
* Enter current password for root (enter for none): Tekan Enter.
 * Switch to unix_socket authentication? [Y/n]: Pilih n.
 * Set root password? [Y/n]: Pilih Y buat bikin password baru.
 * Remove anonymous users? [Y/n]: Pilih Y.
 * Disallow root login remotely? [Y/n]: Pilih Y.
 * Remove test database and access to it? [Y/n]: Pilih Y.
 * Reload privilege tables now? [Y/n]: Pilih Y.
## Step 4: Cek Status MariaDB
Ketik:
```
sudo apt systemctl status mariadb
```
Jika hasilnya menunjukkan active (running), itu artinya MariaDB sudah ter-install dan siap digunakan.

