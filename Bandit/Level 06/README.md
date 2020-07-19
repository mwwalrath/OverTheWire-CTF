# Bandit Level 6 → Level 7

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit6

**Password:** DXjZPULLxYr17uwoI01bNLQbtFemEgo7

```
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Commands Used

find - search for files in a directory hierarchy
- **-user _uname_** File is owned by user uname (numeric user ID allowed).
- **-group _gname_** File belongs to group gname (numeric group ID allowed).
- **-size _n[cwbkMG]_** File uses *n* units of space, rounding up.
  - *c* for bytes

cat - concatenate files and print on the standard output

## Solution

```
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
```
```
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
```
