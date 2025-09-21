# Tutorial Mengintegrasikan VS Code dengan GitHub
## Step 1: Install VS Code Terlebih Dahulu
### Update Sistem 
```
sudo apt update
```
### Install Paket Prasyarat
```
sudo apt install software-properties-common apt-transport-https wget -y

```
### Unduh dan Tambahkan Kunci GPG Microsoft
```
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -

```
### Tambahkan Repository VS Code
```
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
```
### Perbarui indeks paket lagi setelah menambahkan repositori baru:
```
sudo apt update
```
### Install VS Code
```
sudo apt install code
```
Setelah instalasi selesai, kamu bisa meluncurkan VS Code dari menu aplikasi.

## Step 2: Meng-install Git
```
sudo apt-get install git
```
### Pastikan Git Sudah Ter-Install
```
git --version
```
Jika Git sudah terinstal dengan benar, akan muncul informasi versi Git yang terpasang di komputer kamu.
## Step 3: Konfigurasi Git Awal
Sebelum mulai, beri tahu Git siapa kamu. Hal ini cuma perlu dilakukan sekali saja.
Buka Terminal/Git Bash, lalu ketik perintah berikut, ganti Nama Kamu dan emailmu@example.com dengan nama dan email GitHub-mu.
```
git config --global user.name "Nama Kamu"
git config --global user.email "emailmu@example.com"
```
## Step 3: Mengambil Proyek dari GitHub
* Buka GitHub: Pergi ke halaman repositori yang sudah kamu buat.
* Salin URL: Klik tombol hijau < > Code, lalu salin URL HTTPS-nya.
* Buka Terminal/Git Bash: Buka terminal di folder tempat kamu ingin menyimpan proyek.
* Jalankan Perintah clone: Ketik git clone diikuti dengan URL yang sudah kamu salin tadi.
```
git clone https://github.com/nama-kamu/nama-proyek.git
```
## Step 4: Buka Proyek di VS Code dan Mulai Mengerjakan
Setelah proyek di-clone, kita bisa mulai mengerjakan tugas dokumentasi di VS Code.
 * Buka VS Code.
 * Pilih File > Open Folder... dan navigasi ke folder proyek yang baru saja di-clone.
 * Di dalam VS Code, buat file-file dokumentasinya (misalnya, README.md) dan mulai tulis isinya.
   
Kita bisa menulis kode, dokumentasi, dan nanti mengunggahnya ke GitHub, semuanya bisa dilakukan dari dalam VS Code.

