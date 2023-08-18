# Repositori Docker Compose Graylog ElasticSearch

Repositori ini menyediakan konfigurasi Docker Compose untuk mendeploy Graylog bersama dengan Elasticsearch dan MongoDB menggunakan kontainer Docker. Setup ini memungkinkan Anda dengan cepat membuat sistem manajemen log terpusat menggunakan Graylog.

## Persyaratan

Sebelum Anda memulai, pastikan Anda sudah menginstal hal-hal berikut:

- Docker: [Instal Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Instal Docker Compose](https://docs.docker.com/compose/install/)

## Memulai

1. Klon repositori ini ke mesin lokal Anda:

   ```sh
   git clone https://github.com/m34l/Graylog-Elasticsearch-Docker
   cd Graylog-Elasticsearch-Docker

2. Deploy
   ```sh
   docker-compose -f docker-compose.original -up -d
   docker ps

3. Mengakses Antarmuka Web Graylog:

Setelah layanan aktif, Anda dapat mengakses antarmuka web Graylog dengan membuka web browser dan mengunjungi http://localhost:9000/.

Username: admin
Password: admin

4. Mengirimkan Log ke Graylog:

Konfigurasikan aplikasi atau sistem Anda untuk mengirimkan log ke Graylog menggunakan GELF, Syslog, atau protokol dan port yang didukung lainnya.

5. Untuk menghentikan dan menghapus kontainer, jalankan perintah berikut:

   ```sh
   docker-compose down
   
# Catatan
Setup ini mengasumsikan bahwa berkas konfigurasi yang diperlukan ditempatkan dalam direktori config yang sesuai.

Data dan log disimpan di direktori host yang dimount ke dalam kontainer. Pastikan untuk mem-backup data penting.

Ingat untuk mengamankan lingkungan Anda, terutama jika digunakan dalam lingkungan produksi.

# Kontribusi

Kontribusi untuk memperbaiki atau memperluas setup Docker Compose ini sangat diterima! Jangan ragu untuk membuka isu atau permintaan pull
