# Level 18 Solution

**Level Goal Description**

Find password for next level password in passwords.new and is the only line that has been changed between passwords.old and passwords.new

## Commands used

```bash
 diff passwords.new passwords.old
```

gives output

```bash
42c42
< x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
---
> C6XNBdYOkgt5ARXESMKWWOUwBeaIQZ0Y
```

Output tells us that line 42 changed and that < operator shows line from the new password that is different and > shows the line changed in password old

## Password

x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
