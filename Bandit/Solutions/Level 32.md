# Level Goal
There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.

Clone the repository and find the password for the next level.

# Commands you may need to solve this level
git

# Solusi
setelah kita clone repo, kita coba cetak ***README.md*** didapatkan
```
bandit31@bandit:/tmp/bandi31/repo$ cat README.md
This time your task is to push a file to the remote repository.

Details:
    File name: key.txt
    Content: 'May I come in?'
    Branch: master
```
untuk mendapatkan password, kita buat file ***key.txt*** isinya yaitu ***May I come in?*** pada branch ***master***
```
bandit31@bandit:/tmp/bandi31/repo$ nano key.txt
bandit31@bandit:/tmp/bandi31/repo$ git add -f 'key.txt'
bandit31@bandit:/tmp/bandi31/repo$ git commit -m "update key.txt"
bandit31@bandit:/tmp/bandi31/repo$ git push
.
.
.
Total 6 (delta 1), reused 0 (delta 0)
remote: ### Attempting to validate files... ####
remote: 
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote: 
remote: Well done! Here is the password for the next level:
remote: 56a9bf19c63d650ce78e6ec0354ee45e
remote: 
.
.
.
```
maka didapatkan password.
<details>
<summary>Password</summary>
56a9bf19c63d650ce78e6ec0354ee45e
</details>