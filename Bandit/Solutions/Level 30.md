# Level Goal
There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.

Clone the repository and find the password for the next level.

# Commands you may need to solve this level
git

# Solusi
Sama seperti level sebelumnya, tapi permasalahannya adalah tidak ada password pada commit.\
kita cek pada semua branch dengan opsi ***-a*** untuk menampilkan semua branch
```
bandit29@bandit:/tmp/bandi29/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
```
lalu coba kita ganti branch dengan menggunakan perintah ***checkout***
```
bandit29@bandit:/tmp/bandi29/repo$ git checkout remotes/origin/dev
.
.
.
```
lalu kita lihat semua log 
```
bandit29@bandit:/tmp/bandi29/repo$ git log
commit bc833286fca18a3948aec989f7025e23ffc16c07
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:52 2020 +0200

    add data needed for development

commit 8e6c203f885bd4cd77602f8b9a9ea479929ffa57
Author: Ben Dover <noone@overthewire.org>
Date:   Thu May 7 20:14:51 2020 +0200

    add gif2ascii

commit 208f463b5b3992906eabf23c562eda3277fea912
Author: Ben Dover <noone@overthewire.org>
Date:   Thu May 7 20:14:51 2020 +0200

    fix username

commit 18a6fd6d5ef7f0874bbdda2fa0d77b3b81fd63f7
Author: Ben Dover <noone@overthewire.org>
Date:   Thu May 7 20:14:51 2020 +0200

    initial commit of README.md
```
disini yang cukup menarik menurut saya yaitu ***add data needed for development*** kita coba lihat isi dari commit tersebut, maka didapatkan password
```
bandit29@bandit:/tmp/bandi29/repo$ git show bc833286fca18a3948aec989f7025e23ffc16c07
commit bc833286fca18a3948aec989f7025e23ffc16c07
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:52 2020 +0200

    add data needed for development

diff --git a/README.md b/README.md
index 1af21d3..39b87a8 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for bandit30 of bandit.
 ## credentials
 
 - username: bandit30
-- password: <no passwords in production!>
+- password: 5b90576bedb2cc04c86a9e924ce42faf
```
<details>
<summary>Password</summary>
5b90576bedb2cc04c86a9e924ce42faf
</details>