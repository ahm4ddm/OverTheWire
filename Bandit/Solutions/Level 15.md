# Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

# Commands you may need to solve this level
ssh, telnet, nc, openssl, s_client, nmap

# Solusi
Kita masuk ke bandit14 cek password lalu, kita lakukan perintah ****nc*** digunakan untuk r/w data menggunakan tcp/ip atau bisa digunakan untuk membuat koneksi dengan jaringan lainnya.
```
bandit14@bandit:~$ nc localhost 30000
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
```
sintaks:
```
 nc <host> <port>
```
<details>
<summary>Password</summary>
BfMYroe26WYalil77FoDi9qh59eK5xNr
</details>