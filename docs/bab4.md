#Bab IV - MODULARITAS

Suatu pemrograman yang baik seharusnya program yang besar dipecah menjadi programprogram
yang kecil yang selanjutnya disebut modul. Modul-modul kecil tersebut dapat dipanggil
sewaktu-waktu diperlukan. Dalam PHP juga mendukung konsep tersebut yang selanjutnya
diberinama modularitas. Kita dapat menyisipkan isi suatu file/modul lain ke dalam file/modul
tertentu.

Terdapat 2 perintah/function untuk hal tersebut dalam PHP yaitu menggunakan include dan
require.



##Include()

Untuk memudahkan pemahaman, diberikan contoh berikut. Misalkan kita akan membuat menu
link sejumlah 4 buah yaitu index, about, links, dan contact pada setiap halaman web yang kita
buat. Teknik yang digunakan adalah membuat menu link dalam suatu modul tersendiri kemudian
modul tersebut dipanggil pada setiap halaman web yang diinginkan terdapat menu link di
dalamnya.

menu.php

```
<html>
	<body>
			 <a href="index.php">Home</a> -
			 <a href="about.php">About Us</a> -
			 <a href="links.php">Links</a> -
			 <a href="contact.php">Contact Us</a> <br>
```

index.php

```
<?php
	 include("menu.php");
?>
	 <p>Ini adalah halaman index</p>
</body>
</html>
```

about.php

```
<?php
	 include("menu.php");
?>
	 <p>Ini adalah halaman about</p>
		 </body>
     </html>
```
Dari teknik di atas tampak adanya kemudahan dalam membuat halaman web. Dalam hal ini, kita
tidak perlu membuat menu link di setiap halaman web yang ada. Bayangkan seandainya kita
punya halaman web sejumlah 100 buah yang kesemuanya ingin diberi menu link tanpa
menggunakan teknik di atas, tentu hal tersebut sangat merepotkan.

Meskipun secara teknis, kode pembangun web dipecah dalam modul-modul, namun ketika di
browser akan terlihat menyatu. Berikut ini adalah kode HTML yang dihasilkan oleh browser ketika
membuka halaman web index.php

```
<html>
	 <body>
		 <a href="index.php">Home</a> -
		 <a href="about.php">About Us</a> -
		 <a href="links.php">Links</a> -
		 <a href="contact.php">Contact Us</a> <br>
			 <p>Ini adalah halaman index</p>
	 </body>
</html>
```



##Require()
Cara penggunaan maupun fungsi dari require() sama dengan include(). Jadi apa perbedaannya?
Sebaiknya mana yang kita gunakan? Perhatikan contoh berikut ini

```
<?php
	 include("noFileExistsHere.php");
		 echo "Hello World!";
?>
```

dengan asumsi bahwa file noFileExistxHere.php tidak ada.
Maka dengan menggunakan include() akan dihasilkan tampilan:

```
Warning: main(noFileExistsHere.php): failed to open stream: No such
file or directory in include.php on line 2
```

```
Warning: main(): Failed opening 'noFileExistsHere.php' for inclusion
(include_path='.:/usr/lib/php:/usr/local/lib/php') in include.php on
line 2
```

Hello World

Selanjutnya kita akan gunakan require().

```
<?php
	 require("noFileExistsHere.php");
		 echo "Hello World!";
?>
```

dan hasilnya

```
Warning: main(noFileExistsHere.php): failed to open stream: No such
file or directory in require.php on line 2
```

```
Fatal error: main(): Failed opening required 'noFileExistsHere.php'
(include_path='.:/usr/lib/php:/usr/local/lib/php') in require.php on
line 2
```

Bandingkan kedua hasil di atas, khususnya yang tercetak merah. Pada include(), error yang
dihasilkan hanya berupa Warning saja dan statement berikutnya masih dapat dijalankan. Hal ini
terlihat bahwa teks Hello World! Masih ditampilkan di browser. Sedangkan pada require(),
error yang dihasilkan berupa Fatal Error. Dengan demikian statement selanjutnya tidak akan
dijalankan.

Disarankan agar Anda menggunakan require() dengan harapan bahwa kode PHP yang Anda
buat tidak akan diproses apabila terdapat file yang hilang atau tidak ada.
