# Bandit Level 7 → Level 8

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit7

**Password:** HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

```
ssh -p 2220 bandit7@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt next to the word millionth

## Commands Used

ls - list directory contents

grep - print lines matching a pattern

## Solution

```
bandit7@bandit:~$ ls
data.txt
```
```
bandit7@bandit:~$ grep millionth data.txt
cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
