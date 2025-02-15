# Instal Driver Wi-Fi Alfa Awus1900 di Linux

![](https://github.com/fixploit03/INSTAL-DRIVER-WIFI-ALFA-AWUS-1900/blob/main/awus1900.jpg)

1. **Update dan upgrade repositori**  
   Jalankan perintah berikut untuk memperbarui dan meningkatkan sistem:

   ```
   sudo apt update && sudo apt upgrade -y
   ```

2. **Reboot sistem**  
   Setelah update selesai, reboot sistem dengan perintah:

   ```
   reboot
   ```

3. **Instal dependensi yang diperlukan**   
   Instal paket-paket yang dibutuhkan untuk kompilasi driver:

   ```
   sudo apt install -y linux-headers-$(uname -r) build-essential bc dkms git libelf-dev rfkill iw
   ```

4. **Buat direktori untuk menyimpan driver**  
   Buat direktori di dalam folder home untuk menyimpan source driver:

   ```
   mkdir -p ~/src
   ```

5. **Pindah ke direktori tersebut**  
   Navigasi ke folder yang baru dibuat:

   ```
   cd ~/src
   ```

6. **Kloning driver dari GitHub**  
   Unduh source code driver dari GitHub dengan perintah:

   ```
   git clone https://github.com/morrownr/8814au.git
   ```

7. **Masuk ke direktori driver**  
   Pindah ke folder hasil kloning:

   ```
   cd 8814au
   ```

8. **Instal driver**  
   Jalankan skrip instalasi driver dengan perintah berikut:

   ```
   sudo ./install-driver.sh
   ```

Setelah proses instalasi selesai, WiFi Alfa Awus1900 seharusnya sudah bisa digunakan. Jika masih ada masalah, coba reboot sistem atau cek apakah modul driver sudah dimuat dengan perintah:

```
lsmod | grep '8814au'
```

**Semoga bermanfaat!**
