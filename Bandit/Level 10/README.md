# Bandit Level 10 → Level 11

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit10

**Password:** truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

```
ssh -p 2220 bandit10@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Commands Used

ls - list directory contents

base64 - base64 encode/decode data and print to standard output
- **-d, --decode** Decode data

## Solution

```
bandit10@bandit:~$ ls
data.txt
```
```
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
