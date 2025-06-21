# Sudo and Root User Notes

## Running Multiple Commands as Root

- Use `sudo su` to switch to the root user. This allows you to run multiple commands as root without needing to prepend `sudo` each time.

# set_permissions.sh Script

This script changes the permissions of `example.txt` to remove the executable permission for the user.

## Script

```bash
#!/bin/bash
# Change the permissions of example.txt to be not executable by the user
chmod u-x example.txt
echo "Permissions changed for example.txt"
```

## Usage

1. Save the script as `set_permissions.sh`.
2. Make it executable:
   ```bash
   chmod +x set_permissions.sh
   ```
3. Run the script:

## Verifying Root User

- To check which user you are currently using, run:
  ```bash
  whoami
  ```
- If you are root, the prompt will typically show `#` instead of `$`.

## Root Shell Warning

- The `#` prompt indicates you are in a root shell with unrestricted access.
- **Be careful:** Commands run as root can affect the entire system.

## Dangerous Command Example

- The following command will remove everything from the Linux file system and break your system.  
  **Never run this:**
  ```bash
  rm -rf /
  ```
- As root, the system will not prompt for confirmation.

## Sudo Log Entries

- Sudo command usage is logged in `/var/log/auth.log`.

- To view recent sudo log entries:
  ```bash
  sudo tail
  ```
