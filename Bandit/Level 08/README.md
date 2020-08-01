# Bandit Level 8 → Level 9

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit8

**Password:** cvX2JJa4CFALtqS87jk27qwqGhBM9plV

```
ssh -p 2220 bandit8@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Commands Used

ls - list directory contents

sort - sort lines of text files

uniq - report or omit repeated lines
- **-u, --unique** Only print unique lines

## Solution

```
bandit8@bandit:~$ ls
data.txt
```
```
bandit8@bandit:~$ sort data.txt | uniq -u
```
