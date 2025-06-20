# Level 12 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit11@bandit.labs.overthewire.org -p 2220
   ```

2.

**send output of data.txt to tr translate command with first string showing initial alphabet character set, second string showing shifted character set. Both for uppercase and lower case**

Initial solution

```bash
 cat data.txt | tr ABCDEFGHIJKLMNOPQRSTUVWXYZ NOPQRSTUVWXYZABCDEFGHIJKLM | tr abcdefghijklmnopqrstuvwxyz nopqrstuvwxyzabcdefghijklm

```

Improved solution using character ranges

```bash
 cat data.txt | tr 'A-Ma-mN-Zn-z' 'N-Zn-zA-Ma-m'
```

## Password

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
