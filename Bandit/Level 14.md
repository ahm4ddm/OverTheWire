# Level Goal
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

# Commands you may need to solve this level
ssh, telnet, nc, openssl, s_client, nmap

# Solusi
karena tidak ada password yang dibutuhkan dan diberi ***sshkey.private*** kita cukup masuk menggunakan ssh untuk mengakses bandit14.
```
bandit13@bandit:~$ ssh bandit14@localhost -i sshkey.private
```
lalu kita cetak password yang ada di ***/etc/bandit_pass/bandit14***
```
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
bandit14@bandit:~$ 
```
<details>
<summary>Password</summary>
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
</details>