# Bandit Level 5 → Level 6

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit5

**Password:** koReBOKuIDDepwhWk7jZC0RTdopnAYKh

```
ssh -p 2220 bandit5@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Commands Used

ls - list directory contents

find - search for files in a directory hierarchy
- **-readable** Matches files which are readable.
- **-size _n[cwbkMG]_** File uses *n* units of space, rounding up.
  - *c* for bytes
- - **-executable**  Matches  files  which  are  executable.

cat - concatenate files and print on the standard output

## Solution

```
bandit5@bandit:~$ ls
inhere
```
```
bandit5@bandit:~$ find inhere/ ! -executable -readable -size 1033c
inhere/maybehere07/.file2
```
```
bandit5@bandit:~$ cat inhere/maybehere07/.file2
```
