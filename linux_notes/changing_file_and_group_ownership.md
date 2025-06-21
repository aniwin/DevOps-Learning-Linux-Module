# Changing File and Group Ownership in Linux

In Linux, you can change the owner and group of files and directories using the `chown` and `chgrp` commands.

## Change File Owner

Use the `chown` command to change the owner of a file:

```bash
sudo chown newuser example.txt
```

This command changes the owner of `example.txt` to `newuser`. `sudo` is required for permission.

## Change File Group

Use the `chgrp` command to change the group of a file:

```bash
sudo chgrp admin2 example.txt
```

This command changes the group of `example.txt` to `admin2`.

## Change Owner and Group at the Same Time

You can use `chown` to change both the owner and group:

```bash
sudo chown ubuntu:admin2 example.txt
```

This sets the owner to `ubuntu` and the group to `admin2`.

## Recursively Change Ownership

To change the owner and group for a directory and all its contents, use the `-R` (recursive) option:

```bash
sudo chown -R haipa:admin2 my_directory_copy
```

This command changes the owner to `haipa` and the group to `admin2` for `my_directory_copy` and everything inside it.
