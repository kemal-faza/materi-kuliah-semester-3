Yaitu bahasa yang digunakan untuk mengontrol hak akses ke basis data. DCL ini menentukan siapa dan tindakan apa saja yang boleh dilakukan saat mengakses data tersebut. Biasanya perintah ini dijalankan oleh DBA (*Database Administrator*) karena itu tugasnya sebagai pengelola keamanan dan kewenangan pengguna. Contohnya yaitu:
1. `GRANT`, perintah ini digunakan untuk memberikan hak istimewa (*privileges*) kepada pengguna tertentu agar mereka bisa mengakses atau melakukan operasi tertentu pada objek basis data. Hak aksesnya itu tergantung perintah DML apa saja yang kita perbolehkan untuk pengguna tersebut.
```mysql
GRANT SELECT ON mahasiswa TO dosen1
```

2. `REVOKE`, perintah ini berkebalikan dengan `GRANT`, yang mana fungsinya untuk mencabut hak akses yang sebelumnya telah diberikan kepada pengguna. Hal ini diperlukan dalam segi keamanan apabila pengguna tersebut sudah tidak memerlukan akses ke tabel tersebut.
```mysql
REVOKE SELECT ON mahasiswa TO dosen1
```