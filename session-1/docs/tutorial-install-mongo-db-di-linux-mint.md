# Tutorial Install MongoDB di Linux Mint
## Step 1: Update Sistem Terlebih Dahulu
Ketik:
```
sudo apt update
```
*Install* juga ` gnupg ` dan ` curl `   yang akan dibutuhkan untuk menambahkan *repository*.
```
sudo apt install gnupg curl -y
```
## Step 2: Download MongoDB dan Tambahkan MongoDB GPG Key
MongoDB menggunakan GPG key untuk memastikan paket yang kita unduh itu asli dan aman. Ketik:
```
    curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
    sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
    --dearmor
```
*Command* di atas akan mengunduh GPG key dan menyimpannya di *directory keyrings*.
## Step 3: Tambahkan MongoDB Repository
Ketik:
```
    echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.0.list
```
Command di atas akan menambahkan baris baru ke file `source.list` yang mengarahkan sistem ke repository MongoDB versi 8.0
## Step 4: Instalasi MongoDB
Sekarang, kita bisa mulai instalasinya. Pertama, update lagi daftar *package* detelah menambahkan *repository* baru.
```
sudo apt update
```
Kemudian, jalankan *command* instalasi berikut:
```
    sudo apt install mongodb-org -y
```
*Command* tersebut akan meng-*install* semua *package* yang dibutuhkan untuk MongoDB, termasuk server dan *shell*nya. 
## Step 5: Kelola Layanan MongoDB
MongoDB tidak langsung aktif setelah di-install. Kita perlu mengaktifkan dan menjalankannya secara manusal.
* Mulai layanan MongoDB:
  ```
  sudo systemctl start mongod
  ```
* Pastikan layanan berjalan dengan baik:
  ```
  sudo systemctl status mongod
  ```
  Jika hasilnya menunjukkan **active (running)**,berarti sudah berhasil.
  
* Aktifkan MongoDB agar berjalan otomatis saat startup:
  ```
  sudo systemctl enable mongod
  ```
Selesai. MongoDB sudah terpasang dan siap digunakan.
