Yaitu bahasa yang digunakan untuk mengelola transaksi di dalam sebuah basis data. Transaksi yang dimaksud adalah satu unit pekerjaan yang terdiri dari satu atau lebih perintah DML. TCL ini digunakan untuk memastikan bahwa sekelompok perubahan ini diperlakukan sebagai satu kesatuan yang utuh. Hal ini sangat penting untuk menjaga integritas dan konsistensi data. TCL ini memberikan kontrol untuk memutuskan kapan perubahan data harus disimpan permanen atau dibatalkan. Contohnya yaitu:
1. `COMMIT`, perintah ini digunakan untuk menyimpan semua hasil perubahan yang sebelumnya telah dilakukan ke dalam sebuah transaksi secara permanen ke dalam basis data. Setelah perintah `COMMIT` dijalankan, perubahan tersebut tidak dapat dibatalkan lagi menggunakan perintah `ROLLBACK`.
```mysql
UPDATE mahasiswa SET nama = 'Muhamad' WHERE nim = '12345'
UPDATE mahasiswa SET nama = 'Kemal' WHERE nim = '67890'
COMMIT;
```

2. `ROLLBACK`, perintah ini digunakan untuk membatalkan semua perubahan yang telah dibuat sejak `COMMIT` terakhir, dan mengembalikan basis data ke kondisi `COMMIT` tersebut. Perintah ini biasanya digunakan saat terjadi kesalahan di tengah transaksi atau jika pengguna memutuskan untuk membatalkan seluruh operasi.
```mysql
UPDATE mahasiswa SET nama = 'Muhamad' WHERE nim = '12345'
/* Misalkan terjadi error di sekitar sini */
ROLLBACK;
```

3. `SAVEPOINT`, perintah ini digunakan untuk mengidentifikasi atau menandai suatu titik tertentu di dalam sebuah transaksi yang panjang. Hal ini memungkinkan kita untuk melakukan `ROLLBACK` hanya sampai ke titik tersebut, tanpa harus kembali ke `COMMIT` terakhir.
```mysql
UPDATE mahasiswa SET nama = 'Muhamad' WHERE nim = '12345'
SAVEPOINT A;

UPDATE mahasiswa SET nama = 'Faza' WHERE nim = '67890'
ROLLBACK TO SAVEPOINT A;
```

4. `SET TRANSACTION`, perintah ini digunakan untuk mengganti atau mengatur opsi untuk transaksi yang sedang berjalan. Contohnya adalah mengatur tingkat isolasi suatu transaksi atau membuatnya menjadi *read-only*.
```mysql
SET TRANSACTION READ ONLY
```