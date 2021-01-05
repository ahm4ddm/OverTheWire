# Level Goal
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

# Commands you may need to solve this level
cat, grep, ls, diff

# Solusi
Saat masuk ke bandit18 disana ada file ***passwords.new dan passwords.old***\
kita bisa melakukan perbandingan pada file tersebut menggunakan ***diff***
```
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
---
> kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
```
kita coba masuk ke bandit18 menggunakan password diatas ternyata berhasil.
<details>
<summary>Password</summary>
kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
</details>
