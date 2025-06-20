# Level 14 Solution

**Level Goal Description**

Goal of this level is to find password for the next level which is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.

## Commands used

1. **Logged into Bandit Level using private ssh key from bandit13**

   ```bash
   ssh -i sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org
   ```

2. **moved into /etc/bandit_pass/ folder and viewed bandit14 file to get password**

```bash
cd /
cd /etc/bandit_pass/
cat bandit14
```

## Password

MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
