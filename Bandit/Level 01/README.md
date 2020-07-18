# Bandit Level 1 → Level 2

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit1

**Password:** boJ9jbbUNNfktd78OOpsqOltutMc3MY1

```
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in a file called - located in the home directory

## Commands Used

ls - list directory contents

cat - concatenate files and print on the standard output

## Solution

```
bandit1@bandit:~$ ls
-
```
```
bandit1@bandit:~$ cat ./-
```
