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

### **1. Pengantar DevOps**

DevOps adalah pendekatan dalam pengembangan perangkat lunak yang menyatukan tim **Development** (pengembang) dan **Operations** (operasional) untuk meningkatkan kolaborasi, automasi, dan efisiensi dalam siklus hidup aplikasi—mulai dari pengembangan, pengujian, rilis, hingga pemantauan. Tujuan utamanya adalah menciptakan sistem yang tangguh, stabil, dan mampu beradaptasi dengan cepat terhadap kebutuhan pengguna.

### **2. Tiga Prinsip Utama DevOps**

DevOps dibangun di atas tiga prinsip utama yang disebut sebagai **The Three Ways**:

- **The First Way: Flow**
  Fokus pada alur kerja yang lancar dari Development ke Operations ke Customer. Tujuannya adalah mempercepat proses delivery dari ide menjadi fitur yang bisa digunakan pengguna.

- **The Second Way: Feedback**
  Menekankan pentingnya umpan balik yang cepat dan terus-menerus. Feedback dari customer, sistem, maupun anggota tim digunakan untuk perbaikan berkelanjutan.

- **The Third Way: Continual Learning and Experimentation**
  Mendukung budaya pembelajaran berkelanjutan dan eksperimen. Kegagalan dianggap sebagai peluang belajar, dan inovasi terus didorong.

### **3. CALMS Framework**

CALMS adalah kerangka kerja untuk menilai kesiapan dan implementasi DevOps, yang terdiri dari lima pilar:

- **Culture**: Budaya kolaboratif, tidak menyalahkan.
- **Automation**: Automasi proses untuk efisiensi dan kecepatan.
- **Lean**: Fokus pada peningkatan berkelanjutan dan efisiensi.
- **Measurement**: Pengukuran metrik kinerja seperti waktu deploy dan tingkat bug.
- **Sharing**: Berbagi pengetahuan dan praktik baik antar tim.

CALMS pertama kali diperkenalkan oleh **Damon Edwards** dan **John Willis**.

### **4. DevOps Pipeline**

DevOps Pipeline adalah **serangkaian proses dan tools otomatis** yang menghubungkan developer dan tim operasional untuk memastikan bahwa perubahan kode dapat diuji, dibangun, dan di-deploy secara aman ke lingkungan produksi. Pipeline ini mencakup tahapan seperti:

- **Continuous Integration (CI)**
  Praktik menggabungkan perubahan kode secara berkala ke repositori pusat dan melakukan pengujian otomatis. Hal ini mencegah konflik integrasi yang kompleks.

- **Build**
  Proses mengubah source code dan aset lainnya menjadi artefak (file hasil build) yang siap di-deploy. Contohnya adalah file `.jar`, `.zip`, atau image Docker.

- **Test**
  Tahapan pengujian otomatis (unit, integration, end-to-end) untuk memastikan aplikasi bekerja sesuai ekspektasi.

- **Deploy**
  Tahap di mana artefak aplikasi dikirim ke server production atau staging.

- **Monitor**
  Aplikasi dipantau untuk mendeteksi error atau kejanggalan, sekaligus memberikan feedback kepada tim.

### **5. Tools DevOps Populer**

Berikut beberapa tools yang umum digunakan dalam proses DevOps:

#### **Continuous Integration / Build Tools**

- **Jenkins**: Otomatisasi CI/CD yang populer dan open-source.
- **AWS CodeBuild**: Layanan AWS untuk build otomatis, pengujian, dan produksi artefak.
- **GitHub Actions**: Menjalankan CI/CD workflows langsung dari repositori GitHub.

#### **Version Control**

- **Git**: Sistem kontrol versi terdistribusi.
- **GitHub / GitLab / Bitbucket**: Layanan repositori Git yang mendukung kolaborasi dan integrasi dengan pipeline CI/CD.

#### **Configuration & Deployment**

- **Docker**: Mengemas aplikasi dalam container untuk memastikan konsistensi di berbagai lingkungan.
- **Kubernetes**: Orkestrasi container dalam skala besar.
- **Terraform**: Infrastructure as Code (IaC) untuk provisioning dan manajemen infrastruktur.

#### **Monitoring & Logging**

- **Prometheus + Grafana**: Pemantauan dan visualisasi metrik sistem.
- **ELK Stack (Elasticsearch, Logstash, Kibana)**: Analisis log.
- **AWS CloudWatch**: Monitoring dan alerting dari AWS.

#### **Serverless**

- **AWS Lambda**: Menjalankan fungsi kecil tanpa mengelola server. Kode hanya berjalan saat dipanggil.

### **6. Pentingnya Monitoring**

Monitoring sejak tahap development hingga produksi membantu tim:

- Mendeteksi bug secara dini.
- Meningkatkan kepercayaan diri saat melakukan deploy.
- Mempercepat feedback loop.
- Memberikan wawasan nyata terhadap perilaku aplikasi di lingkungan pengguna.

### **7. Fakta DevOps**

- Pada tahun 2012, **Amazon** berhasil melakukan **lebih dari 1000 deploy per hari**.
- Tim yang mengimplementasikan DevOps secara efektif mampu merilis software lebih cepat, dengan kualitas yang lebih tinggi, dan tingkat kegagalan yang lebih rendah.

### **8. Contoh Pertanyaan Evaluasi DevOps**

Untuk mengukur efektivitas DevOps, berikut beberapa pertanyaan penting (selain aspek finansial individu):

- Seberapa sering terjadi bug?
- Seberapa cepat perubahan kode bisa di-deploy?
- Berapa lama waktu yang dibutuhkan dari commit ke production?
- Berapa banyak rollback yang terjadi?

### **Penutup**

DevOps bukan hanya tentang tools, tetapi juga tentang **budaya kolaboratif, automasi yang efektif, dan feedback yang cepat**. Implementasi DevOps yang tepat akan meningkatkan produktivitas tim, mempercepat delivery produk, dan memberikan pengalaman yang lebih baik bagi pengguna.

Catatan ini bisa kamu gunakan kapan saja jika suatu saat lupa tentang dasar-dasar DevOps dan tools yang sering digunakan dalam proses CI/CD dan monitoring modern.
