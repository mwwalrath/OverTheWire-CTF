# Bandit Level 4 → Level 5

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit 4

**Password:** pIwrPrtPN36QITSp3EQaw936yaFoFgAB

```
ssh -p 2220 bandit4@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Commands Used

ls - list directory contents

file - determine file type

cat - concatenate files and print on the standard output

## Solution

```
bandit4@bandit:~$ ls
inhere
```
```
bandit4@bandit:~$ file inhere/*
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data
```

```
bandit4@bandit:~$ cat inhere/-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```
