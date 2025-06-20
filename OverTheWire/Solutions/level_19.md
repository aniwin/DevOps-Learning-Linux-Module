# Level 19 Solution

**Level Goal Description**

Password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Commands used

Connect a secure shell connecting as bandit18 on port 2220 use -t flag to force pseudo terminal allocation to run shell immediately on login

```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 -t "/bin/sh"
```

```bash
cat readme
```

## Password

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
