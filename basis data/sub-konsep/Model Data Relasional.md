Model data ini dikenalkan oleh **Ted Codd** dari IBM Research pada tahun 1970. Model ini sekarang banyak digunakan dalam sistem basis data modern karena mudah dipahami.

Model ini merepresentasikan data dalam bentuk relasi atau secara sederhana merupakan tabel dua dimensi yang memiliki baris dan kolom, yang mana:
- **Kolom (atribut/*fields*)** yang mewakili properti dari data.
- **Baris (tuple/*records*)** yang mewakili satu entitas atau satu set data lengkap.
- **Sel**, yang mewakili sub-entitas dari suatu data dan juga merupakan perpotongan antara baris dan kolom.

Ada beberapa ketentuan yang ketat di dalam model ini, yaitu:
1. Tidak ada baris yang rangkap/terduplikat, yang mana keunikannya terjamin oleh *primary key* pada setiap baris.
2. Urutan baris tidak berpengaruh, karena kita mengambil data berdasarkan nilainya.
3. Urutan kolom juga tidak berpengaruh, karena kita mengaksesnya berdasarkan namanya.
4. Setiap sel hanya bisa berisi satu nilai tunggal, tidak dapat berisi beberapa nilai sekaligus.

![[Pasted image 20250821101431.png]]

Ada beberapa kelebihan dan kekurangan model data ini. Di antara kelebihannya yaitu:
- Struktur data menjadi lebih mudah dimodifikasi karena strukturnya bukan berupa *pointer* seperti model data [[Model Data Hierarki|hierarki]] atau [[Model Data Network|network]].
- Dapat membuat kueri yang kompleks menggunakan SQL (Structured Query Language)
- Integritas data dapat terjaga karena adanya aturan seperti *Entity Integrity* dan *Referential Integrity* yang mudah diimplementasikan.
- *Developer* bisa dengan mudah mengembangkan aplikasi.

Adapun kekurangannya yaitu:
- Data yang disimpan tidak terpusat, apabila kita ingin mendapatkan informasi yang lengkap, kita harus menggabungkan beberapa tabel yang mana jika tidak dioptimalkan akan memakan sumber daya yang besar.
- *Developer* harus memahami bagaimana data-data tersebut terhubung di dalam tabel.
- *Developer* juga harus memahami cara menggunakan SQL agar bisa berinteraksi dengan data tersebut.
