After all this git stuff its time for another escape. Good luck!

# Commands you may need to solve this level
sh, man

# Solusi
Setelah login dengan ***bandit32*** didapatkan tampilan 
```
WELCOME TO THE UPPERCASE SHELL
>> id
sh: 1: ID: not found
>> sh
sh: 1: SH: not found
```
saya lakukan apapun tidak bisa :(\
lalu melihat pada literatur di internet bahwa untuk escape dari itu kita bisa menggunakan ***$0***  yang mana itu merupakan bash special parameters. [$0 ketika dijabarkan menjadi nama dari sebuah shell atau shell script](https://bash.cyberciti.biz/guide/$0) jadi kita bisa escape dari tampilan UPPERCASE SHELL tadi.\
default dari ***$0*** apabila kita tidak set maka itu menujuk ke shell.
```
$ echo $0
sh
```
langsung saja kita cetak password ***bandit33***
```
$ cat /etc/bandit_pass/bandit33
c9c3199ddf4121b10cf581a98d51caee
```
<details>
<summary>Password</summary>
c9c3199ddf4121b10cf581a98d51caee
</details>