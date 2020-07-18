# Bandit Level 0 → Level 1

## Level Goal

### Part 1

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

### Part 2

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Commands Used

ssh - OpenSSH SSH client (remote login program)

ls - list directory contents

cat - concatenate files and print on the standard output

## Solution - Part 1

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit0

**Password:** bandit0

```
ssh -p 2220 bandit.labs.overthewire.org
```

## Solution - Part 2

```
bandit0@bandit:~$ ls
readme
```
```
bandit0@bandit:~$ cat readme
```
