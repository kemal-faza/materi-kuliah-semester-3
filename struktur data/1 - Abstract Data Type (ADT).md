Sebelum masuk ke pembahasan mengenai ADT, kita sebaiknya mengingat beberapa konsep yang sebelumnya kita pelajari dan berhubungan dengan ADT ini. Yang pertama adalah cara-cara berpikir komputasional seperti:
1. **Dekomposisi**, yaitu memecah masalah-masalah menjadi bagian yang lebih kecil.
2. **Abstraksi**, yaitu menyederhanakan masalah-masalah tersebut dengan hanya fokus pada detail-detail yang penting.
3. **Algoritma**, yaitu cara kita menyelesaikan persoalan yang ada.
4. ***Pattern Recognition***, yaitu mengenali pola masalah yang terjadi, barangkali pernah terjadi sebelumnya dan masalah tersebut bisa diselesaikan lebih cepat.

Yang kedua mengenai type, nilai, dan variabel, yang artinya:
1. **Tipe**, adalah jenis dari suatu data yang bisa direpresentasikan oleh komputer.
2. **Variabel**, yaitu nama tempat menyimpan sebuah nilai.
3. **Nilai**, adalah sesuatu yang bertipe dan bisa disimpan di dalam variabel.

Setelah mengenai mengenai tipe, ada beberapa jenis tipe data, yaitu:
1. **Tipe data tunggal**, yang hanya boleh berisi satu nilai saja, seperti `boolean`, `integer`, `real`, `character`, dan `string`.
2. **Tipe data koletif**, yang bisa berisi banyak nilai sekaligus, seperti `array`.
3. **Tipe data komposit**, yaitu tipe data yang kita bentuk sendiri berdasarkan jenis tipe data lainnya, contohnya `titik`, `jam`, dan `date`.
```pseudocode
{ Tipe data titik }
type Titik : < x : integer {absis},
			   y : integer {ordinat} >
```

Selain tipe data, ada juga pengertian mengenai beberapa *sub-routine*/subprogram, yaitu:
1. **Fungsi**, yaitu subprogram yang mengembalikan nilai, fungsi ini bisa menerima nilai ataupun tidak.
2. **Prosedur**, subprogram yang tidak mengembalikan nilai, tapi bisa merubah nilai dari variabel yang sudah ada. Hal ini didasari dari keadaan awal sebelum prosedur dieksekusi (*initial state*/`I.S.`) dan keadaan akhir setelah prosedur dieksekusi (*final state*/`F.S.`).
3. **Parameter formal dan aktual**. **Parameter formal** adalah parameter yang kita gunakan saat melakukan pembuatan fungsi atau prosedur, parameter ini masih belum ada nilainya. Sedangkan **parameter aktual** adalah nilai yang kita masukkan saat menjalankan fungsi atau prosedur.

## Struktur Data
Saat kita membangun sebuah program, membuat struktur data yang baik adalah salah satu *building block* yang penting. Karena tanpa pengorganisasian data yang baik, program tidak dapat berjalan dengan semestinya. 

Struktur data ini bukan hanya mendefinisikan bagaimana data disimpan, melainkan bagaimana data tersebut disusun dan dikelola agar tercapainya efisiensi biaya seperti penggunaan memori dan sebagainya.

Terdapat dua kategori utama dalam jenis struktur data, yaitu:
1. Primitif & Non-Primitif
	1. Primitif, yaitu struktur data paling dasar dalam pemrograman, seperti `integer`, `char`, dan `boolean`.
	2. Non-Primitif, yaitu struktur data yang lebih kompleks dan terbentuk dari tipe data primitif, seperti `array`, `linked list`, dan `tree`.
2. Linear & Non-Linear
	1. Linear, yaitu struktur data yang datanya disusun secara sekuensial. Hal ini terbagi menjadi:
		1. **Penyimpanan sekuensial**, data-datanya disimpan berdekatan secara fisik di memori yang memungkinkan akses menjadi lebih cepat, contohnya seperti `array`.
		2. **Akses sekuensial**, walaupun letaknya di memori tidak berurutan, akan tetapi tiap elemen memiliki petunjuk mengenai lokasi elemen selanjutnya. Akses ini harus berurutan dari awal, tidak bisa langsung mengakses ke tengah data, contohnya adalah `linked list`.
	2. Non-Linear, yang hubungan antardata-nya tidak berurutan dan bisa saja bercabang. Contohnya seperti `tree` dan `graph`.

## Abstract Data Type (ADT)
ADT adalah abstraksi dari tipe data yang membuat pengguna bisa fokus pada hal apa saja yang bisa dilakukan tanpa harus mengetahui bagaimana hal tersebut terjadi. Hal ini membuat pengguna bisa langsung mengimplementasikan ADT tersebut tanpa memikirkan kerumitan di dalamnya. 

ADT ini memungkinkan perubahan pada implementasi apabila diperlukan tanpa harus mengubah program utama ADT tersebut selama spesifikasinya tetap sama. 

ADT terdiri dari beberapa komponen seperti:
1. Type, yaitu jenis struktur data yang akan digunakan, hal ini mirip seperti tipe data komposit.
2. Primitif, yaitu fungsi atau prosedur yang digunakan untuk memanipulasi data dengan `type` tersebut. Ada beberapa jenis primitif, yaitu:
	1. ***Constructor***, yang digunakan untuk membuat nilai dari `type` tersebut. Biasanya namanya diawali dengan `Make`, seperti `MakeTitik.
	2. ***Selector***, yang digunakan untuk mengakses nilai salah satu komponen dari `type` tersebut. Biasanya diawali dengan `Get`, seperti `GetAbsis`.
	3. ***Mutator***, yang digunakan untuk mengubah nilai salah satu komponen dari `type` tersebut. Biasanya diawali dengan `Set`, seperti `SetAbsis`.
	4. ***Validator***, yang digunakan untuk memeriksa apakah suatu nilai itu sesuai dengan `type` tersebut. Biasanya diawali dengan `Is`, seperti `IsEqual`.
	5. ***Destructor***, yang digunakan untuk menghancurkan nilai yang ada pada `type` tersebut.
	6. **Baca/Tulis**, yang digunakan untuk berinteraksi dengan perangkat I/O.
	7. **Operator rasional**, seperti `<`, `>`, dan `=`.
	8. **Operator aritmatika**, seperti `+`, `-`, `*`, atau `/`.
	9. **Konversi**, yang digunakan untuk mengkonversi `type` tersebut ke tipe primitif atau sebaliknya.

ADT adalah sebuah definisi statik atau *blueprint*. definisinya sudah ditentukan saat dirancang dan dikompilasi. Objek yang menggunakan ADT inilah yang bersifat dinamis karena bisa berubah-ubah, sedangkan definisi ADT-nya tetap statik.

## Desain ADT
ADT memiliki 2 bagian utama, yaitu:
1. Definisi dan Spesifikasi Tipe dan Prototipe, ini berisi beberapa spesifikasi seperti type dan primitif (fungsi atau prosedur).
2. Body / Realisasi Prototipe, yang berisi implementasi dari fungsi/prosedur yang didefinisikan dan memanfaatkan *constructor* dan *selector* sebisa mungkin.
```latex
						Modul T_Titik
			Definisi dan Spesifikasi Tipe dan Prototipe
type Titik : < x : integer, y : integer >
procedure CreateTitik (output T : Titik)
{I.S : - ; F.S : T terdefinisi}
{Proses mengisi absis dan ordinat dengan 0}

function F (T : Titik) -> integer
{mengembalikan jumlah nilai absis + ordinat}

					Body/Realisasi Prototipe
procedure CreateTitik (output T : Titik)
	Kamus lokal
		-
	Algoritma
		T.x <- 0
		T.y <- 0

function F (T: Titik) -> integer
	Kamus lokal
		-
	Algritma
		-> T.x + T.y
```

Terdapat sebuah program utama yang digunakan untuk mengetes ADT, program ini dinamakan ***driver***, tujuannya adalah memastikan bahwa setiap komponen dari ADT itu berjalan dengan semestinya sebelum diimplementasikan pada aplikasi yang lebih kompleks. Driver ini akan memanggil setiap primitif (fungsi dan prosedur) yang telah dibuat dan mengujinya dengan beberapa kemungkinan parameter.

Jika diibaratkan, pengetesan ini memiliki hubungan sebagai *supplier* dan *client*. Yang mana ADT sebagai *supplier* akan menyediakan tipe data dan primitif untuk diuji coba. Sedangkan *driver* sebagai *client* akan menguji coba tipe data dan primitif yang dimiliki oleh ADT tersebut.

## Perbedaan Paradigma Fungsional dan Prosedural

![[Screenshot 2025-08-27 203550.png]]

Berdasarkan gambar ini, paradigma fungsional umumnya memiliki struktur ADT sederhana seperti header, defspek (definisi dan spesifikasi), realisasi, dan aplikasi yang sudah mencakup tipe data dan program utamanya. Akan tetapi, pada paradigma prosedural, tipe data dan program utama itu dipisahkan menjadi ADT yang berbeda. Hal ini diperlukan agar ADT bisa menjadi komponen yang dapat digunakan kembali.

## Enkapsulasi pada ADT

![[Screenshot 2025-08-27 203607.png]]

Pada gambar ini, tipe data A dan B bisa langsung digunakan pada program utama, tanpa perlu mengetahui detail bagaimana tipe data tersebut diimplementasikan karena mereka merupakan ADT yang sudah siap pakai. Berikut ini contohnya.

![[Screenshot 2025-08-27 203616.png]]

## Jenis ADT
Berdasarkan cara menstrukturkan data, ADT terbagi menjadi tiga, yaitu:
1. Unit tunggal, yaitu suatu variabel yang memiliki komponen penyusun bertipe data tunggal, contohnya `titik` yang penyusunnya berupa `x` dan `y` yang bertipe `integer`.
2. Unit kolektif, yaitu suatu variabel yang komponen penyusunnya bertipe data kolektif, seperti `table` atau `matrix` yang penyusunnya bisa berupa `array`.
3. Unit koleksi berkait, yaitu suatu variabel yang komponennya saling terhubung satu sama lain, seperti `linked-list` atau `tree`.

Untuk implementasi ADT pada bahasa C, terdapat pengelompokkan berdasarkan strukturnya, yaitu:

| ADT                                        | Bahasa C                         |
| ------------------------------------------ | -------------------------------- |
| Definisi dan Spesifikasi Tipe dan Primitif | File header modul berekstensi .h |
| Body/Realisasi Primitif                    | File kode modul berekstensi .c   |
| Program Utama/Driver                       | File kode utama berekstensi .c   |
