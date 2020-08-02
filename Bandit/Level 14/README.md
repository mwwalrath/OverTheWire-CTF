# Bandit Level 14 → Level 15

**Hostname:** bandit.labs.overthewire.org

**Username:** bandit14

**Password:** 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

```
ssh -p 2220 bandit14@bandit.labs.overthewire.org
```

## Level Goal

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost.**

## Commands Used

telnet — user interface to the TELNET protocol

## Solution

```
bandit14@bandit:~$ telnet localhost 30000
Trying 127.0.0.1...
Connected to localhost.
Escape character is '^]'.
4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
```
