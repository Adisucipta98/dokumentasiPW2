#BAB XII. FUNCTION DATE

Pada bab ini akan dibahas mengenai cara menampilkan tanggal ke dalam halaman web. Tanggal
yang akan ditampilkan menyesuaikan waktu server, bukan waktu yang ada di client. Hal ini
disebabkan PHP merupakan server side programming.

Contoh:

```
<?
	 echo date("m/d/y");
?>
```

Function date() digunakan untuk menampilkan tanggal pada saat itu
(sesuai waktu server). Misalkan pada saat itu adalah tanggal 12
Nopember 2005, maka tampilan dari script di atas adalah
11/12/05
Kita dapat mengubah format tanggal dalam bentuk 12-11-05 dengan perintah

```
<?
	 echo date("d-m-y");
?>
```

Lantas bagaimana kalau kita ingin menampilkan tanggal pada 2 hari mendatang? Berikut ini
scriptnya.

```
<?
	 $duaharilagi = mktime(0, 0, 0, date("m"), date("d")+2, date("y"));
		 echo "Dua hari lagi adalah tanggal ". date("d/m/y", $duaharilagi);
?>
```

Function mktime() digunakan untuk membuat timestamp, dengan sintaks:
mktime(hour, minute, second, month, day, year)

Contoh:

```
<?php
	 $tomorrow = mktime(0, 0, 0, date("m") , date("d")+1, date("Y"));
	 $lastmonth = mktime(0, 0, 0, date("m")-1, date("d"), date("Y"));
	 $nextyear = mktime(0, 0, 0, date("m"), date("d"), date("Y")+1);
		 echo "Besok adalah tanggal ". date("d/m/y", $tomorrow) . "<br>";
		 echo "Sebulan lalu adalah tanggal ". date("d/m/y", $lastmonth). "<br>";
		 echo "Setahun lagi adalah tanggal ". date("d/m/y", $nextyear). "<br>";
?>
```

Beberapa ini beberapa jenis timestamp yang dapat digunakan untuk mengatur format tampilan
tanggal dan waktu

![Gambar](..\pendahuluan3.png)

Contoh:

```
<?php
// Misalkan hari ini adalah: 10 Maret 2001, 5:16:18 pm
	 $today = date("F j, Y, g:i a");
		 echo "$today";
	 $today = date("m.d.y");
		 echo "$today";
	 $today = date("j, n, Y");
		 echo "$today";
	 $today = date("Ymd");
		 echo "$today";
	 $today = date("H:i:s");
		 echo "$today";
?>
```

Hasilnya adalah:

```
March 10, 2001, 5:16 pm
03.10.01
10, 3, 2001
20010310
17:16:17
```
