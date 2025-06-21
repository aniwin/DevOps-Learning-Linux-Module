# `chmod` Command in Linux

The `chmod` command allows us to change the permissions of a file or directory. Permissions can be set using **symbolic** or **numeric** (octal) representations.

---

## Symbolic vs Numeric Permissions

- **Symbolic:** Uses letters (`r`, `w`, `x`) and operators (`+`, `-`, `=`).
- **Numeric:** Uses octal numbers (e.g., `755`, `644`).

---

## Example: Converting Permissions

- `rw-----w-`
  - User: read, write
  - Group: none
  - Others: write
  - **Octal Representation:** `602`

---

## Symbolic Mode Example

```sh
chmod u+x,g+r,o-w example.txt
```

- Grants user execute permission.
- Grants group read permission.
- Removes write permission from others.

> **Tip:** In `zsh`, the file color may change after adding execute permissions. Use `ls -l` to verify.

---

## Numeric Permissions Example

- `rwxr-x---`
  - User: read, write, execute
  - Group: read, execute
  - Others: none
  - **Octal:** `750`

```sh
chmod 750 example.txt
```

---

## Grouping Permissions with Symbolic Operators

```sh
chmod ug=rw,o=r example.txt
```

- Users and groups: read and write
- Others: read only

> **Note:** Do **not** leave spaces between the comma-separated permissions, or you'll get an error!
