# Vim Notes

For all the shortcuts, see [vim.rtorr.com](https://vim.rtorr.com/).

## Basic Modes

- **Insert mode:** Press `i`

## Navigation

- `h` — move left
- `j` — move down
- `k` — move up
- `l` — move right
- `Shift + 4` (`$`) — move to end of line
- `w` — move forward by a word
- `b` — move backward by a word
- `g_` — go to last non-blank character of line
- `G` — go to last line of document
- `gg` — go to first line of document
- `:<line number>` — go to a specific line

## Searching

- `/<pattern>` — search for pattern
- `n` — repeat search in same direction
- `N` — repeat search in opposite direction

## Editing

- `dd` — delete whole line
- `D` — delete from cursor to end of line
- `yy` — yank (copy) line
- `P` — paste

## Undo/Redo

- `u` — undo last change
- `Ctrl + r` — redo undone change

## Miscellaneous

- `:syntax on` — enable syntax highlighting
- `:set number` — show line numbers

## Saving and Exiting

- `:w` — save (does not exit)
- `:wq!` — force save and exit
- `:q!` — force quit and discard changes

> If you get stuck in insert mode, try `Ctrl + q`
