# Aplikasi CRUD Mahasiswa

Aplikasi pengelolaan data mahasiswa menggunakan **Java**, **Hibernate**, dan **JasperReports** yang dibangun melalui **NetBeans** sebagai bagian dari praktikum.

## Fitur

* Create, Read, Update, Delete (CRUD) data mahasiswa
* Koneksi database menggunakan Hibernate ORM
* Pembuatan laporan menggunakan JasperReports
* Export laporan dalam format PDF

## Teknologi

* NetBeans 8.2
* Java JDK 8 (Java SE 8)
* Hibernate ORM 5.x (versi default yang umum digunakan pada NetBeans 8.2)
* JasperReports 6.x (mengikuti library bawaan praktikum)

## Database

Menggunakan **MySQL** (XAMPP) dengan tabel **mahasiswa** berisi kolom:

* `id` (INT, Primary Key, Auto Increment)
* `npm` (VARCHAR)
* `nama` (VARCHAR)
* `jurusan` (VARCHAR)

## Setup

### 1. Membuat Database di MySQL (XAMPP)

1. Buka **phpMyAdmin**.
2. Buat database baru bernama `db_mahasiswa`.
3. Jalankan query berikut:

```sql
CREATE TABLE mahasiswa (
  id INT AUTO_INCREMENT PRIMARY KEY,
  npm VARCHAR(20),
  nama VARCHAR(100),
  jurusan VARCHAR(50)
);
```

### 2. Import Project ke NetBeans 8.2

1. Buka NetBeans.
2. Pilih **File > Open Project**.
3. Arahkan ke folder project praktikum.
4. Klik **Open Project**.

### 3. Konfigurasi Library Hibernate & JasperReports

1. Klik kanan project → **Properties**.
2. Masuk ke **Libraries**.
3. Tambahkan file `.jar` Hibernate dan JasperReports yang disediakan oleh dosen/praktikum.
4. Pastikan Hibernate Configuration (`hibernate.cfg.xml`) berisi koneksi:

```xml
<property name="hibernate.connection.url">jdbc:mysql://localhost:3306/db_mahasiswa</property>
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password"></property>
```

### 4. Menjalankan Aplikasi

1. Klik kanan project → **Run**.
2. Aplikasi siap digunakan untuk CRUD dan generate laporan.

## Author

Farahat (51422033)
