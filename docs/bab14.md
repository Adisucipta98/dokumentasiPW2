#BAB XIV. BEKERJA DENGAN COOKIES

Cookies telah lama digunakan dalam internet yang digunakan oleh administrator web untuk
menyimpan informasi user atau pengunjung di komputer user tersebut.

##Membuat Cookies

Untuk membuat cookies, caranya dengan menggunakan perintah setcookie(name, value,
expiration). Perintah ini memiliki 3 buah argumen, yaitu

* name, merupakan nama dari cookie. Nama cookie ini dapat dipanggil sewaktu-waktu untuk mendapatkan informasi. Jadi jangan sampai nama cookie ini lupa.
* value, merupakan informasi atau data yang disimpan dalam cookie. Biasanya value ini berupa username atau tanggal pengaksesan suatu halaman web.
* expiration, merupakan batas waktu penyimpanan cookie (dalam detik timestamp).

Apabila lama penyimpanan sebuah cookie melebihi batas waktu ini, maka secara
otomatis cookie tersebut akan terhapus.

Contoh:
Pada contoh ini akan dibuat perintah PHP untuk membuat cookie yang digunakan untuk
menyimpan data waktu kunjungan terakhir seorang user yang mengakses suatu halaman web.
Cookie ini diberi batas waktu sampai 2 bulan (60 hari) penyimpanan.

```
<?php
	 $duabulanlagi = time() + 60 * 24 * 3600;
	 setcookie(KunjunganTerakhir, date("G:i - m/d/y"), $duabulanlagi);
?>
```

##Mengambil Informasi dari Cookie

Apabila cookie belum terhapus, maka kita dapat mengambil informasi dari cookie. Untuk
mengecek apakah suatu cookie sudah terhapus atau belum menggunakan perintah

```
isset($_COOKIE['nama_cookie'])
```

Apabila cookie masih ada, maka perintah di atas menghasilkan TRUE. Sedangkan apabila sudah
terhapus, akan menghasilkan nilai FALSE.
Sedangkan untuk mengambil informasi dari cookie, menggunakan perintah

```
$_COOKIE['nama_cookie']
```

Contoh:
Berikut ini contoh perintah PHP untuk menampilkan tanggal kunjungan terakhir user yang
mengunjungi halaman web.

```
<?php
	 if(isset($_COOKIE['KunjunganTerakhir']))
	 {
	 $visit = $_COOKIE['KunjunganTerakhir'];
		 echo "Kunjungan Anda terakhir pada - ". $visit;
	 }
	 else
		 echo "Anda sudah 2 bulan lebih tidak mengunjungi web ini";
?>
```

