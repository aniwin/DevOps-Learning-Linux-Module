# Environment Variables

Environment variables define the environment in which processes run.  
They affect the behavior of processes stored on your system.

## Common Environment Variables

- `$PATH` — tells the system where to look for executable files
- `$HOME` — current user's home directory
- `$USER` — current user's username
- `$SHELL` — shell program in use

## Setting Environment Variables

- Temporary setting (only for current session):

  ```bash
  export NAME=value
  ```

  Example:

  ```bash
  export JAVA_HOME=/usr/bin/java
  ```

- Check if you've set it:

  ```bash
  echo $JAVA_HOME
  ```

- Store configuration settings in environment variables.

## Setting Environment Variables Permanently

To set environment variables permanently, use the `.zshrc` or `.bashrc` file in your home directory.

- **.zshrc**  
  Located in your home directory.  
  Main config file for the Zsh shell.  
  Used for customizing the Zsh interactive shell — define aliases, set environment variables, configure the prompt, etc.

- **.bashrc**  
  Also located in your home directory.  
  Used for configuring the interactive Bash shell.  
  Set aliases, environment variables, define functions, and configure the shell prompt in this file.
