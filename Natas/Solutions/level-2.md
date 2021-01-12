```
Username: natas2
URL:      http://natas2.natas.labs.overthewire.org
```
# Solusi
kita lihat page source didapatkan sebagai berikut:
```
<html>
..
..
There is nothing on this page
<img src="files/pixel.png">
..
..
</html>
```
coba kita lihat path pada ***files*** yaitu dengan menambahkan akhir url ***http://natas2.natas.labs.overthewire.org/files/*** didapatkan
```
Index of /files
	Name	Last modified	Size	Description
[PARENTDIR]	Parent Directory	 	-	 
	pixel.png	2016-12-15 16:07	303	 
	users.txt	2016-12-20 05:15	145	 
Apache/2.4.10 (Debian) Server at natas2.natas.labs.overthewire.org Port 80
```
kita lihat isi ***users.txt*** didapatkan password:
```
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```
### Password
sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14