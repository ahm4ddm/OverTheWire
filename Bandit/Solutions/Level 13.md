# Level Goal
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file

# Solusi
buat direktore baru di tmp
```
bandit12@bandit:~$ mkdir /tmp/solusi
bandit12@bandit:~$ cp data.txt /tmp/solusi
bandit12@bandit:~$ cd /tmp/solusi
bandit12@bandit:/tmp/solusi$ ls
data.txt
```
Setelah itu kita cetak didapatkan header kalau data.txt merupakan file binary.\
```
bandit12@bandit:/tmp/solusi$ cat data.txt
00000000: 1f8b 0808 0650 b45e 0203 6461 7461 322e  .....P.^..data2.
00000010: 6269 6e00 013d 02c2 fd42 5a68 3931 4159  bin..=...BZh91AY
```
kita ganti data.txt menjadi data.bin menggunakan ```xxd -r``` untuk convert file menjadi binary
```
bandit12@bandit:/tmp/solusi$ xxd -r data.txt > data.bin
bandit12@bandit:/tmp/solusi$ ls
data.bin  data.txt
bandit12@bandit:/tmp/solusi$ file data.bin
data.bin: gzip compressed data, was "data2.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
bandit12@bandit:/tmp/solusi$ 
```
didapatkan file ***gzip compressed data*** \
kita ganti dan lakukan decompress
```
bandit12@bandit:/tmp/solusi$ mv data.bin data.gz
bandit12@bandit:/tmp/solusi$ gzip -d data.gz
bandit12@bandit:/tmp/solusi$ ls
data  data.txt
bandit12@bandit:/tmp/solusi$ file data
data: bzip2 compressed data, block size = 900k
```
Ternyata didapatkan file ***bzip2 compressed data***\
kita ganti dan lakukan decompress lagi
```
bandit12@bandit:/tmp/solusi$ mv data data.bz2
bandit12@bandit:/tmp/solusi$ bzip2 -d data.bz2
bandit12@bandit:/tmp/solusi$ ls
data  data.txt
bandit12@bandit:/tmp/solusi$ file data
data: gzip compressed data, was "data4.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
Didapatkan file ***gzip compressed data*** kita ganti dan lakukan decompress lagi
```
bandit12@bandit:/tmp/solusi$ mv data data.gz
bandit12@bandit:/tmp/solusi$ gzip -d data.gz
bandit12@bandit:/tmp/solusi$ ls
data  data.txt
bandit12@bandit:/tmp/solusi$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/solusi$ 
```
didapatkan file ***POSIX tar archive***\
lalu kita decompress lagi 
```
bandit12@bandit:/tmp/solusi$ mv data data.tar
bandit12@bandit:/tmp/solusi$ tar -x -f data.tar
```
dimana: 
>-x = ekstrak file\
>-f = file

setelah kita decompress didapatkan file ***data5.bin*** tapi setelah diidentifikasi ternyata file beripe ***tar***
kita ganti dan lakukan decompress lagi.
```
bandit12@bandit:/tmp/solusi$ ls
data5.bin  data.tar  data.txt
bandit12@bandit:/tmp/solusi$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/solusi$ mv data5.bin data5.tar
bandit12@bandit:/tmp/solusi$ tar -x -f data5.tar
bandit12@bandit:/tmp/solusi$ ls
data5.tar  data6.bin  data.tar  data.txt
bandit12@bandit:/tmp/solusi$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
```
Setelah didecompress didapatkan file ***data6.bin*** yang mana setelah diidentifikasi merupakan file ***bzip2 compressed data***\
kita ganti lalu lakukan decompress
```
bandit12@bandit:/tmp/solusi$ mv data6.bin data6.bz2
bandit12@bandit:/tmp/solusi$ bzip2 -d data6.bz2
bandit12@bandit:/tmp/solusi$ ls
data5.tar  data6  data.tar  data.txt
bandit12@bandit:/tmp/solusi$ file data6
data6: POSIX tar archive (GNU)
```
Didapatkan file ***data6*** yang mana data tersebut ***POSIX tar archive***\
kita ganti lagi lalu lakukan decompress
```
bandit12@bandit:/tmp/solusi$ mv data6 data6.tar
bandit12@bandit:/tmp/solusi$ tar -x -f data6.tar
bandit12@bandit:/tmp/solusi$ ls
data5.tar  data6.tar  data8.bin  data.tar  data.txt
bandit12@bandit:/tmp/solusi$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Thu May  7 18:14:30 2020, max compression, from Unix
```
Didapatkan file ***data8.bin*** setelah dicek file tersebut ***gzip compressed data***\
kita ganti lalu lakukan decompress lagi
```
bandit12@bandit:/tmp/solusi$ mv data8.bin data8.gz
bandit12@bandit:/tmp/solusi$ gzip -d data8.gz
bandit12@bandit:/tmp/solusi$ ls
data5.tar  data6.tar  data8  data.tar  data.txt
bandit12@bandit:/tmp/solusi$ file data8
data8: ASCII text
```
didapatkan file ***data8*** setelah dicek merupakan file text. setelah saya cetak menampilkan password
```
bandit12@bandit:/tmp/solusi$ cat data8
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```
Saya menyimpulkan bahwa password dicompress sebanyak 8 kali jadi harap sabar dan teliti untuk level ini:)
<details>
<summary>Password</summary>
8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
</details>
