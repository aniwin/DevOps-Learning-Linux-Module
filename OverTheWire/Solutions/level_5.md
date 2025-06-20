# Level 4 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the only human-readable file in the inhere directory

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit4@bandit.labs.overthewire.org -p 2220
   ```

2. **Used cd to enter into inhere directory**

   ```bash
   cd inhere
   ```

3. **Used command below to run file on every file in or below current directory**

   ```bash
   find . -type f -exec file '{}' \;
   ```

   This showed ./-file07: ASCII text to be the only human readable file in directory

4. **used cat followed by -- so that it treats -file07 as a filename**

   ```bash
   cat -- -file07
   ```

## Password

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
