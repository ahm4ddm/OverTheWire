# Level Goal
The password for the next level is stored in a file called spaces in this filename located in the home directory

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
Setelah menggunakan ```ls``` ada file space. untuk menjalankannya cukup kita beri tanda petik(') atau dobel petik(").\
 setelah itu kita cek tipe file didapatkan ascii text. langsung kita cetak file untuk mendapatkan password.
 ```
 bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ file 'spaces in this filename'
spaces in this filename: ASCII text
bandit2@bandit:~$ cat 'spaces in this filename'
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
bandit2@bandit:~$ 
```
<details>
<summary>Password</summary>
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
</details>