# Level Goal
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

# Commands you may need to solve this level
ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)

# Solusi
Pada level ini localhost dijadikan connect dan listen.\
kita buat 2 terminal\
Terminal 1
```
bandit20@bandit:~$ nc -lvp 1337
listening on [any] 1337 ...
```
Terminal 2
```
bandit20@bandit:~$ ./suconnect 1337
```
lalu masukkan password level sebelumnya di terminal 1
```
bandit20@bandit:~$ nc -lvp 1337
listening on [any] 1337 ...
connect to [127.0.0.1] from localhost [127.0.0.1] 44134
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```
didapatkan password.

<details>
<summary>Password</summary>
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
</details>