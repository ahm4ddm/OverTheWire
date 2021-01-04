# Level Goal
The password for the next level is stored in a hidden file in the inhere directory.

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
Setelah masuk kita gunakan perintah ```ls``` untuk list direktori atau file. lalu perintah ```cd``` untuk pindah direktori.
saat kita melihat list tidak ditampilakan adanya file maupun direktori. lalu gunakan opsi ```-l``` untuk mencetak bentuk list dan ```a``` menampilkan file atau direktori tersebunyi.
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 May  7  2020 .
drwxr-xr-x 3 root    root    4096 May  7  2020 ..
-rw-r----- 1 bandit4 bandit3   33 May  7  2020 .hidden
bandit3@bandit:~/inhere$ file .hidden
.hidden: ASCII text
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
bandit3@bandit:~/inhere$ 
```
<details>
<summary> Password</summary>
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
</details>