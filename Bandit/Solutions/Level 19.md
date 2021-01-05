# Level Goal
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

# Commands you may need to solve this level
ssh, ls, cat

# Solusi
Setelah login ke ke ***bandit18*** langsung keluar. kita bisa menggunakan perintah dengan memanfaatkan ssh\
sintaks:
```
ssh user@host <port> <command>
```
```
$ssh bandit18@bandit.labs.overthewire.org -p 2220 whoami
bandit18@bandit.labs.overthewire.org's password: 
bandit18
```
kita coba cek list file atau direktori
```
$ssh bandit18@bandit.labs.overthewire.org -p 2220 ls -la
bandit18@bandit.labs.overthewire.org's password: 
total 24
drwxr-xr-x  2 root     root     4096 May  7  2020 .
drwxr-xr-x 41 root     root     4096 May  7  2020 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r-----  1 bandit19 bandit18 3549 May  7  2020 .bashrc
-rw-r--r--  1 root     root      675 May 15  2017 .profile
-rw-r-----  1 bandit19 bandit18   33 May  7  2020 readme
```
langsung saja kita cetak file readme untuk mendapatkan password
```
$ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
bandit18@bandit.labs.overthewire.org's password: 
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```
<details>
<summary>Password</summary>
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
</details>