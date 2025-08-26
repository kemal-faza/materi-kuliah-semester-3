## Basis Data (*Data Base*)

Basis data merupakan sekumpulan data yang saling terhubung satu sama lain. Keunggulan dari basis data yaitu dapat berelasi satu sama lain walaupun berbeda file dalam basis data yang sama. Basis data memiliki kemampuan untuk menyimpan data yang berjumlah sangat besar. Data yang tersimpan dapat digunakan untuk berbagai keperluan tergantung kebutuhan. Sistem basis data ini dapat diimplementasikan pada berbagai jenis komputer karena fleksibilitasnya.

Sistem ini dibuat karena sistem yang lama sudah tidak relevan lagi dengan masa sekarang. Perbedaannya dapat dilihat pada [[Organisasi File Konvensional vs Basis Data|perbandingan antara sistem konvensional dengan sistem basis data.]]

## Komponen Basis Data
Sistem basis data memiliki beberapa komponen yang membangunnya, seperti:
1. Data, hal ini memiliki karakteristik terintegrasi dan dapat dipakai bersama. Data ini juga dapat diakses oleh satu pengguna (*single user*) atau banyak pengguna (*multi-user*) secara bersamaan (concurrent). Hal ini memerlukan mekanisme untuk mengelola agar keutuhan datanya tetap terjaga.
2. Perangkat keras, yaitu peralatan seperti komputer dan peralatan pendukungnya.
3. Perangkat lunak/[[Aplikasi|aplikasi]], hal ini diperlukan agar orang awam bisa menggunakan sistem basis data dengan mudah, contohnya adalah [[Sistem Manajemen Basis Data (SMBD) atau Sistem Manajemen Basis Data (SMBD)|SMBD]].
4. Pengguna, hal ini terbagi menjadi 3, yaitu:
	1. Programmer, yang membuat perangkat lunak.
	2. Pengguna akhir (*end-user*), pengguna perangkat lunak yang sudah jadi.
	3. [[Data Base Administrator (DBA) atau Administrator Basis Data (ADB)|Data Base Administrator (DBA)]], yang mengelola kewenangan akses, mengkoordinasikan pengguna, dan menyediakan perangkat keras dan lunak yang dibutuhkan.

Sistem basis data ini memiliki beberapa keuntungan dan resiko. Di mana keuntungannya seperti:
1. Memiliki [[Redundansi Data|redundansi data]] yang minim.
2. Data selalu konsisten.
3. Data tidak bergantung dengan hal lain (independen).
4. Data terintegrasi.
5. Data bisa dipakai secara bersamaan.
6. Dapat melakukan standarisasi terhadap struktur atau data di dalamnya agar tetap konsisten.
7. Dapat mempermudah pengembangan aplikasi.
8. Akses data dan informasi menjadi lebih cepat.
9. Dapat meningkatkan keamanan dibandingkan sistem konvensional.

Dan untuk resikonya yaitu:
1. Membutuhkan *hardware* dan *software* yang mumpuni.
2. Membutuhkan sumber daya manusia yang mempunyai keahlian spesifik mengenai basis data.
3. Karena data terpusat, maka jika terjadi gangguan, semua yang memakai data tersebut akan terkena.
4. Terjadi konflik tentang siapa yang akan mengelola data siapa karena datanya terpusat di satu tempat.