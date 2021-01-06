# Level Goal
There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.

Clone the repository and find the password for the next level.

# Commands you may need to solve this level
git

# Solusi
Hampir mirip seperti level sebelumnya, tapi pada level ini password tidak ditampilkan 
```
bandit28@bandit:/tmp/bandi28/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx
```
kita bisa cek history dengan perintah ***git log***
```
bandit28@bandit:/tmp/bandi28/repo$ git log
commit edd935d60906b33f0619605abd1689808ccdd5ee
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:49 2020 +0200

    fix info leak

commit c086d11a00c0648d095d04c089786efef5e01264
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:49 2020 +0200

    add missing data

commit de2ebe2d5fd1598cd547f4d56247e053be3fdc38
Author: Ben Dover <noone@overthewire.org>
Date:   Thu May 7 20:14:49 2020 +0200

    initial commit of README.md
```
ada beberapa log, disini menurut saya yang mencurigakan adalah ***add missing data***\
langsung saja kita lihat isi commit tersebut dengan perintah 
```
git show <commit>
```
didapatkan password
```
bandit28@bandit:/tmp/bandi28/repo$ git show c086d11a00c0648d095d04c089786efef5e01264
commit c086d11a00c0648d095d04c089786efef5e01264
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:49 2020 +0200

    add missing data

diff --git a/README.md b/README.md
index 7ba2d2f..3f7cee8 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials
 
 - username: bandit29
-- password: <TBD>
+- password: bbc96594b4e001778eee9975372716b2
```
<details>
<summary>Password</summary>
bbc96594b4e001778eee9975372716b2
</details>