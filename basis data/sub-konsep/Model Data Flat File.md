Adalah cara yang paling dasar dalam menyimpan sebuah data, seperti kita biasanya menyimpan data pada notepad atau tabel spreadsheet sederhana. Data yang disimpan diatur dalam bentuk baris (*record*) dan kolom (*field*).

![[Pasted image 20250814074919.png]]

Berdasarkan *field*-nya, penerapan model ini terbagi menjadi dua, yaitu:
1. *Field* dengan panjang tetap.
	![[Pasted image 20250814074943.png]]
2. *Field* dengan panjang bervariasi.
	![[Pasted image 20250814075019.png]]

Ada beberapa keterbatasan penggunaan model flat file ini, diantaranya:
- Struktur data yang kompleks tidak akan mudah direalisasikan. Jika kita mempunyai dua buah file yang ingin dihubungkan, hal itu tidak bisa dilakukan dengan model ini.
- Datanya sulit diatur, karena penyimpanannya berbasis file dan tidak terpusat, sulit mengelola datanya untuk dikelola oleh banyak pengguna.
- Keakuratan data tidak terjamin, karena [[Redundansi Data|redundansi]] yang tinggi, mengakibatkan data menjadi tidak konsisten.
- Karena berbentuk file, lokasi file tersebut di dalam komputer harus diketahui. Apabila lokasi yang disebutkan salah atau filenya berpindah, maka pembacaan data akan gagal.
- Sulit melakukan pemeliharaan atau pengembangan berkelanjutan, karena jika mengubah struktur data, berarti mengubah kode program agar bisa membaca ulang struktur tersebut.