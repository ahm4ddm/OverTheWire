# Level Goal
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

# Solusi
Setelah dicek ada file ***bandit20-do*** dan file merupakan file ELF 
```
bandit20-do: setuid ELF 32-bit LSB executable
```
setelah menjalankan file tersebut ada petunjuk penggunaan
```
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
```
ternyata untuk mendapatkan password kita harus menjalankan file tersebut.
atau biasanya disebut ***setuid*** dimana pengguna diizinkan menjalankan file executable dengan file sistem hak akses.\
langsung saja lakukan cetak password sesudah kita menjalankan file tersebut
```
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```
<details>
<summary>Password</summary>
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
</details>