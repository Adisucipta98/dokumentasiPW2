
#BAB II. PHP - SINTAKS

Kode-kode PHP dituliskan di antara tanda berikut ini:  

```
<?php  
... ... ...  
?>  
```

atau 

``` 
<?  
... ... ...  
?> 
```
 
Apabila Anda membuat kode PHP dan berencana akan mendistribusikan ke pihak/orang lain, 
maka usahakan untuk menggunakan sintaks <?php ... ?>. 
Hal ini dikarenakan untuk penggunaan kode yang menggunakan <? ?> terkadang tidak bisa dijalankan dalam server tertentu.



## Menyimpan File PHP

Apabila Anda memiliki kode PHP yang disisipkan dalam HTML dalam suatu file dan menginginkan web server dapat menjalankannya, 
maka file tersebut harus disimpan dalam ekstensi .php . 
Apabila Anda menyimpannya dengan ekstensi .html atau .htm, maka kode PHP tersebut tidak akan diproses dan akan ditampilkan 
dalam web browser seperti apa adanya (berupa kode-kode). 

**Contoh :**

```
<html> 
	 <head> 
		 <title>Halaman PHP pertamaku</title> 
	 </head> 
	 <body> 
		 <?php 
			 echo "Hello World!"; 
		 ?> 
	 </body> 
</html>
```



##Semicolon (;)

Apabila Anda perhatikan contoh sebelumnya, maka terdapat tanda titik koma (semicolon) pada akhir perintah echo. 
Tanda semicolon merupakan penanda akhir dari statement PHP dan harus ada. 

**contoh :**

```
<html> 
	 <head> 
		 <title>Halaman PHP pertamaku</title> 
	 </head> 
	 <body> 
		 <?php 
			 echo "Hello World! ";
			 echo "Hello World! ";
			 echo "Hello World! ";
			 echo "Hello World! ";
			 echo "Hello World! "; 
		 ?> 
	 </body> 
</html>
```


##Pindah Spasi

Seperti halnya HTML, pergantian spasi dalam PHP tidak akan mempengaruhi tampilan hasilnya. 
Dengan kata lain, pergantian spasi akan diabaikan oleh PHP.

Perhatikan contoh berikut ini. Pada contoh tersebut diberikan tiga bentuk penulisan kode PHP
yang berbeda namun akan dihasilkan tampilan yang sama dalam web browser.

Contoh:

```
<html>
	 <head>
		 <title>Halaman PHP pertamaku</title>
	 </head>
	 <body>
		 <?php
			 echo "Hello World! ";
		     echo "Hello World! ";
		 ?>
	 </body>
</html>
```

```
<html>
	 <head>
		 <title>My First PHP Page</title>
	 </head>
	 <body>
		 <?php
			 echo "Hello World! "; echo "Hello World! ";
		 ?>
	 </body>
</html>
```

```
<html>
	 <head>
		 <title>Halaman PHP pertamaku</title>
	 </head>
	 <body>
		 <?php
			 echo "Hello World! ";
			 echo "Hello World! ";
		 ?>
	 </body>
</html>
```



##Variabel

Misalkan dalam PHP kita akan menyimpan suatu nilai berupa angka atau string dalam suatu
variabel, caranya adalah membuat nama variabel terlebih dahulu kemudian diberikan suatu
assignment pada nilai yang diinginkan. 
Perhatikan sintaks berikut ini.

```
$nama_variabel = nilai;
```

**Note: jangan lupa tanda dollar ($)**

**Contoh:**

```
<?php
	 $hello = "Hello World!";
	 $sebuah_bilangan = 4;
	 $bilanganYangLain = 8;
?>
```

Dari contoh di atas tampak bahwa dalam PHP, nama variabel tidak perlu dideklarasikan terlebih
dahulu seperti halnya bahasa Pascal atau C/C++.



##Aturan Penamaan Variabel

Berikut ini adalah beberapa aturan penulisan nama variabel:

* Nama variabel harus diawali dengan huruf atau underscore (_)
* Nama variabel hanya boleh dituliskan dengan alpha numeric a-z, A-Z, 0-9 dan underscore
* Nama variabel yang terdiri lebih dari satu kata, dapat dipisahkan dengan underscore



##Echo

Seperti yang Anda lihat pada contoh-contoh kode PHP sebelumnya, bahwa perintah echo
digunakan untuk menampilkan teks ke dalam browser. Suatu teks atau string dapat dituliskan di
browser dengan langsung dituliskan dalam echo yang diapit oleh dua tanda petik ganda (quotes)
atau menyimpan string atau teks terlebih dahulu dalam suatu variabel kemudian dituliskan dalam
echo. 

Berikut ini adalah contohnya:

contoh :

```
<?php
	 $StringKu = "Hello!";
		 echo $StringKu;
		 echo "<h5>I love using PHP!</h5>";
?>
```

**PENTING !!**

Hati-hati dalam penulisan suatu string yang di dalamnya terdapat tanda petik ganda (quotes)
menggunakan echo. Dalam echo, tanda quotes merupakan penanda awal dan akhir teks/string
yang akan ditulis dengan echo, sehingga Anda harus memperhatikan hal-hal berikut ini :

* Jangan menggunakan tanda quotes di dalam teks yang akan ditulis dengan echo
* Apabila Anda tetap ingin menuliskan tanda quotes dalam teks yang akan ditulis dengan echo,
  maka berikan tanda slash “\” di depan quotes tersebut.
* Selain itu, dapat pula Anda gunakan tanda petik tunggal (apostrophes) untuk
  menggantikan tanda quotes pada teks.

**Contoh :**

```
<?php
	 echo "<font face="verdana" size="4">I love using PHP!</font>";
?>
```

```
<?php
	 echo "<font face=\"verdana\" size=\"4\">I love using PHP!</font>";
?>
```

```
<?php
echo "<font face='verdana' size='4'>I love using PHP!</h5>";
?>
```

Pada contoh kode pertama di atas akan terjadi error karena dalam teks yang ditulis dalam echo
terdapat tanda quotes. Sedangkan untuk kode kedua dan ketiga tidak terdapat error dan akan
dihasilkan output yang sama di browser.



##Menampilkan Nilai Variabel dengan Echo

Nilai variabel dapat dengan mudah ditampilkan dengan menggunakan echo, baik nilai yang
berupa bilangan maupun string. Berikut ini adalah contoh-contoh di antaranya:

Contoh:

```
<?php
	 $string_ku = "Hello.. Nama saya: ";
	 $bilangan_ku = 4;
	 $huruf_ku = "a";
		 echo $string_ku;
		 echo $bilangan_ku;
		 echo $huruf_ku;
?>
```

Catatan:
Untuk menampilkan nilai variabel dengan echo tanpa menggunakan tanda quotes.
Berikut ini contoh menampilkan gabungan suatu nilai dari variabel yang berupa string.

Contoh:

```
<?php
	 $string_ku = "Hello. Nama saya: ";
	 $baris_baru = "<br>";
		 echo $string_ku."Ari".$baris_baru;
		 echo "Hi, Nama saya Ari. Kamu siapa? ".$string_ku.$baris_baru;
		 echo "Hi, Nama saya Ari. Kamu siapa? ".$string_ku."Amalia";
?>
```

Untuk menggabungkan beberapa string menjadi satu digunakan operator dot (.)



##Komentar dalam PHP.

Seperti halnya bahasa pemrograman yang lain, komentar dalam suatu kode PHP tidak akan
dieksekusi. Terdapat dua cara memberikan komentar dalam PHP, yaitu :

* Diberikan tanda // di depan teks komentar. Perintah ini hanya bisa berlaku untuk
  komentar dalam satu baris
* Diberikan tanda /* di depan teks komentar dan diakhiri dengan */. Perintah ini dapat
  digunakan untuk komentar yang terdiri lebih dari satu baris.

Contoh:

```
<?php
	 echo "Hello World!"; // Ini akan mencetak Hello World!
	 echo "<br>Psst...You can't see my PHP comments!"; // echo "nothing";
	 // echo "Namaku Faza!";
?>
```

```
<?php
	 /* Berikut ini adalah perintah
	    untuk menuliskan Hello World */
	 echo "Hello World!";
	 /* echo "My name is Humperdinkle!";
     echo "No way! My name is Ari-PHP Programmer!";
	 */
?>
```