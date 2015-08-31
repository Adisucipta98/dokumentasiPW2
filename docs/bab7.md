#BAB VII. BEKERJA DENGAN FORM

Setelah kita belajar dasar-dasar perintah PHP, sekarang saatnya mengaplikasikannya pada
aplikasi web. Biasanya PHP digunakan sebagai pengolah data yang diinputkan melalui form yang
dibuat dengan HTML. Sebagai contoh, andaikan Anda memiliki toko virtual dalam web yang
menjual alat-alat tulis seperti pensil, buku tulis, dan ballpoint. Berikut ini adalah salah satu bentuk
kode HTML yang digunakan untuk membuat form pemesanan pembelian barang-barang
tersebut.

```
<html>
	 <body>
	 <h2>Toko Alat Tulis Amalia</h2>
		 <form action="proses.php" method="post">
			 <select name="barangpesanan">
				 <option>Pensil</option>
				 <option>Buku Tulis</option>
				 <option>Ballpoint</option>
			 </select>
```

Jumlah pesanan: 

```
			 <input name="jumlah" type="text">
			 <input type="submit" value="Submit">
		 </form>
	 </body>
</html>
```

Seperti yang Anda lihat pada kode HMTL di atas, perintah action="proses.php" digunakan
untuk mengarahkan ke file PHP yang digunakan untuk memproses barang pembelian ketika
tombol submit ditekan. Dalam form yang dihasilkan dari kode di atas terdapat 2 buah komponen
input yaitu berbentuk combobox dan textbox. 

Untuk combobox, diberi nama “barangpesanan”
(perhatikan perintah <select name="barangpesanan">) dan textbox diberi nama “jumlah”
(perhatikan perintah <input name="jumlah" type="text">).
Penjelasan mengenai method="post" akan dijelaskan pada bab berikutnya.
Sedangkan berikut ini adalah salah satu contoh kode PHP untuk memproses input dari form di
atas. 

Kode PHP ini disimpan dengan nama proses.php.

```
<html>
	 <body>
		 <?php
			 $jumlah = $_POST['jumlah'];
			 $barangpesanan = $_POST['barangpesanan'];
				 echo "Anda memesan ". $jumlah . " " . $barangpesanan . ".<br>";
				 echo "Terima kasih atas kesediaan Anda memesan barang dari kami!";
		 ?>
	 </body>
</html>
```

Kalau Anda perhatikan, terdapat keterkaitan perintah $_POST['xxx']; dengan "xxx" pada
name = "xxx" (nama komponen input).
