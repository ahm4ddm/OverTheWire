# Level Goal
The password for the next level is stored in the file data.txt, which contains base64 encoded data

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

# Solusi
Password diencode base64 kita bisa melakukan decode untuk mendapatkan password
```
bandit10@bandit:~$ file data.txt
data.txt: ASCII text
bandit10@bandit:~$ strings data.txt | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$ 
```
<details>
<summary>Password</summary>
IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
</details>