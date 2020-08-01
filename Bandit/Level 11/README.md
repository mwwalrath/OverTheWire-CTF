# Bandit Level 11 → Level 12

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit11

**Password:** IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

```
ssh -p 2220 bandit11@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Commands Used

ls - list directory contents

cat - concatenate files and print on the standard output

tr - translate or delete characters

## Solution

```
bandit11@bandit:~$ ls
data.txt
```
```
cat data.txt | tr a-zA-Z n-za-mN-ZA-M
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
