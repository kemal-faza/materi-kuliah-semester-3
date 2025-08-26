Model data ini mengorganisasi data dalam sebuah struktur yang menyerupai pohon (*tree*) terbalik. Model ini didasarkan pada hubungan *parent/child*. 

Ada beberapa istilah mengenai entitas pada model data ini, yaitu:
- ***Root***, yaitu entitas paling atas dari *tree* tersebut.
- ***Parent***, yaitu entitas yang berada di atas dan terhubung ke entitas di bawahnya.
- ***Child***, yaitu entitas yang berada di bawah dan terhubung ke entitas di atasnya.

![[Pasted image 20250814213803.png]]

Beberapa konsep utama dalam model ini adalah:
- Setiap data yang disimpan diatur dalam tingkatan atau level. Setiap *child* hanya boleh memiliki satu *parent*.
- Untuk menelusuri data yang ada di *child* level terbawah, kita harus memulai dari *root* dan menelusuri ke *child* di bawahnya hingga sampai ke *child* yang dituju. Kita tidak bisa langsung menelusuri ke *child* tersebut tanpa melewati *parent*-nya terlebih dahulu.
- Relasi antar tabel (*child/parent*) dihubungkan menggunakan *pointer* yang mana menunjukkan alamat lokasi data tersebut di dalam penyimpanan.

Model data ini memiliki beberapa kelebihan dan kekurangan. Kelebihannya yaitu:
1. Pencarian data menjadi lebih cepat karena jalur aksesnya yang sudah terstruktur.
2. Integrasi data dapat terjaga karena datanya terhubung secara alami melalui hubungan *parent/child*.

Untuk kekurangannya yaitu:
1. Model ini tidak fleksibel, karena *developer* perlu mengetahui dengan detail urutan hierarki dari *root* hingga ke data yang dituju.
2. Karena setiap *child* hanya boleh memiliki satu *parent*, model ini sulit menangani hubungan *many-to-many*, yang apabila tetap kita implementasikan akan mengakibatkan [[Redundansi Data|redundansi data]].