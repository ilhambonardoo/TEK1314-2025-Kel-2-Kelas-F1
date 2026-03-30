# Baseline Report (Fase 1: Hardening Review)

## 1. Identitas Sistem
* **Nama Kelompok**: Kelompok 2
* **Hostname Server Target**: SRV-WEB-KEL02F
* **IP Address Server**: 
* **IP Address Attacker/Client**: 

## 2. Topologi Jaringan
![Topologi Jaringan](./assets/topologi.png)
*(Penjelasan singkat: Server terhubung dengan Security Onion untuk monitoring traffic jaringan...)*

## 3. System Hardening
Kami telah melakukan penguatan pada sistem operasi dengan langkah berikut:
1. **Penonaktifan Layanan**: Mematikan layanan [sebutkan layanan, misal: telnet/ftp] yang tidak diperlukan.
2. **Manajemen User**: Menonaktifkan login root langsung dan membuat user non-root bernama `[nama user]`.
3. **Security Patch**: Melakukan update OS ke versi patch terbaru.

## 4. Network Hardening (Firewall)
Kami menggunakan UFW (Uncomplicated Firewall) dengan konfigurasi Default Deny untuk incoming traffic.
![Bukti Konfigurasi UFW](./assets/ufw-rules.png)

## 5. Verifikasi Logging (Minggu ke-5)
Berikut adalah bukti bahwa Security Onion telah terinstal dan aktif merekam aktivitas jaringan.
![Sguil Dashboard - ICMP Record](./assets/security-onion-ping.png)
* **Keterangan**: Gambar di atas menunjukkan *log* aktivitas ICMP (Ping) dari IP Attacker (`[IP Attacker]`) menuju IP Target (`[IP Target]`) beserta *timestamp*-nya.
