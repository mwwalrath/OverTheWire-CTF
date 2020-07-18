# Bandit Level 3 → Level 4

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit3

**Password:** UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

```
ssh -p 2220 bandit3@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored in a hidden file in the inhere directory.

## Commands Used

ls - list directory contents
- **-a, --all** do not ignore entries starting with .

cat - concatenate files and print on the standard output

## Solution
```
bandit3@bandit:~$ ls
inhere
```
```
bandit3@bandit:~$ ls -a inhere
.  ..  .hidden
```
```
bandit3@bandit:~$ cat inhere/.hidden
```
