# Level 11 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the file data.txt, which contains base64 encoded data

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit10@bandit.labs.overthewire.org -p 2220
   ```

2. **send output of data.txt to the base64 command with flag -d to decode**

```bash
 cat data.txt | base64 -d
```

## Password

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
