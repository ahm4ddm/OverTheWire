# Level Goal
The password for the next level is stored in the file data.txt next to the word millionth

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

# Solusi 
Setelah masuk, saya mengecek tipe file didapatkan ```data.txt: UTF-8 Unicode text```\
lalu saya cat file terdapat banyal sekali text yang mana membuat laptop tiba-tiba hang (jangan dicoba) :( \
disini kita bisa mengakali untuk mendapatkan password yaitu menggunakan perintah ```grep``` untuk mencari pola dari inputan
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep 'millionth'
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV
bandit7@bandit:~$ 
```
perintah ```|``` merupakan pipe digunakan untuk lebih dari 2 perintah.
```
Syntax :

perintah1 | perintah2 | perintah3 | .... | commandN
```

<details>
<summary>Password</summary>
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
</details>