Yaitu properti atau sifat yang dimiliki oleh suatu entitas. Setiap atribut ini memiliki nilai yang merepsentasikan atribut tersebut.

Atribut ini terbagi menjadi 2, yaitu:
1. **Atribut komposit**, yaitu atribut yang dapat dipecah lagi ke bagian yang lebih kecil.
2. **Atribut sederhana (*atomic*)**, adalah unit atribut terkecil yang tidak dapat dipecah lagi.

![[Pasted image 20250812103016.png]] 

Dapat kita lihat contoh dari atribut komposit yaitu atribut **Address** dan **StreetAddress**, atribut ini dapat dipecah lagi menjadi atribut lainnya. Selain dari 2 atribut tersebut, sisanya adalah atribut sederhana.

Berdasarkan nilainya, atribut terbagi menjadi 2 jenis, yaitu:
1. ***Single-valued***, yaitu atribut yang hanya bisa memiliki satu nilai, contohnya adalah **Umur**.
2. ***Multi-valued***, yaitu atribut yang bisa memiliki lebih dari satu nilai, contohnya adalah **Hobi** atau **Bahasa yang dikuasai**.

Kalau berdasarkan bagaimana nilainya disimpan, atribut ini terbagi juga menjadi 2, yaitu:
1. ***Stored***, yaitu yang nilainya ditulis secara langsung.
2. ***Derived***, adalah yang nilainya didapat dari perhitungan atribut lain.

Atribut juga dapat berisi nilai `null`, nilai ini mencerminkan **"tidak ada"** atau informasi yang tidak diketahui, bukan nilai nol, bukan juga ruang kosong (*blank space*). Contohnya jika kita memiliki entitas mahasiswa yang di dalamnya ada atribut lulus S1 dan lulus S2, saat mahasiswa tersebut masih menjalani studi S1, atirbut lulus S2 masih tidak berlaku padanya, ini yang membuat nilai atribut lulus S2 tersebut adalah `null`.

Jika suatu atribut memiliki sifat komposit dan *multi-valued*, maka atribut tersebut kita sebut atribut kompleks. Atribut ini memiliki notasi seperti:
- () untuk *nesting*.
- {} untuk *multi-value*.
Contoh dari atribut kompleks ini adalah:
{ riwayat_pekerjaan (
	nama_pekerjaan,
	jabatan,
	lama_bekerja
) }

Pada pembuatan atribut, kita akan menentukan tipe data nilai untuk atribut tersebut, tipe data inilah yang kita sebut dengan ***Value Sets***. Tipe data yang ditulis bisa berupa *numeric*, *text*, *boolean*, dan lain-lain. Contohnya seperti:
- Umur harus berupa *numeric*.
- Status Lulus harus berupa *boolean*.

