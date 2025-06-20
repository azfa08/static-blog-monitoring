# 📘 Static Blog Monitoring

Proyek blog statis yang dideploy otomatis ke server dengan pipeline CI/CD, serta memiliki monitoring disk usage container dan notifikasi alert ke Discord.

## 🚀 Teknologi yang Digunakan
- **Static Site Generator:** Hugo / Jekyll
- **CI/CD:** Jenkins + Docker
- **Deployment:** Kubernetes
- **Monitoring:** Prometheus, Node Exporter, Alertmanager
- **Notification:** Discord Webhook

## 🔁 Alur Kerja CI/CD
1. Artikel dipush ke repo
2. Jenkins otomatis build blog statis
3. Docker image dibuat dan dipush
4. Image dideploy ke Kubernetes
5. Prometheus memantau disk usage
6. Jika melebihi threshold → Alert ke Discord

## 📂 Struktur Folder 
```
static-blog-monitoring/
├── blog-template/          # Artikel & tema blog Hugo
├── ansible/                # Konfigurasi Ansible
├── Jenkinsfile             # CI/CD pipeline Jenkins
├── Dockerfile              # Image Docker untuk blog
├── k8s/                    # File deployment Kubernetes
├── monitoring/             # Prometheus & Alertmanager config
├── README.md
└── CONTRIBUTING.md
```
