#latihan1 Penggunaan Dasar Database MySql | Data Definition Language (DDL) Menggunakan CMD
Penggunaan Dasar Database MySql | Data Definition Language (DDL) Menggunakan CMD

-- 1.	Buat sebuah database dengan nama latihan01!
-- 2.	Buat sebuah tabel dengan nama biodata dengan field nama dan alamat pada database latihan01!
-- 3.	Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!
-- 4.	Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
-- 5.	Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!
-- 6.	Ubah kolom id menjadi char(11)!
-- 7.	Ubah nama kolom phone menjadi hp (varchar 20)!
-- 8.	Hapus kolom keterangan dari tabel!
-- 9.	Ganti nama tabel menjadi data_mahasiswa!
-- 10.	Ganti nama field id menjadi nim!
-- 11.	Jadikan nim sebagai primary key!

-- 1. Buat sebuah database dengan nama latihan01!
create database latihan01;

-- 2. Buat sebuah tabel dengan nama biodata dengan field nama dan alamat pada database latihan01!
use latihan01;
create table biodata
( nama varchar (15) not null,
alamat varchar (20) not null );

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 3. Tambahkan sebuah kolom keterangan (varchar 15), sebagai kolom terakhir!
alter table biodata
add keterangan varchar (15) not null;

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 4. Tambahkan kolom id (int 11) di awal (sebagai kolom pertama)!
alter table biodata
add id int (11) null
first;

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 5. Sisipkan sebuah kolom dengan nama phone (varchar 15) setelah kolom alamat!
alter table biodata
add column
phone varchar (15) not null
after alamat;

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 6. Ubah kolom id menjadi char(11)!
alter table biodata
modify id char(11) null; 

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 7. Ubah nama kolom phone menjadi hp (varchar 20)!
alter table biodata
change phone hp varchar (20) not null;

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 8. Hapus kolom keterangan dari tabel!
alter table biodata
drop keterangan;

-- Untuk melihat struktur tabel ketik 
desc biodata;

-- 9. Ganti nama tabel menjadi data_mahasiswa!
rename table biodata to data_mahasiswa;

-- Untuk melihat struktur tabel ketik 
desc data_mahasiswa;

-- 10. Ganti nama field id menjadi nim!
alter table data_mahasiswa
change id nim char (11) null;

-- Untuk melihat struktur tabel ketik 
desc data_mahasiswa;
