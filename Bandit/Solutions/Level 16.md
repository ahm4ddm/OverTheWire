# Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

# Commands you may need to solve this level
ssh, telnet, nc, openssl, s_client, nmap

# Solusi
Dari level goal diatas kita kita harus melakukan koneksi dengan menggunakan SSL encryption untuk mendapatkan password pada level berikutnya.\
kita bisa menggunakan ***ncat*** dan opsi ***--ssl*** \
berikut sintaks:
```
ncat --ssl <host> <port>
```
lalu kita masukkan password pada level sebelumnya.
```
bandit15@bandit:~$ ncat --ssl localhost 30001
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd
```
<details>
<summary>Password</summary>
cluFn7wTiGryunymYOu4RcffSxQluehd
</details>