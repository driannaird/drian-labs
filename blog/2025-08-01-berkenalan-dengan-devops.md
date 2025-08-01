---
slug: berkenalan-dengan-devops
title: Berkenalan Dengan Devops
authors:
  - name: Drian
    title: Software Engineer
    url: https://github.com/driannaird
    image_url: https://github.com/driannaird.png
tags: [devops]
---

# Catatan Lengkap DevOps: Rangkuman Mudah Dipahami dan Diingat

## Apa Itu DevOps?

DevOps adalah gabungan dari dua kata: **Development** (pengembangan) dan **Operations** (operasi). Ini bukan sekadar alat atau teknologi, melainkan **budaya kerja dan pendekatan kolaboratif** yang bertujuan untuk mempercepat proses pengembangan perangkat lunak, meningkatkan kualitas, dan mempercepat waktu ke pasar (time to market).

DevOps mendorong otomatisasi dan integrasi berkelanjutan dari seluruh proses, mulai dari perencanaan, pengembangan, pengujian, hingga deployment dan pemantauan aplikasi.

## Tahapan dalam DevOps Pipeline

DevOps pipeline adalah alur kerja otomatis yang menghubungkan seluruh proses pengembangan hingga rilis ke pengguna akhir. Berikut tahapan utamanya:

1. **Plan**
   Merencanakan fitur, perbaikan bug, atau pembaruan berdasarkan kebutuhan pengguna atau bisnis.

2. **Develop**
   Menulis dan mengelola kode menggunakan sistem version control seperti Git.

3. **Build**
   Mengubah source code menjadi bentuk siap digunakan (seperti file binary, container image, atau artifact lainnya).

4. **Test**
   Melakukan pengujian otomatis untuk memastikan tidak ada bug atau error.

5. **Release**
   Menyusun dan mempersiapkan paket rilis agar dapat digunakan tim deployment.

6. **Deploy**
   Mengirimkan aplikasi ke server atau platform produksi agar bisa diakses oleh pengguna.

7. **Operate and Monitor**
   Memantau performa aplikasi setelah digunakan oleh pengguna, serta mengumpulkan log dan metrik untuk evaluasi.

## Apa Itu Build?

Build adalah proses mengonversi source code menjadi format executable atau artifact yang bisa dijalankan. Misalnya, meng-compile file kode menjadi file `.jar`, `.exe`, atau container image. Proses build biasanya otomatis dan terintegrasi dalam pipeline.

Contoh tool build dari AWS: **AWS CodeBuild**
Tool ini bertugas melakukan compile, testing, dan menghasilkan artifact siap rilis.

## Apa Itu Continuous Integration dan Continuous Delivery (CI/CD)?

**Continuous Integration (CI)** adalah praktik di mana developer secara rutin menggabungkan (merge) kode mereka ke repositori utama. Tujuannya adalah:

- Menghindari konflik kode
- Mendeteksi error lebih cepat
- Memastikan integrasi stabil

**Continuous Delivery (CD)** adalah kelanjutan dari CI, di mana sistem secara otomatis:

- Mengemas kode menjadi artifact
- Menyimpannya
- Menyiapkannya untuk bisa dirilis ke produksi kapan saja

Dalam praktik yang lebih maju, **Continuous Deployment** akan langsung mengirimkan aplikasi ke produksi secara otomatis setelah build dan test berhasil.

## Tiga Prinsip Utama DevOps (The Three Ways)

### 1. The First Way: Alur Kerja yang Efisien

Fokus pada efisiensi alur kerja dari pengembangan hingga ke pengguna. Beberapa hal yang dilakukan:

- Identifikasi bottleneck
- Kurangi proses yang tidak perlu
- Automasi proses build dan deployment
- Gunakan visualisasi seperti Kanban Board

### 2. The Second Way: Umpan Balik Cepat

Menekankan pentingnya feedback dari sistem ke developer secara cepat dan jelas. Contohnya:

- Monitoring real-time
- Alert otomatis
- Review log error dan metrik performa
- Mekanisme rollback jika gagal deploy

### 3. The Third Way: Pembelajaran dan Eksperimen Berkelanjutan

Mendorong budaya pembelajaran, perbaikan, dan eksperimen. Hal ini bisa dilakukan melalui:

- Retrospektif rutin
- Eksperimen kecil pada sistem produksi
- Evaluasi dan peningkatan berkelanjutan

## Framework CALMS

CALMS adalah kerangka untuk menilai kesiapan organisasi dalam mengadopsi DevOps, diperkenalkan oleh Jez Humble.

- **Culture**: Budaya kerja kolaboratif, transparan, dan saling percaya antar tim.
- **Automation**: Automasi proses seperti testing, build, deployment, dan monitoring.
- **Lean**: Pendekatan ramping, menghindari pemborosan waktu dan sumber daya.
- **Measurement**: Pengambilan keputusan berbasis data, semua proses diukur dan dievaluasi.
- **Sharing**: Berbagi informasi, dokumentasi, dan pengetahuan antar tim.

## Tools DevOps yang Umum Digunakan (Terutama di AWS)

| Fungsi               | Tool AWS yang digunakan |
| -------------------- | ----------------------- |
| Repositori Git       | AWS CodeCommit          |
| Build aplikasi       | AWS CodeBuild           |
| Otomatisasi pipeline | AWS CodePipeline        |
| Deployment aplikasi  | AWS CodeDeploy          |
| Fungsi serverless    | AWS Lambda              |
| Pemantauan sistem    | Amazon CloudWatch       |

## Pemantauan dan Monitoring

Monitoring selama pengembangan dan setelah rilis memberikan banyak manfaat, seperti:

- Memberi kepercayaan diri kepada tim untuk melakukan deploy
- Memudahkan deteksi error sejak awal
- Memberikan data objektif untuk perbaikan aplikasi
- Menjadi dasar dalam pengambilan keputusan teknis

Contoh metrik yang biasa dipantau:

- Waktu respons aplikasi
- Penggunaan memori dan CPU
- Frekuensi error
- Jumlah request per detik

## Penutup

DevOps bukan hanya tentang tools, melainkan tentang **budaya kerja dan otomatisasi** yang terintegrasi. Dengan menerapkan prinsip-prinsip DevOps, tim pengembang dan operasi bisa bekerja lebih cepat, lebih andal, dan lebih percaya diri dalam setiap proses pengembangan aplikasi.
