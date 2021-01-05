# Level Goal
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

# Solusi
Karena tipe file ***data.txt*** merupakan file data jadi untuk menampilkan format untuk bisa dibaca manusia menggunakan perintah ***strings***
Pada Level Goal diatas atas petunjuk bahwa password diawali dengan karakter '=' disini kita bisa menggunakan ***grep*** untuk mendapatkan password.

```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | sort | grep '='
A=|t&E
c^ LAh=3G
=:G e
<I=zsGi
========== password
S=A.H&^
*SF=s
========== the*2i"4
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
Zdb=
Z)========== is
bandit9@bandit:~$ 

```
<details>
<summary>Password</summary>
truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
</details>