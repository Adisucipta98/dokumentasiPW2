#BAB III. PHP – OPERATOR

Dalam bahasa pemrograman secara umum, operator digunakan untuk memanipulasi atau
melakukan proses perhitungan pada suatu nilai. Sampai saat ini, Anda telah mengenal operator
“.” (menggabungkan string) dan “=” (proses assignment). Selain dua operator itu masih banyak
jenis operator yang lain dalam PHP yaitu:

* Operator aritmatik
* Operator perbandingan
* Gabungan operator aritmatik dan assignment



##Operator Aritmatik
**Berikut ini adalah tabel operator aritmatik, makna dan contohnya:**

![Gambar](..\pendahuluan.png)

Contoh:

```
<?php
	 $penjumlahan = 2 + 4;
	 $pengurangan = 6 - 2;
	 $perkalian = 5 * 3;
	 $pembagian = 15 / 3;
	 $modulus = 5 % 2;
		 echo "Menampilkan penjumlahan: 2 + 4 = ".$penjumlahan."<br>";
		 echo "Menampilkan pengurangan: 6 - 2 = ".$pengurangan."<br>";
		 echo "Menampilkan perkalian: 5 * 3 = ".$perkalian."<br>";
		 echo "Menampilkan pembagian: 15 / 3 = ".$pembagian."<br>";
		 echo "Menampilkan modulus: 5 % 2 = " . $modulus.";
?>
```



##Operator Perbandingan

Perbandingan digunakan untuk menguji hubungan antara nilai dan atau variabel. Operator ini
digunakan dalam suatu statement bersyarat yang selalu menghasilkan nilai TRUE atau FALSE.

Misalkan:

```
$x = 4; $y = 5;
```

berikut ini adalah beberapa contoh penggunaan operator perbandingan dan hasilnya

![Gambar](..\pendahuluan1.png)



##Kombinasi Operator Aritmatik dan Assignment

Dalam pemrograman seringkali dijumpai proses yang melibatkan proses increment. Misalkan kita
menginginkan proses increment dengan tingkat kenaikan 1, maka perintah yang dituliskan dapat
berupa

```
$counter = $counter + 1;
```

dalam PHP, perintah di atas dapat ditulis dalam satu perintah singkat sebagai

```
$counter += 1;
```

Dari contoh di atas tampak bahwa operator yang digunakan (+=) merupakan gabungan dari
operator aritmatik dan assignment. Berikut ini adalah bentuk-bentuk operator lain jenis ini.

![Gambar](..\pendahuluan2.png)



##Operator Pre/Post Increment dan Decrement

Operator jenis ini merupakan pengembangan dari operator jenis sebelumnya. Operator ini hanya
digunakan pada proses increment maupun decrement dengan tingkat 1.
Berikut ini adalah operator yang termasuk jenis ini:

```
· $x++; ekuivalen dengan $x += 1; atau $x = $x + 1;
· $x--; ekuivalen dengan $x -= 1; atau $x = $x – 1;
```

Contoh:

```
<?php
	 $x = 4;
	 $x++;
	 echo "$x;
	 $x = 4;
	 $x--;
		 echo "$x;
?>
```