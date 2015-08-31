# **Installasi Web Server**

####__Persiapan :__
 
* Mesin komputer yang cukup memori, ruang harddisk, dan kecepatan prosesor yang memadai.
* Aplikasi Web Server yang sudah mendukung PHP.
* Contohnya Apache.
* Komputer yang terhubung dengan internet. (Jika web site ingin diakses oleh banyak orang di internet)
* Aplikasi Database Server. (Jika web site akan menggunakan database)
* MySQL server, Ms. SQL Server, Oracle, Postgre SQL, dll.

---
	
####__Installasi Web Server__
 
* Download Aplikasi Web Server
	 1. Apache :
	 [http://httpd.apache.org/download.cgi](http://httpd.apache.org/download.cgi)
	 2. PHP
	 [http://php.net/downloads.php](http://php.net/downloads.php)
	 3. Web Server + PHP bundling
	 4. WAMP
	 [www.wampserver.com](http://www.wampserver.com)
     5. MAMP
	 [www.mamp.info](http://www.mamp.info)
	 6. XAMPP
	 [http://www.apachefriends.org/en/xampp.html](http://www.apachefriends.org/en/xampp.html)
	 
---

####__Installasi XAMPP__

* Paritisi harddisk untuk instalasi direktori XAMPP, sebaiknya berbeda partisi dengan Sistem Operasi.
	   
	 1. Misal, Sistem Windows terinstal di drive C maka install XAMPP selain di drive C.
	 2. Memudahkan memback-up data ketika terjadi crash pada sistem operasi.
		 
![Gambar](../web6.png "Gambar")

---

####__Konfigurasi Web Server__

* Uji coba apakah server sudah berkerja dengan baik
	 [http://127.0.0.1](http://127.0.0.1) atau  [http://localhost](http://localhost) .
	 Maka akan Tampil halaman utama XAMPP jika server sudah berkerja dengan baik.

* Dokumen Website
	 1. Semua file website tempatkan di direktori : 
		 \xampp\htdocs\
		 
	 2. Konfigurasi Apache
		 * Untuk konfigurasi HTTP server, seperti port yang digunakan akses HTTP, 
		 modul yang diaktifkan, lokasi document root, dll.
         \xampp\apache\conf\httpd.conf

	 3. Konfigurasi PHP
	     * Untuk konfigurasi perilaku engine PHP yang berefek pada keamanan dan performa. 
		 Seperti batas maksimal waktu eksekusi script, batas file yang dapat diupload, error reporting, dll.
	     \xampp\php\php.ini

	 4. Konfigurasi MySQL
		 * Konfigurasi server MySQL, seperti administrator user, port, timezone, dll.
	     \xampp\mysql\bin\my.ini


