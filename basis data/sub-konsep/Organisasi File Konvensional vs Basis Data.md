Organisasi file adalah penstrukturan sebuah file yang berisi data, termasuk di dalamnya sistem pengalamatan (addressing) yang bertujuan untuk memudahkan proses pengaksesan dan penggantian data. Organisasi file ini ada 2 jenis, yaitu konvensional dan basis data.

![[Pasted image 20250804171620.png]]

Contoh organisasi file yang konvensional adalah seperti ini. Bisa kita lihat bahwa beberapa program seperti program SPP, program registrasi, dan program laporan itu menggunakan sistem yang berbeda (sistem billing dan sistem registrasi). Masing-masing sistem juga mengunakan file yang berbeda, yang dapat kita liat bahwa terdapat penggunaan dua file SPP yang terpisah.

Beberapa masalah yang dapat terjadi apabila menggunakan cara konvensional tersebut yaitu:
1. Data yang terpisah dan terisolasi, yang mana datanya tidak teringtegrasi antara satu sama lain.
2. Terdapat data duplikat karena datanya disimpan di banyak tempat.
3. Terlalu banyak aktivitas data karena banyak file yang terduplikasi.
4. Program yang dijalankan sangat bergantung pada format file, jika format filenya berubah, maka programnya juga harus berubah
5. Karena datanya terisolasi, sulit menyajikan data yang kompleks dan berasal dari sumber yang berbeda

![[Pasted image 20250805085501.png]]

Dapat kita lihat di sini semua sistem tersebut terintegrasi pada satu basis data, yang mana garis-garis di dalam basis ada itu menandakan keterikatan antardata di dalamnya. Pada pendekatan ini, semua sistem menggunakan file yang digunakan bersama. Hal ini memungkinkan pengguna yang sama atau berbeda dapat mengakses data pada waktu yang bersamaan.  Pendekatan ini juga dilengkapi dengan standarisasi dan mekanisme khusus untuk mengatur proses penggunaan file agar tetap utuh dan konsisten.

Basis data ini memiliki [[Redundansi Data|redundansi data]] yang minim dan bisa melayani banyak pengguna sekaligus secara optimal. 