# PHP Intro
 
**Editor PHP**
	 **Beberapa Editor PHP :**
		
		 * Gratis
			 1. Notepad++
			 2. Eclipse
			 3. Sublime Text 2

		 * Komersial
			 1. Adobe Dreamweaver
			 2. PHPDesigner
			 3. Zend Studio
			 
---

##PHP MyInfo

	 phpinfo();
	 
---

##Penulisan PHP

**Menyisipkan script PHP pada HTML :**

* Embedded Script, Script PHP disisipkan diantara tag HTML
```php
	 <html>
	     <body>
			 <?php 
				 echo “Hello world”; 
				 print “Sedang belajar PHP”;
			 ?>
		 </body>
	 </html>
```

* Non Embedded Script
		 Dalam satu dokumen, murni script PHP.
		 Tag HTML merupakan bagian dari script PHP.
```php
	 <?php 
		 echo “<html>
			 <body>
				 Hello world
				 Sedang belajar PHP
			 </body>
		 </html>”;
	 ?>
```

---

##Komentar
		
1. Single-line Commentor
	 Gunakan karakter “//”
	 
```php 
<?php
    // This is a comment
?>
```

2. Multi-line Commentor**
     Gunakan karakter “/*” dan “*/”

```php	 
<?php
	 /*
		 This is
		 a comment block
	 */
?>
```

**Biasakan gunakan komentar untuk mendokumentasikan script-script PHP.**

---

##Escape Character

* **Daftar Esacape Carakter**

![Gambar](..\web7.png "Gambar")

		 > Contoh 1
			 Echo "Ini Contoh "Escape Character"Pada PHP";
		 > Contoh 2
			 Echo "Ini Contoh \"Escape Character\"Pada PHP";
			 Echo "Ini Contoh \x22Escape Character\x22 Pada PHP";
			 
---
			 
##Menampilkan Eror

* Lihat letak dari file php.ini dengan menggunakan [phpinfo();](phpinfo();)

![Gambar](..\web8.png "Gambar")