# Level Goal
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

# Commands you may need to solve this level
ls, cd, cat, file, du, find

# Solusi
Setelah masuk dan list file didapatkan banyak file **-file01-09**
level ini seperti level sebelumnya yaitu level 2.
untuk mendapatkan password kita menggunakan perintah ```cat ./-file0*``` tanda ```*``` yang berati semua file01 sampai file09.
```
bandit4@bandit:~/inhere$ ls -la
total 48
drwxr-xr-x 2 root    root    4096 May  7  2020 .
drwxr-xr-x 3 root    root    4096 May  7  2020 ..
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file00
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file01
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file02
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file03
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file04
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file05
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file06
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file07
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file08
-rw-r----- 1 bandit5 bandit4   33 May  7  2020 -file09
bandit4@bandit:~/inhere$ cat ./-file0*
�/`2ғ�%��rL~5�g��� �������p,k�;��r*��	�.!��C��J	�dx,�e�)�#��5��
                                                                       ��p��V�_���ׯ�mm������h!?��r�l$�?h�9('���!y�e�#�x�O��=��ly���~��A�f����-E�{���m�����ܗMkoReBOKuIDDepwhWk7jZC0RTdopnAYKh
�T�?�i��j��îP�F�l�n��J����{��@�e�0$�in=��_b�5FA�P7sz��gN
```
<details>
<summary>Password</summary>
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
</details>