# Level Goal
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

# Commands you may need to solve this level
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

# Solusi
Password terencode rot13.\
inti dari encode rot13 yaitu mengganti setiap huruf ke-13 setelahnya dalam alfabet.\
kita bisa mendecode dengan menggunakan perintah ```tr``` atau bisa memakai tools online.
```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ file data.txt
data.txt: ASCII text
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
bandit11@bandit:~$ tr '[A-Za-z]' '[N-ZA-Mn-za-m]' < data.txt
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
bandit11@bandit:~$ 
```
<details>
<summary>Password</summary>
5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
</details>
