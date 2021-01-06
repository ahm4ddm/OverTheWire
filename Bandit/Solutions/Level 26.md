# Level Goal
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

# Commands you may need to solve this level
ssh, cat, more, vi, ls, id, pwd

# Solusi
diberikan file ***bandit26.sshkey***\
langsung kita koneksian tiba tiba langsung keluar 
```
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost
Connection to localhost closed.
```
kita lihat apa yang terjadi
```
bandit25@bandit:/etc$ cat /etc/passwd | grep 'bandit26'
bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext
```
kita cetak untuk informasi detail
```
bandit25@bandit:/etc$ cat /usr/bin/showtext
#!/bin/sh

export TERM=linux

more ~/text.txt
exit 0
```
kita resize pada terminal paling kecil pada saat login ke bandit26 lalu tekan ***v*** lalu tekan ***:***
```
e /etc/bandit_pass/bandit26
```
dimana ***e*** digunakan untuk edit

didapatkan password
<details>
<summary>Password</summary>
5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z
</details>