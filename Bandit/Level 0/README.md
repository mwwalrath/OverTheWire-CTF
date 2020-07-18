# Bandit Level 0
## Level Goal
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

## References
[ssh(1) - Linux man page](https://linux.die.net/man/1/ssh)
## Solution
```
ssh -p 2220 bandit0@bandit.labs.overthewire.org
```
