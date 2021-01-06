# Level Goal
Good job getting a shell! Now hurry and grab the password for bandit27!

# Commands you may need to solve this level
ls

# Solusi 
login pada ***bandit26*** dengan resize terminal 
tekan ***v*** lalu ***:***
```
set shell=/bin/bash
```
lalu tekan ***:*** lagi
```
:shell
bandit26@bandit:~$ 
```
coba kita cat pada ***text.txt***
```
bandit26@bandit:~$ cat text.txt
  _                     _ _ _   ___   __  
 | |                   | (_) | |__ \ / /  
 | |__   __ _ _ __   __| |_| |_   ) / /_  
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \ 
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/ 
bandit26@bandit:~$ 
```
lalu kita cek file pada ***bandit27-do*** ternyata seperti level sebelumnya (setuid). 
```
bandit26@bandit:~$ ./bandit27-do
Run a command as another user.
  Example: ./bandit27-do id
```
langsung kita cat dengan menjalanakan file tersebut, didapatkan password
```
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
3ba3118a22e93127a4ed485be72ef5ea
```
<details>
<summary>Password</summary>
3ba3118a22e93127a4ed485be72ef5ea
</details>