Overhead data adalah data tambahan yang digunakan oleh [[Sistem Manajemen Basis Data (SMBD) atau Sistem Manajemen Basis Data (SMBD)|SMBD]] untuk keperluan internal, seperti manajemen, kinerja, dan pemulihan sistem. Data ini akan dibuat oleh SMBD itu sendiri dan dikelola olehnya.

Contoh overhead data yaitu:
1. **Indeks**, yaitu struktur tambahan pada data yang digunakan untuk mempercepat pencarian data. Anggaplah tiap data memiliki label yang unik agar kita bisa mencari data tersebut dengan mudah dan cepat.
2. **Log Transaksi**, adalah catatan yang berisi setiap perubahan yang terjadi pada basis data (menggunakan [[Data Manipulation Language (DML)|DML]]). Hal ini diperlukan untuk *recovery* atau `ROLLBACK`
3. **System Management Information**, yang melacak blok mana yang sudah terisi dan mana yang masih kosong, hal ini membantu SMBD dalam menempatkan data baru.
4. **Statistik Kinerja**, seperti statistik tentang data (seperti berapa banyak nilai unik pada suatu kolom) untuk membantu *query optimizer*.