# Level 6 Solution

**Level Goal Description**

Goal of this level is to find password stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit5@bandit.labs.overthewire.org -p 2220
   ```

2. **Used ls to list contents of home directory**

   ```bash
   ls
   ```

3. **cd to change into inhere directory**

   ```bash
   cd inhere
   ```

4. **used find to lcate file size of 1033 bytes that isn't executable**

   ```bash
   find -type f -size 1033c -not -executable
   ```

   or

   ```bash
   find -type f -size 1033c ! -executable
   ```

## Password

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
