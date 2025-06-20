# Level 7 Solution

**Level Goal Description**

Goal of this level is to find password stored **somewhere on the server** and has all of the following properties:

owned by user bandit7,
owned by group bandit6,
33 bytes in size

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit6@bandit.labs.overthewire.org -p 2220
   ```

2. **Used find to locate the file**

   Initial solution (difficult to read, showed too many permission errors)

   ```bash
   find / -user bandit7 -group bandit6 -size 33c -ls
   ```

   Improved solution (hides permission denied errors)

   ```bash
   find / 2>/dev/null -user bandit7 -group bandit6 -size 33c -ls
   ```

3. **gives location at /var/lib/dpkg/info/bandit7.password so cd into root and use cat to display contents of that file **

   ```bash
   cd /
   ls -al
   cat /var/lib/dpkg/info/bandit7.password
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

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
