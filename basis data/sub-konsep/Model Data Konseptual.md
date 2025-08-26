Model ini adalah cara menggambarakan data yang paling mendekati pemahaman manusia atau pengguna. Tujuannya untuk mendefinisikan informasi dari dunia nyata tanpa memikirkan detail teknis penyimpanannya di komputer. Model ini hanya menunjukkan data apa saja yang penting dan bagaimana data tersebut bisa terhubung satu sama lain.

Analoginya seperti sketsa arsitektur pembuatan rumah, di dalamnya menunjukkan ruang tamu, kamar tidur, dan dapur, serta menunjukkan bagaimana ruangan-ruangan tersebut saling terhubung. Akan tetapi, sketsa itu tidak menunjukkan jenis semen atau merk kabel yang digunakan.

Model ini memiliki 3 komponen, yaitu:
1. **Entitas (*Entity*)**, adalah objek atau konsep di dunia nyata yang akan disimpan datanya. Contohnya seperti makanan, minuman, atau mahasiswa.
2. [[Atribut (Attribute)|Atribut]], yaitu properti atau sifat yang dimiliki oleh suatu entitas.
3. **Relasi (*Relationship*)**, adalah hubungan antara dua entitas atau lebih.

![[Pasted image 20250812085658.png]]

Jika ada sekumpulan entitas yang memiliki atribut yang sama, itu disebut ***Entity Type***. Contohnya adalah *student type*, yang mana adalah sekelompok pelajar (students) dari suatu instansi pendidikan.

Karena *entity type* adalah sekelompok entitas dengan atribut yang sama, maka diperlukan suatu atribut yang bisa membedakan suatu entitas dengan entitas lainnya pada kelompok yang sama, atribut ini dinamakan ***key attribute***. Contohnya pada *student type*,  *key attribute*-nya adalah nomor induk siswa tersebut, bisa berupa NIM, NISN, atau yang lain.

Ada beberapa istilah dalam pengkategorian entitas ini, yaitu:
1. ***Superclass***, yaitu suatu entitas yang bersifat umum dan mewakili beberapa entitas yang lebih spesifik. Misalnya adalah:
	1. Entitas **Personalia** yang mewakili semua orang yang bekerja di sebuah intitusi, tanpa memandang terhadap tugas spesifiknya. Entitas ini memiliki atribut umum di dalamnya seperti `nama` dan `NIP`. 
	2. Entitas **Kendaraan** yang mewakili semua jenis kendaraan. Entitas ini memiliki atribut umum seperti `jumlah_roda`, `warna`, dan `merek`.
2. ***Subclass***, yaitu sekelompok entitas yang memiliki beberapa kesamaan atribut dan dapat dikategorikan ke dalam *superclass* tertentu. Selain memiliki atribut yang sama dengan *superclass*-nya, entitas ini juga memiliki atribut uniknya sendiri yang membedakannya antara satu dengan yang lain. Misalnya:
	1. Entitas **Dosen**, **Administrasi**, dan **Laboran** yang merupakan bagian dari *superclass* **Personalia**. Yang mana ketiganya pasti memiliki atribut `nama` dan `NIP`, tapi masing-masing dari mereka memiliki atribut uniknya sendiri yang membedakan mereka.
	2. Entitas **Motor** dan **Mobil** yang merupakan bagian dari *superclass* **Kendaraan**.  Yang mana keduanya pasti memiliki atribut `jumlah_roda`, `warna`, dan `merek`, tapi mereka memiliki atribut unik yang membedakan mereka.

Ada dua teknik untuk merancang struktur entitas, yaitu:
1. **Spesialisasi**, yaitu pendefinisian entitas yang lebih spesifik (*subclass*) dari entitas yang bersifat umum (*superclass*). Misalnya entitas **Dosen** yang bisa dibagi menjadi dua entitas yang lebih spesifik seperti **Dosen Tetap** dan **Dosen Tidak Tetap**. Keduanya tetap memiliki atribut umum yang sama, namun ada penambahan atribut unik pada masing-masing entitasnya.
2. **Generalisasi**, yaitu pengelompokan beberapa entitas (*subclass*) menjadi sebuah entitas yang bersifat umum (*superclass*). Misalkan ada beberapa entitas seperti **Mahasiswa Jalur SNBP**, **Mahasiswa Jalur SNBT**, dan **Mahasiswa Jalur Mandiri**. Karena ketiga entitas tersebut memiliki beberapa atribut yang sama seperti `nama` dan `nim`, maka kita dapat mengelompokkannya ke dalam entitas baru (*superclass*) **Mahasiswa**.