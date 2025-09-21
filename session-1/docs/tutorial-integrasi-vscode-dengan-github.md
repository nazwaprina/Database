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
