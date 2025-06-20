# Level 9 Solution

**Level Goal Description**

Goal of this level is to find password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Commands used

1. **Logged into Bandit Level using SSH**

   ```bash
   ssh bandit8@bandit.labs.overthewire.org -p 2220
   ```

2. **Used sort data by using unique to find unique lines that occur once and used -c to see number times of line occured**

   ```bash
   sort data.txt | uniq -cu
   ```

## Password

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
