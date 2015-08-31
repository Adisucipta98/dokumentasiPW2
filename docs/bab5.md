
#BAB V. ARRAY

Dalam PHP, indeks untuk array dapat berupa numerik dan dapat pula berupa suatu nilai atau
yang sering disebut dengan array assosiatif.



##Array Berindeks Numerik

Sintaks umum untuk menyatakan suatu array berindeks numerik beserta nilainya adalah

```
$nama_array[$key] = value;
```

Dalam hal ini $key berupa bilangan bulat mulai dari 0, 1, 2, …

Contoh:

```
$karyawan[0] = "Bob";
$karyawan[1] = "Sally";
$karyawan[2] = "Charlie";
$karyawan[3] = "Clare";
```

Sedangkan berikut ini adalah contoh untuk menampilkan nilai dari suatu array berindeks numerik.

```
<?
	 $karyawan[0] = "Bob";
	 $karyawan[1] = "Sally";
	 $karyawan[2] = "Charlie";
	 $karyawan[3] = "Clare";
		 echo "Berikut ini adalah 2 orang karyawan saya, yaitu ". $karyawan[0] . " & " . $karyawan[1];
		 echo "<br>Dua orang karyawan saya yang lain adalah ". $karyawan[2] . " & " . $karyawan[3];
?>
```



##Array Assosiatif

Untuk array assosiatif, sintaksnya sama dengan array berindeks numerik namun perbedaannya
adalah pada $key. Pada array assosiatif, $key dapat berupa suatu string. Berikut ini adalah
contohnya.

```
$gaji["Bob"] = 2000;
$gaji["Sally"] = 4000;
$gaji["Charlie"] = 600;
$gaji["Clare"] = 0;
```

dan berikut ini adalah contoh kode untuk menampilkan nilai dari array assosiatif

```
<?
	 $gaji["Bob"] = 2000;
	 $gaji["Sally"] = 4000;
	 $gaji["Charlie"] = 600;
	 $gaji["Clare"] = 0;
		 echo "Bob digaji - $" . $gaji["Bob"] . "<br>";
		 echo "Sally digaji - $" . $gaji["Sally"] . "<br>";
		 echo "Charlie digaji - $" . $gaji["Charlie"] . "<br>";
		 echo "dan Clare digaji - $" . $gaji["Clare"];
?>
```
