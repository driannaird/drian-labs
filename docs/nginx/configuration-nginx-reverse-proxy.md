---
sidebar_position: 1
---

# Konfigurasi Nginx sebagai Reverse Proxy

Panduan ini akan membantu Anda mengatur Nginx sebagai reverse proxy untuk aplikasi web (misalnya Next.js, Express, dsb) yang berjalan di Docker atau langsung di server dengan port tertentu.

---

## 1. Buat File Konfigurasi Nginx

Buat file baru di direktori konfigurasi Nginx (`/etc/nginx/sites-available`):

```bash
sudo nano /etc/nginx/sites-available/your-domain.com
```

Ganti `your-domain.com` dengan domain Anda (misalnya `example.com`).

## 2. Tambahkan Konfigurasi Reverse Proxy

Contoh konfigurasi dasar:

```bash
server {
    listen 80;
    server_name your-domain.com www.your-domain.com;

    location / {
        proxy_pass http://localhost:PORT;
        proxy_http_version 1.1;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

Keterangan:

- Ganti `PORT` dengan port aplikasi utama (misalnya Next.js: `4000`).
- Anda bisa menambahkan lebih banyak location sesuai kebutuhan.

## 3. Aktifkan Konfigurasi

Aktifkan konfigurasi dengan membuat symbolic link ke `sites-enabled`:

```bash
sudo ln -s /etc/nginx/sites-available/your-domain.com /etc/nginx/sites-enabled/
```

## 4. Cek Konfigurasi

Periksa apakah konfigurasi valid:

```bash
sudo nginx -t
```

Jika hasilnya `syntax is ok` dan `test is successful`, lanjutkan.

## 5. Reload Nginx

Reload Nginx agar perubahan diterapkan:

```bash
sudo systemctl reload nginx
```

🚀 Selesai!
Nginx sekarang berfungsi sebagai reverse proxy yang meneruskan permintaan dari domain Anda ke aplikasi yang berjalan di server (langsung atau via Docker).
