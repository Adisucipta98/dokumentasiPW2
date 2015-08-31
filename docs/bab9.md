#BAB IX. FUNCTION

Sebuah function merupakan sebuah nama yang kita berikan pada suatu blok program yang
sewaktu-waktu dapat kita panggil dan gunakan. Sebuah function dapat diletakkan di bagian
manapun, bisa di awal, tengah, dan akhir dari keseluruhan bagian kode PHP.
Berikut ini adalah contoh membuat sebuah function sederhana yang di dalamnya tidak ada
statementnya.

Contoh:

```
<?php
	 function myCompanyMotto()
	 {
	 }
		 myCompanyMotto();
?>
```

Pada contoh di atas, myCompanyMotto merupakan nama function. Nama function inilah yang
dapat dipanggil sewaktu-waktu diperlukan. Aturan membuat nama function sama dengan ketika
membuat nama variabel (lihat di Bab II). Statement/perintah dari function dituliskan di dalam
kurung kurawal {}. Sedangkan perintah myCompanyMotto(); bagian paling bawah dari kode di
atas merupakan cara memanggil function. Perhatikan contoh berikutnya:

Contoh:

```
<?php
	 function myCompanyMotto()
	 {
		 echo "Sabar adalah bagian dari keimanan";
	 }
	 myCompanyMotto();
?>
```

Pada contoh tersebut, terdapat perintah echo di dalam function. Sehingga begitu nama function
dipanggil, PHP akan menampilkan teks yang di-echo-kan tersebut.
Sebuah function dapat dipanggil berulang-ulang, seperti pada contoh berikut.

```
<?php
	 function myCompanyMotto()
	 {
		 echo "Sabar adalah bagian dari keimanan";
	 }
		 echo "Selamat datang di PT. Nada Corp. <br>";
	 myCompanyMotto();
		 echo "Terima kasih atas kunjungan Anda<br>";
		 echo "dan ingatlah selalu... <br>";
	 myCompanyMotto();
?>
```

##Fungsi dengan Parameter

Contoh function sebelumnya tidak menggunakan parameter. Peran parameter adalah sebagai
input untuk function yang selanjutnya diolah oleh function tersebut. Berikut ini contoh
penggunaan parameter pada function.

```
<?php
	 function UcapanSalam($nama)
	 {
		 echo "Hallo ". $nama . "!<br>";
	 }
?>
```

Pada contoh di atas, variabel $nama merupakan parameter dari function. Nilai dari variabel
tersebut akan ditambahkan pada string yang di-echo-kan.
Selanjutnya akan diberikan contoh penggunaan function dengan parameter.

```
<?php
	 function UcapanSalam($nama)
	 {
		 echo "Hallo ". $nama . "!<br>";
	 }
		 UcapanSalam("Agus");
		 UcapanSalam("Ahmad");
		 UcapanSalam("Budi");
		 UcapanSalam("Fauzan");
?>
```

Jumlah parameter dari function boleh lebih dari satu. Untuk memisahkan antar parameter
digunakan tanda koma. Berikut ini contohnya.

```
<?php
	 function UcapanSalam($kepada, $dari)
	 {
		 echo $dari . " mengucapkan salam kepada ". $kepada . "<br>";
	 }
		 UcapanSalam("Ari", "Amalia");
		 UcapanSalam("Amalia", "Nada");
		 UcapanSalam("Nada", "Faza");
		 UcapanSalam("Fauzan", "Ari");
?>
```

##Pengembalian Nilai (Return Value)

Sebuah function juga dapat mengembalikan suatu nilai. Function hanya dapat mengembalikan
sebuah nilai saja. Nilai yang dikembalian dapat berupa suatu bilangan (bulat, real), string,
maupun array, dll.
Berikut ini adalah contoh penggunaan function yang mengembalikan nilai.

```
<?php
	 function Jumlahkan($x, $y){
	 $hasil = $x + $y;
	 return $hasil;
	 }
	 $bil = 0;
		 echo "Nilai bil mula-mula adalah ". $bil ."<br>";
	 $bil = Jumlahkan(3, 4);
		 echo "Nilai bil setelah memanggil function adalah " . $bil ."<br>";
?>
```

Function Jumlahkan() di atas mengembalikan nilai dari variabel $hasil yang merupakan hasil
penjumlahan dari nilai $x dan $y. Sedangkan perintah $bil = Jumlahkan(3, 4); bermakna
nilai yang dikembalikan function Jumlahkan(3, 4) disimpan pada variabel $bil (dalam hal ini
nilai $bil adalah 7).
