# Level 20 Solution

**Level Goal Description**

The password for the next level is stored in a file `/etc/bandit_pass/bandit20`. However, you are **not** able to read the file directly as the current user (`bandit19`). Instead, you are provided with a special program `bandit20-do` that allows executing commands as `bandit20`.

## Commands used

Login to bandit19

```bash
ssh bandit19@bandit.labs.overthewire.org -p 2220"
```

```bash
./bandit20-do
```

run cat command to view the password in file /etc/bandit_pass/bandit20

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Password

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
