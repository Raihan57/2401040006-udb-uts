# UTS Praktikum Infrastruktur Jaringan

## Nama & NIM Mahasiswa

* **Nama** : (Muhammad Raihan Hibatullah)
* **NIM**  : 240104006

---

## Administrator Port

* **Adminer Port** : **8006**

---

## IP ZeroTier

* **IP ZeroTier** : (172.22.38.90)

---

## Struktur Project

```
240104006-udb-uts/
├── docker-compose.yml
└── README.md
```

---

## Konfigurasi Layanan

### MySQL (Internal)

* **Container Name** : uts_mysql
* **Database**       : uts_mysql_db
* **Username**       : uts_user
* **Password**       : uts_password
* **IP Address**     : 172.30.6.10
* **Port**           : 3306

### PostgreSQL (Internal)

* **Container Name** : uts_postgres
* **Database**       : uts_postgres_db
* **Username**       : uts_user
* **Password**       : uts_password
* **IP Address**     : 172.30.6.20
* **Port**           : 5432

### Adminer

* **Container Name** : uts_adminer
* **IP Address**     : 172.30.6.30
* **Port Host**      : 8006

---

## Cara Menjalankan Proyek

1. Masuk ke direktori project

```bash
cd 240104006-udb-uts
```

2. Jalankan container Docker

```bash
docker-compose up -d
```

3. Pastikan semua container berjalan

```bash
docker ps
```

4. Akses Adminer melalui browser

```
http://IP_ZEROTIER:8006
```

---

## Cara Login Adminer

### Login MySQL

* **System**   : MySQL
* **Server**   : uts_mysql
* **Username** : uts_user
* **Password** : uts_password
* **Database** : uts_mysql_db

### Login PostgreSQL

* **System**   : PostgreSQL
* **Server**   : uts_postgres
* **Username** : uts_user
* **Password** : uts_password
* **Database** : uts_postgres_db

---

## Dokumentasi Wajib

Lampiran tangkapan layar berikut:

1. Output perintah `docker ps`
2. Adminer diakses melalui IP ZeroTier
3. Login Adminer ke MySQL
4. Login Adminer ke PostgreSQL

---

## Catatan

* Seluruh service berjalan dalam **1 custom Docker bridge network**
* Database **tidak diekspos ke publik**, hanya dapat diakses melalui Adminer
* Adminer hanya dapat diakses melalui jaringan **ZeroTier**

---

## Sanksi

Pelanggaran terhadap ketentuan UTS akan dikenakan sanksi sesuai peraturan praktikum.
