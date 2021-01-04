# Level Goal
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
Dari level goal diatas password disimpan dalam direktori home serta nama file **readme**.
Setelah berhasil mengkoneksikan, kita cek menggunakan ```pwd``` untuk melihat dimana kita berada lalu ```ls``` untuk melihat list direktori maupun file serta terakhir kita ```cat``` untuk mencetak isi file dalam kasus ini yaitu mencetak password.

```
bandit0@bandit:~$ pwd
/home/bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
bandit0@bandit:~$
```
<details>
<summary>Password</summary>
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
</details>