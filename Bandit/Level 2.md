# Level Goal
The password for the next level is stored in a file called - located in the home directory

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
password tersimpan dalam file **-** di direktori home. ketika saya mencoba menjalakan dengan perintah ```file```
```
bandit1@bandit:~$ file -

/dev/stdin: very short file (no magic)
```
tidak menampilkan password. tapi yang menarik adalah file tersebut adalah file stdin.\
untuk mencetak file tersebut gunakan perintah ```./``` yang berati menjalankan suatu file di direktori itu sendiri.
```
bandit1@bandit:~$ file -

/dev/stdin: very short file (no magic)
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
bandit1@bandit:~$ 
```
<details>
<summary>Password</summary>
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
</details>