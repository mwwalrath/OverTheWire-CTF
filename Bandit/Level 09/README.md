# Bandit Level 9 → Level 10

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit9

**Password:** UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

```
ssh -p 2220 bandit9@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Commands Used

ls - list directory contents

strings - print the strings of printable characters in files.

grep - print lines matching a pattern

## Solution

```
bandit8@bandit:~$ ls
data.txt
```
```
bandit9@bandit:~$ strings data.txt | grep ===
========== the*2i"4
========== password
Z)========== is
&========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```
