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
