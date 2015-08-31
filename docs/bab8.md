#BAB VIII. POST AND GET METHOD

Pada contoh sebelumnya (Bab 7), kita mengirim data input dari form menuju ke file PHP untuk
diproses menggunakan metode post. Selain metode tersebut, terdapat pula metode get. Lantas
perbedaannya apa? Kapan kita gunakan metode post atau get? Itulah yang akan dibahas pada
bab ini.

Untuk melihat perbedaan post dan get, kita akan sedikit mengubah file HTML form dan file
PHP proses.php sebelumnya.

```
<html>
	 <body>
		 <h2>Toko Alat Tulis Amalia</h2>
		 <form action="proses.php" method="get">
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

dan isi proses.php nya adalah

```
<html>
	 <body>
		 <?php
			 $jumlah = $_GET['jumlah'];
			 $barangpesanan = $_GET['barangpesanan'];
				 echo "Anda memesan ". $jumlah . " " . $barangpesanan . ".<br>";
				 echo "Terima kasih atas kesediaan Anda memesan barang dari kami!";
		 ?>
	 </body>
</html>
```

Perbedaan kode HTML dan PHP di atas dengan sebelumnya adalah yang dicetak merah.
Metode pengiriman data input dari form menggunakan get, dan dalam proses.php $_POST
diganti dengan $_GET.

Apabila aplikasi di atas dijalankan, maka secara sekilas hasil yang tampak sama dengan ketika
digunakan metode post. Namun, coba perhatikan URL yang tampak ketika proses.php muncul.
Pada URL tersebut terdapat tambahan ?barangpesanan=...&jumlah=... setelah nama file
(proses.php). 

Titik-titik tersebut akan diisi dengan data sesuai dengan yang diinputkan pada form.
Coba bandingkan dengan URL ketika digunakan metode post. Data isian pada form tidak
ditampilkan pada URL. Sehingga inilah perbedaan antara keduanya.

Dengan demikian, hendaknya kita jangan menggunakan metode get ketika akan memproses
data input melalui form. Bayangkan seandainya form tersebut digunakan untuk login atau untuk
keperluan yang menyangkut privasi. 

Apabila Anda gunakan metode get, maka semua input data
akan ditampilkan pada URL. Bisa-bisa password Anda akan kelihatan di URL (jika terdapat input
password ketika login).

Untuk metode get, biasanya digunakan untuk input data melalui link (bukan melalui form). Untuk
contoh aplikasinya dapat dilihat pada contoh-contoh aplikasi pada bab-bab berikutnya.
