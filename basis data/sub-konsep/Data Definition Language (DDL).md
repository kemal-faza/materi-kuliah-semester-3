Yaitu bahasa yang digunakan untuk mendefinisikan atau mengelola struktur (skema) basis data. Perintah ini akan memanipulasi metadata dari basis data tersebut. Contohnya yaitu:
1. `CREATE`, perintah ini digunakan untuk membuat objek baru di dalam basis data. Objek ini bisa berupa tabel, view, index, dan lain-lain. Misalkan ingin membuat sebuah tabel untuk menyimpan data mahasiswa, kita perlu mendefinisikan nama table dan kolom-kolom di dalamnya.
```mysql
CREATE TABLE mahasiswa (
	nim VARCHAR(10)
	nama VARCHAR(50)
	jurusan VARCHAR(30)
);
```

2. `ALTER`, perintah ini digunakan untuk memanipulasi struktur dari objek yang sudah ada. Perintah ini bisa digunakan untuk menambah, mengubah, dan menghapus kolom dari sebuah tabel. Misalnya setelah membuat tabel `mahasiswa`, kita lupa menambahkan kolom tanggal lahir.
```mysql
ALTER TABLE mahasiswa
ADD status_lulus VARCHAR(10);
```

3. `DROP`, perintah ini digunakan untuk menghapus objek dari basis data secara permanen. Tindakan ini sulit dibatalkan, karena tidak hanya menghapus data, tapi juga seluruh struktur objeknya. Misalnya kita ingin menghapus tabel `mahasiswa_lama` yang sudah tidak terpakai lagi.
```mysql
DROP TABLE mahasiswa_lama;
```

4. `TRUNCATE`, perintah ini digunakan untuk menghapus semua *record* (baris data) dari suatu tabel. Berbeda dengan `DROP` yang menghapus tabel-nya, `TRUNCATE` hanya menghapus isi tabel-nya saja. Misalkan kita ingin menghapus data jadwal ujian sementara tahun lalu untuk diisi dengan jadwal baru.
```mysql
TRUNCATE TABLE jadwal_ujian_sementara;
```

5. `COMMENT`, perintah ini digunakan untuk menambahkan komentar atau catatan ke *data dictionary*. Tujuan ditambahkannya komentar ini sebagai dokumentasi, agar *developer* lain atau kita di masa depan bisa mengerti tujuan dari objek tersebut dibuat. Misalkan kita ingin menambahkan komentar pada tabel `mahasiswa`.
```mysql
COMMENT ON TABLE mahasiswa IS 'Tabel ini digunakan untuk menyimpan data semua mahasiswa.';
```

6. `RENAME`, perintah ini digunakan untuk mengganti nama dari suatu objek. Misalkan kita ingin mengganti nama tabel `mahasiswa` menjadi `mhs`.
```mysql
RENAME mahasiswa TO mhs;
```