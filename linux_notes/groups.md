# Linux Groups

## Viewing Groups

- View all groups on the system:
  ```bash
  cat /etc/group
  ```

## Creating a New Group

- Create a new group named `devops`:
  ```bash
  sudo groupadd devops
  ```

## Adding a User to a Group

- Add `newuser` to the `devops` group:

  ```bash
  sudo usermod -aG devops newuser
  ```

- Switch to `newuser` and confirm group membership:
  ```bash
  su - newuser
  groups
  ```

## Removing a User from a Group

- Remove `newuser` from the `devops` group:
  ```bash
  sudo gpasswd -d newuser devops
  ```

## Deleting a Group

- Delete the `devops` group:

  ```bash
  sudo groupdel devops
  ```

- Confirm deletion:
  ```bash
  grep devops /etc/group
  ```

## Users in Multiple Groups

- Users can belong to multiple groups.

- Example: Add `newuser` to both `admin` and `admin2` groups:
  ```bash
  sudo groupadd admin2
  sudo usermod -aG admin,admin2 newuser
  su - newuser
  ```
