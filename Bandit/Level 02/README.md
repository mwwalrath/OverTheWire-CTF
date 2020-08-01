# Bandit Level 2 → Level 3

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit2

**Password:** CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

```
ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Commands Used

ls - list directory contents

cat - concatenate files and print on the standard output

## Solution

```
bandit2@bandit:~$ ls
spaces in this filename
```
```
bandit2@bandit:~$ cat 'spaces in this filename'
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```
