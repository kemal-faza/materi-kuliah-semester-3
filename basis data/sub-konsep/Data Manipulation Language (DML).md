Yaitu bahasa yang digunakan untuk mengelola data yang ada di dalam objek skema. DML ini digunakan untuk bekerja dengan data yang ada di dalam tabel, bisa memasukkan, mengambil, mengubah, atau menghapus data di dalam tabel tersebut. Contohnya yaitu:
1. `SELECT`, perintah ini digunakan untuk mengambil data dari sebuah tabel, kita bisa mengambil secara general atau spesifik.
```mysql
/* mengambil semua data dari tabel mahasiswa */
SELECT * FROM mahasiswa;

/* mengambil data dari kolom nama dan nim dari tabel mahasiswa */
SELECT nama, nim FROM mahasiswa; 
```

2. `INSERT`, perintah ini digunakan untuk memasukkan data baru dalam bentuk baris (*record*) ke dalam tabel.
```mysql
INSERT INTO mahasiswa (nama, nim, jurusan)
VALUES ('Kemal', '12345', 'Informatika');
```

3. `UPDATE`, perintah ini digunakan untuk memperbarui atau mengubah data yang sudah ada di dalam tabel. Biasanya perintah ini akan dibarengi dengan klausa `WHERE` agar perubahan datanya spesifik, jika tidak, semua data akan berubah.
```mysql
UPDATE mahasiswa
SET jurusan = 'Teknik Komputer'
WHERE nim = '12345';
```

4. `DELETE`, perintah ini digunakan untuk menghapus satu atau beberapa baris (*record*) sekaligus. Sama seperti `UPDATE`, perintah ini juga dianjurkan dibarengi dengan klausa `WHERE`. Karena kalau tidak, semua data akan terhapus.
```mysql
DELETE FROM mahasiswa
WHERE nim = '12345';
```

5. `MERGE`, perintah ini memungkinkan menjalankan perintah `INSERT`, `UPDATE`, dan `DELETE` sekaligus. Perintah ini berfungsi untuk menyinkronkan data antara 2 tabel.
```mysql
/* tabel mahasiswa sebagai target perubahan */
MERGE INTO mahasiswa AS target

/* tabel update_mahasiswa sebagai sumber baru untuk datanya */
USING update_mahasiswa AS source

/* perubahan tergantung kesamaan nim */
ON target.nim = source.nim

/* ketika nimnya sama dan status_lulus-nya bernilai 'Lulus', hapus data di tabel target */
WHEN MATCHED AND source.status_lulus = 'Lulus' THEN
	DELETE

/* ketika hanya nimnya yang sama, update data di tabel target dengan data di tabel source */
WHEN MATCHED THEN
	UPDATE SET
		target.nama = source.nama
		target.jurusan = source.jurusan
		target.status_lulus = source.status_lulus

/* ketika tidak ada nim yang sama di tabel target, masukkan data baru */
WHEN NOT MATCHED BY target THEN
	INSERT (nim, nama, jurusan, status_lulus)
	VALUES (source.nim, source.nama, source.jurusan, source.status_lulus);
```

6. `LOCK TABLE`, perintah ini digunakan untuk mengontrol *concurrency* (akses serentak). Dengan mengunci tabel seperti ini, kita bisa melakukan serangkaian operasi penting dengan aman, tanpa khawatir tentang integritas data. Misalnya anda ingin menghitung data tagihan UKT untuk seluruh mahasiswa.
```mysql
LOCK TABLE tagihan_ukt IN EXCLUSIVE MODE
```