# Level Goal
There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.

Clone the repository and find the password for the next level.

# Commands you may need to solve this level
git

# Solusi
Hampir sama pada level sebelumnya, tapi permasalahan tidak ada password pada semua branch.
kita bisa menggunakan ***git-show-ref*** untuk list referensi pada lokal repo
```
andit30@bandit:/tmp/bandi30/repo$ git show-ref
3aefa229469b7ba1cc08203e5d8fa299354c496b refs/heads/master
3aefa229469b7ba1cc08203e5d8fa299354c496b refs/remotes/origin/HEAD
3aefa229469b7ba1cc08203e5d8fa299354c496b refs/remotes/origin/master
f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea refs/tags/secret
```
ada beberapa commit, kita cetak yang bawah sendiri, karena itu mencurigakan
```
bandit30@bandit:/tmp/bandi30/repo$ git show f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea
47e603bb428404d265f59c42920d81e5
```
dan itu merupakan password

<details>
<summary>Password</summary>
47e603bb428404d265f59c42920d81e5
</details>