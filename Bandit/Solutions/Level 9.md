# Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

# Solusi
setelah saya mencoba mencetak langsung menampilkan banyak sekali text yang mirip password.\
Untuk mendapatkan password yang asli kita gunakan perintah piping ```|``` pada level sebelumnya lalu kita ```sort``` dan ```uniq```
permasalahannya masih banyak text yang bertipe password.\
setelah membaca referensi manual dari ```uniq``` ada salah satu opsi ***-u*** digunakan hanya untuk mencetak baris yang unik.\
setelah dicoba password berhasil didapatkan.
```
bandit8@bandit:~$ cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
bandit8@bandit:~$ 
```
<details>
<summary>Password</summary>
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
</details>