#BAB XV. PHP- MySQL

MySQL merupakan salah satu DBMS open source yang paling populer pada saat ini. Meskipun
dahulu MySQL pernah dikritisi karena tidak memiliki beberapa fitur yang ada dalam DBMS pada
umumnya, namun saat ini MySQL sudah banyak dikembangkan.

##Koneksi PHP ke MySQL

Sebelum kita melakukan koneksi ke MySQL ada beberapa parameter yang harus kita ketahui
terlebih dahulu. Untuk melakukan koneksi, dibutuhkan:

* Server name, merupakan nama server atau no. IP server dimana MySQL tersebut diinstall
* Username, merupakan nama user yang diberikan wewenang untuk mengakses database dalam MySQL
* Password, merupakan password yang dimiliki username dalam rangka autentifikasi.
* Database name, merupakan nama database dalam MySQL yang ingin kita akses.

Untuk memperoleh informasi parameter di atas, dapat menghubungi server administrator.
Sedangkan perintah PHP untuk melakukan koneksi ke MySQL adalah

```
<?php
	 mysql_connect("nama server", "username", "password") or
	 die(mysql_error());
		 echo "Koneksi ke MySQL Sukses<br>";
?>
```

Perintah di atas akan menampilkan Koneksi ke MySQL sukses apabila koneksi telah berhasil,
sedangkan apabila gagal akan menampilkan pesan kesalahan.

##Memilih Database

Setelah koneksi berhasil, selanjutnya kita dapat memilih database yang kita inginkan. Adapun
perintahnya menggunakan mysql_select_db().

Contoh:

```
<?php
	 mysql_connect("localhost", "admin", "1admin") or die(mysql_error());
		 echo "Connected to MySQL<br />";
	 mysql_select_db("test") or die(mysql_error());
		 echo "Connected to Database";
?>
```

Contoh di atas menggambarkan bagaimana cara melakukan koneksi ke MySQL dengan nama
servernya localhost, username : admin, dan password: 1admin. Selanjutnya memilih
database test.

##Memberikan Query ke MySQL

Setelah kita memilih database dimana kita akan bekerja, selanjutnya kita dapat memberikan
perintah query seperti SELECT, DELETE, CREATE, UPDATE. Berikut ini contoh script PHP
untuk membuat tabel example dalam database test.

```
<?php
	 mysql_connect("localhost", "admin", "1admin") or die(mysql_error());
	 mysql_select_db("test") or die(mysql_error());
	 mysql_query("CREATE TABLE example(
	 id INT NOT NULL AUTO_INCREMENT,
		 nama VARCHAR(30),
		 umur INT)
	 PRIMARY KEY(id)")
	 or die(mysql_error());
		 echo "Tabel sudah dibuat";
?>
```

Pada contoh di atas, dapat dilihat bahwa perintah PHP untuk menuliskan query ke MySQL
adalah

```
mysql_query("query");
```

Sedangkan berikut ini contoh script untuk menyisipkan 2 buah record/data ke tabel example.

```
<?php
	 mysql_connect("localhost", "admin", "1admin") or die(mysql_error());
	 mysql_select_db("test") or die(mysql_error());
	 mysql_query("INSERT INTO example(nama, umur)
		 VALUES('budiman', 20)");
	 mysql_query("INSERT INTO example(nama, umur)
		 VALUES('surti', 30)");
			 echo "Data sudah dimasukkan";
?>
```

##Mengambil Data dari MySQL

Mengambil data di sini terkait dengan penggunaan query SELECT. Berikut ini contoh untuk
menampilkan record pertama dari tabel example.

```
<?php
	 mysql_connect("localhost", "admin", "1admin") or die(mysql_error());
	 mysql_select_db("test") or die(mysql_error());
	 $result = mysql_query("SELECT * FROM example")
	 or die(mysql_error());
		 // menyimpan record ke dalam variabel $data
	 $record = mysql_fetch_array( $result );
		 // menampilkan data dari $record untuk setiap field
		 echo "Namanya: ".$record['nama']. "<br>";
		 echo "Umurnya: ".$record['umur'];
?>
```

Output script di atas adalah:

```
Namanya: budiman
Umurnya: 20
```

Perintah di atas hanya akan menampilkan record pertama dari tabel example. Lantas,
bagaimana caranya untuk menampilkan record yang lebih dari satu?
Untuk menampilkan record yang lebih dari satu, kita gunakan looping. Perhatikan contoh berikut
ini.

```
<?php
	 mysql_connect("localhost", "admin", "1admin") or die(mysql_error());
	 mysql_select_db("test") or die(mysql_error());
	 $hasil = mysql_query("SELECT * FROM example")
	 or die(mysql_error());
	 while ($record = mysql_fetch_array($hasil))
	 {
		 echo "Namanya: ".$record['nama']. "<br>";
		 echo "Umurnya: ".$record['umur']. "<br><br>";
	 }
?>
```

Looping while di atas akan terus berjalan selama record masih ada untuk dibaca. Hasil dari script
di atas adalah

```
Namanya: budiman
Umurnya: 20
Namanya: surti
Umurnya: 30
Catatan:
```

Untuk lebih memudahkan Anda dalam administrasi dan mengatur database dalam MySQL,
sangat dianjurkan untuk menginstall phpMyAdmin yang dapat diunduh melalui situs resminya di
[http://phpmyadmin.sourceforge.net/](http://phpmyadmin.sourceforge.net/"http://phpmyadmin.sourceforge.net/")

