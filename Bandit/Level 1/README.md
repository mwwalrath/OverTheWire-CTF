# Bandit Level 0 → Level 1

## Level Goal

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## References

[cat(1) - Linux man page](https://linux.die.net/man/1/cat)

## Solution

```
cat readme
```
