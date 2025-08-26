Model data ini adalah pengembangan dari model data [[Model Data Hierarki|hierarki]], yang mana memiliki fleksibilitas struktur seperti **jaring laba-laba** atau **graf**. Dalam model  ini, kita mendasari data dengan hubungan *owner/member* yang mirip dengan hubungan *parent/child*.

Beberapa konsep utama model data ini yaitu:
- Struktur yang berupa graf, hal ini membuat satu *member* bisa memiliki banyak *owner* dan memungkinkan implementasi hubungan *many-to-many* yang sebelumnya tidak bisa dilakukan.
- Relasi antara *owner* dengan *member* ini disebut dengan ***set***, yang terdiri dari satu *owner* dan satu/beberapa *member*.
- Karena bentuk strukturnya yang seperti graf, hal ini membuat akses data menjadi lebih fleksibel. Yang di mana jika kita ingin mencari sebuah data, kita dapat mulai dari beberapa titik, tidak harus dari atas ke bawah, yang membuat pencarian data menjadi lebih efisien.

![[Pasted image 20250821073443.png]]

Model data ini juga memiliki beberapa kelebihan dan kekurangan. Di mana kelebihannya yaitu:
1. Pengaksesan data yang menjadi lebih fleksibel dan efisien karena strukturnya yang berupa graf.
2. Bisa mengimplementasikan relasi yang kompleks seperti *many-to-many*.
3. Karena satu *member* bisa memiliki beberapa *owner*, maka kita tidak perlu menduplikasi data tersebut seperti sebelumnya, hal ini membantu mengurangi [[Redundansi Data|redundansi]].

Adapun untuk kekurangannya yaitu:
1. Karena strukturnya yang rumit, membuatnya sulit dimodifikasi.
2. Program yang bergantung pada struktur modelnya, yang apabila terjadi perubahan struktur, maka kode program juga harus ikut berubah.
3. *Developer* harus sangat memahami tentang struktur keseluruhan *set*, *owner*, dan *member* yang ada pada basis data.