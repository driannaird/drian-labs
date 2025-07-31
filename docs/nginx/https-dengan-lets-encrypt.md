---
sidebar_position: 2
---

# Konfigurasi HTTPS di Nginx menggunakan Let's Encrypt (Certbot)

Panduan ini akan membantu Anda mengamankan website Anda dengan HTTPS secara **gratis** menggunakan **Let's Encrypt** dan **Certbot** di server Nginx.

---

## Prasyarat

Pastikan Anda sudah memiliki:

- Server dengan akses root (misalnya VPS).
- Nama domain yang sudah mengarah ke IP server (gunakan DNS A record).
- Aplikasi Nginx sudah terinstall dan berjalan.

---

## 1. Install Certbot dan Plugin Nginx

Untuk Ubuntu/Debian:

```bash
sudo apt update
sudo apt install certbot python3-certbot-nginx
```

## 2. Pastikan Domain Aktif dan Arah ke Server

Gunakan perintah berikut untuk mengecek apakah domain mengarah ke server:

```bash
ping your-domain.com
Jika IP yang muncul adalah IP server Anda, berarti domain sudah siap.
```

## 3. Jalankan Certbot untuk Nginx

Gunakan perintah berikut untuk mengatur HTTPS secara otomatis:

```bash
sudo certbot --nginx -d your-domain.com -d www.your-domain.com
```

Saat diminta:

- Pilih apakah ingin redirect semua HTTP ke HTTPS (opsi ini direkomendasikan).
- Certbot akan mengedit file konfigurasi Nginx Anda dan menambahkan blok SSL secara otomatis.

## 4. Verifikasi HTTPS Aktif

Akses domain Anda di browser dengan https://your-domain.com. Pastikan:

- Tidak ada peringatan SSL.
- Ikon gembok muncul di address bar.

## 5. Perpanjangan Otomatis

Let's Encrypt hanya berlaku selama 90 hari, tapi Certbot akan mengatur perpanjangan otomatis.

Periksa statusnya:

```bash
sudo systemctl status certbot.timer
```

Coba uji perpanjangan manual:

```bash
sudo certbot renew --dry-run
```

Jika tidak ada error, artinya sistem perpanjangan otomatis bekerja dengan baik.

---

## Troubleshooting Umum

| Masalah                   | Solusi                                                 |
| ------------------------- | ------------------------------------------------------ |
| Port 80/443 diblok        | Jalankan: `sudo ufw allow 'Nginx Full'`                |
| Domain belum aktif        | Pastikan DNS sudah benar dan propagasi selesai         |
| Certbot gagal memperbarui | Pastikan file konfigurasi Nginx valid: `sudo nginx -t` |

---

## Optional: Hapus SSL

Jika Anda ingin menghapus HTTPS:

#### 1. Nonaktifkan sertifikat:

```bash
sudo certbot delete
```

#### 2. Edit file Nginx untuk menghapus blok `listen 443` dan `ssl_*`.

#### 3. Reload Nginx:

```bash
sudo systemctl reload nginx
```

---

## Selesai!

Website Anda sekarang sudah **aman dengan HTTPS** gratis dari Let’s Encrypt menggunakan Nginx dan Certbot.
