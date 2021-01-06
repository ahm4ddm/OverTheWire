# Level Goal
There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo. The password for the user bandit27-git is the same as for the user bandit27.

Clone the repository and find the password for the next level.

# Commands you may need to solve this level
git

# Solusi
Pada level ini kita dituntut untuk bisa menggunakan git\
langsung saja, buat direktori di ***tmp*** lalu lakukan ***git clone*** untuk password memakai password level sebelumnya
```
bandit27@bandit:/tmp/bandi27$ git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
Cloning into 'repo'...
Could not create directory '/home/bandit27/.ssh'.
.
.
```
kita pindah ke direktori dan list direktori didapatkan
```
bandit27@bandit:/tmp/bandi27$ ls
repo
bandit27@bandit:/tmp/bandi27$ cd repo
bandit27@bandit:/tmp/bandi27/repo$ ls
README
``` 
langsung kita cetak file tersebut didapatkan password
```
bandit27@bandit:/tmp/bandi27/repo$ cat README
The password to the next level is: 0ef186ac70e04ea33b4c1853d2526fa2
```
<details>
<summary>Password</summary>
0ef186ac70e04ea33b4c1853d2526fa2
</details>