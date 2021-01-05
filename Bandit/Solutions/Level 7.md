# Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

# Commands you may need to solve this level
ls, cd, cat, file, du, find, grep

# Solusi
Karena password disimpan di suatu tempat server kita perlu menggunakan perintah ```find``` pada level sebelumnya yaitu level 6.
```
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/root’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
.
.
.
find: ‘/var/lib/polkit-1’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/log’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
```
>/ = berati ditektori root\
>-user = namaUser\
>-group = namaGroup\

didapatkan direktori ```/var/lib/dpkg/info/bandit7.password```

lalu kita cetak didapatkan password
```
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```
<details>
<summary>Password</summary>
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
</details>