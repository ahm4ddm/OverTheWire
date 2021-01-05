# Level Goal
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

# Commands you may need to solve this level
ssh, telnet, nc, openssl, s_client, nmap

# Solusi
kita disuruh mencari password di server menggunakan host ***localhost*** port ***31000-32000***\
kita bisa menggunakan ***nmap*** untuk mencari port yang aktif
```
bandit16@bandit:~$ nmap - A -p 31000-32000 127.0.0.1
Starting Nmap 7.40 ( https://nmap.org ) at 2021-01-05 14:01 CET
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00036s latency).
.
.
.
31790/tcp open  ssl/unknown
| fingerprint-strings: 
|   FourOhFourRequest, GenericLines, GetRequest, HTTPOptions, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq: 
|_    Wrong! Please enter the correct current password
| ssl-cert: Subject: commonName=localhost
| Subject Alternative Name: DNS:localhost
| Not valid before: 2020-12-03T12:25:02
|_Not valid after:  2021-12-03T12:25:02
|_ssl-date: TLS randomness does not represent time
.
.
.
```
nmap menampilkan beberapa port, disini saya fokus pada port ***31790*** karena ada pesan please correct password.\
lalu saya gunakan perintah ***ncat*** lalu munculah private key
```
bandit16@bandit:~$ ncat --ssl localhost 31790
cluFn7wTiGryunymYOu4RcffSxQluehd
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
.
.
.
```
lalu saya copy ssh private key setelah itu saya buat file dan set permissions menjadi r/w
```
bandit16@bandit:mkdir /tmp/solusi17
bandit16@bandit:/tmp/solusi17$ nano bandit.key
bandit16@bandit:/tmp/solusi17$ chmod 600 bandit.key
bandit16@bandit:/tmp/solusi17$ ssh -i bandit.key bandit17@localhost
```
lalu berhasil masuk ke ***bandit17***\
setelah itu saya masuk disana ada file ***passwords.new passwords.old*** setelah dicoba tidak berhasil, lalu saya lihat pada level sebelumnya yaitu 

>The password for the next level is stored in /etc/bandit_pass/bandit14

saya langsung cetak pada folder tersebut.
```
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn
```
<details>
<summary>Password</summary>
xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn
</details>