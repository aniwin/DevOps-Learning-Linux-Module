# Useful Aliases

Below are some helpful aliases to set in your shell configuration:

```sh
alias hello='echo "Hello World"'
alias rm='rm -i'         # Ask every time you want to delete a file
alias cp='cp -i'         # Prompt before overwriting files
alias ..='cd ..'         # Move up one directory
alias ...='cd ../..'     # Move up two directories
alias .3='cd ../../..'   # Move up three directories
alias .4='cd ../../../..' # Move up four directories

# Git Aliases
alias checkout='git checkout'
alias commit='git commit -m'
alias addall='git add .'
alias pull='git pull origin'
alias push='git push origin'
alias sha = 'git stash apply'
alias shp = 'git stash pop'
```
