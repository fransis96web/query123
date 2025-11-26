- **Masuk ke MySQL**
```sql
mysql -u root
``` 

- **Melihat daftar database**
```sql
show databases;
```
- **Membuat database**
```sql
create database phpdasar;
```  
- **Masuk kedalam database** (*Menggunakan database*)
```sql
use phpdasar;
```
- **Membuat table dengan nama mahasiswa**
```sql  
create table mahasiswa(
  id int primary key auto_increment,
  nama varchar(100),
  nrp char(9),
  email varchar(100),
  jurusan varchar(100),
  gambar varchar(100)
);
```

- **Melihat tabel-tabel di database phpdasar**
```sql
show tables;
```

- **Melihat deskripsi tabel**
```sql
describe mahasiswa;
```

- **Menambahkan data kedalam tabel (CERATE)**
```sql
insert into mahasiswa values (
  '', 'Fransis', '215410072', 'fransis@example.info','Informatika','frans.jpg'
);
``` 

- **Melihat isi tabel**
```sql
select * from mahasiswa;
```

- **Menampilkan data dari field nama**
```sql
select nama from mahasiswa;
```

- **Melihat data pada field tertentu (Misalnya NIM / nrp)**
```sql
select nrp from mahasiswa;
```

```sql
select nrp,nama from mahasiswa;
```

```sql
select nrp,nama,jurusan from mahasiswa;
```
- **READ**
```sql
select nama,gambar from mahasiswa;
```

- **Menambah 1 record pada tabel mahasiswa (CREATE)**
```sql
insert into mahasiswa values(
  '','Agnes','215410000','agnes@hotmail.com','Teknik Komputer','Agnes.jpg'
);
```

- **Menampilkan data dari field tertentu  (READ)**
```sql
select nama from mahasiswa;
```
- **READ**
```sql
select nrp,nama,jurusan from mahasiswa;
```

- **Mencari data berdasarkan nrp / nim (READ - SEARCHING)**
```sql
select * from mahasiswa where nrp='215410072';
```

- **Menampilkan isi tabel**
```sql
select * from mahasiswa;
```

- **Melakukan Edit Data / Record berdasarkan primary key "id" (UPDATE)**
```sql
update mahasiswa set jurusan='Informatika' where id = 2;
```

- **Menampilkan isi table (READ)**
```sql
select * from mahasiswa;
```

- **Menghapus 1 Record (atau data) berdasarkan id / primary key**
```sql
delete from mahasiswa where id=1;
```

- **Menampilkan isi table** (e.g., menampilkan isi tabel mahasiswa)
```sql
select * from mahasiswa;
```
- **DELETE**
```sql
delete from mahasiswa where id=1;
```

- **Menghapus table (e.g., menghapus tabel mahasiswa)**
```sql
drop table mahasiswa;
``` 

- **Menghapus database**
```sql
DROP DATABASE phpdasar;
```

- **Menampilkan semua database**
```sql
SHOW DATABASES;
```

- **Hapus 1 Field / Kolom:**
```sql
ALTER TABLE nama_tabel DROP COLUMN nama_kolom;
```  

---
### LAINNYA   


**Tambah rule `Admin`**  
```query
ALTER TABLE users MODIFY level ENUM('admin', 'petugas', 'mahasiswa') NOT NULL;
```


```sql
create database toko;
```
```sql
use toko;
```
```sql
create table if not exists barang (
  id int auto_increment not null primary key,
  nama varchar(40) not null,
  harga int not null default 0,
  stok int not null default 0,
  foto varchar(70) not null default ''
);
```
```sql
insert into barang(nama,harga,stok, foto) values
  ('Sepatu Adidas 1',500000,5,'sepatu1.jpg'),
  ('Sepatu Adidas 2',600000,5,'sepatu2.jpg'),
  ('Sepatu Converse 1',450000,6,'sepatu3.jpg'),
  ('Sepatu Converse 2',550000,6,'sepatu4.jpg'),
  ('Sepatu Sneakers 1',560000,7,'sepatu5.jpg'),
  ('Sepatu Sneakers 2',660000,7,'sepatu6.jpg'),
  ('Sepatu Sneakers 3',760000,4,'sepatu7.jpg');
```
