ls -l # allows you to view Linux file permissions

## Understanding Linux File Permissions

File permissions determine who can read, write, and execute files in Linux.

- **Read (`r`)**: View file contents.
- **Write (`w`)**: Modify file contents.
- **Execute (`x`)**: Run the file as a program.

Permissions are assigned to three categories:

- **User**: The owner of the file.
- **Group**: A set of users with similar permissions.
- **Other**: All other users.

Permissions can be represented as:

- **String** (e.g., `rwxr-xr--`)
- **Octal** (e.g., `755`)
- **Binary**

You can use an [octal calculator](https://chmod-calc-five.vercel.app/) to quickly determine the correct octal notation.

**Useful resources:**

- [Binary to Octal Explanation (YouTube)](https://www.youtube.com/watch?v=WbTrMMTtmBM&t=151s)
- [How to Read Binary](https://www.lifewire.com/how-to-read-binary-4692830)
- [Linux File Permissions Explained (Red Hat)](https://www.redhat.com/en/blog/linux-file-permissions-explained)

### Changing Permissions

If you have a script called `set_permissions.sh` and try to run it without execute permissions (`./set_permissions.sh`), you'll get a permission denied error.

To add execute permissions for everyone:

```bash
chmod +x set_permissions.sh
```

To add execute permission for the user (owner) only:

```bash
chmod u+x example.txt
```

### Using Symbolic Operators

You can set permissions for user (`u`), group (`g`), and others (`o`) using symbolic notation:

```bash
chmod ug=rw,o=r example.txt
```

This command gives read and write permissions to the user and group, and read-only permission to others.
