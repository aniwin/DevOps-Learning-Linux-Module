to remove a directory rm -r <dir>
mv multiline_copy.txt multiline_backup.txt # mv can also be used to create a copy of file not just for moving files
cp -r my_directory my_directory_copy
#this cp -r is to create a copy of the my_directory folder
mkdir -p project/src/components /n this is to create not only project but src and components folders too

#this will list subdirectories recursively ls -R project
project:
src

project/src:
components

rmdir command can only remove empty directories

to remove all contents in directory and subdirectories then you need rmdir -r to remove recursively

so if you do rm -r project you take out all of proj src and components directories

if you want to make a directory with spacing in word do # mkdir "My Example"

also use backslash approach # mkdir My\ Example\ 2 to create folder "My Example 2"

# Sudo and Root User Notes

## Running Multiple Commands as Root

- Use `sudo su` to switch to the root user. This allows you to run multiple commands as root without needing to prepend `sudo` each time.

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
  but to access string folder names cd "My Example"
  or My\ Example \2
  ```

## Directory and File Commands

### Remove a Directory

```bash
rm -r <dir>
```

Removes a directory and its contents recursively.

### Move or Rename a File

```bash
mv multiline_copy.txt multiline_backup.txt
```

`mv` can also be used to rename files.

### Copy a Directory

```bash
cp -r my_directory my_directory_copy
```

The `-r` flag copies directories recursively.

### Create Nested Directories

```bash
mkdir -p project/src/components
```

Creates `project`, `src`, and `components` directories as needed.

### List Subdirectories Recursively

```bash
ls -R project
```

Example output:

```
project:
src

project/src:
components
```

### Remove Empty Directories

```bash
rmdir <dir>
```

`rmdir` only removes empty directories.

### Remove Directory and All Contents

```bash
rm -r <dir>
```

Removes the directory and all its subdirectories and files.

### Create Directory with Spaces

```bash
mkdir "My Example"
mkdir My\ Example\ 2
```

Both commands create directories with spaces in their names.

### Access Directory with Spaces

```bash
cd "My Example"
cd My\ Example\ 2
```

Use quotes or backslashes to handle spaces in directory names.
