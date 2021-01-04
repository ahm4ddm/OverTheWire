# Soal
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
Ada banyak sekali direktori dan file. tidak mungkin kita cek satu persatu.
disini kita memanfaatkan peintah ```find```
pada Level Goal ada bebrapa ketentuan, kita cukup mencari berdasakan size.
setelah itu saya lihat manual page ```find``` terdapat beberapa opsi yaitu:

>-size n[cwbkMG]
              File uses less than, more than or  exactly  n  units  of  space,
              rounding up.  The following suffixes can be used:

>`b'    for  512-byte blocks (this is the default if no suffix is used)

>`c'    for bytes

>`w'    for two-byte words

>`k'    for kibibytes (KiB, units of 1024 bytes)

>`M'    for mebibytes (MiB, units of 1024 * 1024 = 1048576 bytes)

>`G'    for gibibytes (GiB,  units  of  1024  *  1024  *  1024  = 1073741824 bytes)

Karena bytes kita menggunakan **c**

```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ find -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        bandit5@bandit:~/inhere$ 
```
<details>
<summary>Password</summary>
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
</details>
