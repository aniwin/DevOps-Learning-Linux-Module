# Level 10 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit9@bandit.labs.overthewire.org -p 2220
   ```

2.

Initial solution to find ===, and looking for password string, very difficult to sees

```bash
 sort data.txt | strings -s ==
```

Better solution using grep and using -e human readable string flag

```bash
 cat data.txt | strings -e s | grep ==
```

## Password

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
