```
Username: natas3
URL:      http://natas3.natas.labs.overthewire.org
```
# Solusi 
kita lihat page source didapatkan sebagai berikut:
```
<html>
..
..
There is nothing on this page
<!-- No more information leaks!! Not even Google will find it this time... -->
..
..
</html>
```
disini yang menarik adalah informasi tidak bisa bocor bahkan tidak bisa dicari oleh google.\
disini kita bisa menggunakan ***robot.txt*** yang mana berfungsi sebagai filter pada website.
saya menganggapnya satpam bagi website. kenapa? karena untuk memberi tahu pengunjung (robot search engine) halaman mana yang boleh dan tidak boleh dibuka oleh search engine bot.\
kita cek dengan memasukkan robots.txt pada url ***http://natas3.natas.labs.overthewire.org/robots.txt*** didapatkan:
```
User-agent: *
Disallow: /s3cr3t/
```
terlihat bahwa ada path rahasia. kita bisa melihat isinya dengan ***http://natas3.natas.labs.overthewire.org/s3cr3t/***  didapatkan:
```
Index of /s3cr3t
	Name	Last modified	Size	Description
[PARENTDIR]	Parent Directory	 	-	 
	users.txt	2016-12-20 05:15	40	 
Apache/2.4.10 (Debian) Server at natas3.natas.labs.overthewire.org Port 80
```
kita buka ***users.txt*** didaptkan password
```
natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
```
### Password
Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ