### Using Vim
To read more about vim modes:

:h vim-modes

Enter help = :help

Esc = return to Normal mode

-------------------------

Press `i` to enter Insert mode

Press `v` to enter Visual mode

Press `:` to enter Command-line mode

---------------------------

Press `:q` to quit
Press `:w` to write (save) the file
Press `:wq` to write and exit (or "ZZ")
Press `:q!` to exit without saving changes

--------------------------

Navigation

`h` - left
`j` - down
`k` - up
`l` - right

Navigate to end of line = `$`
Navigate to beginning of line = `0`

Forward a word = `w`
Backward a word = `b`

Navigate to bottom of file = `G`
Navigate to top of file = `gg` or `1 + G`

Scroll half-page down = `Ctrl + D`
Scroll half-page up = `Ctrl + U`

Enable line numbers = `:set number`
Disable line numbers = `:set nonumber`

Go to certain line = `:<line number>`

---------------------------

Follow hyperlink = `Ctrl + ]`
Exit hyperlink = `Ctrl + T`

vim help = `man vim`

Save copy as = `:w <newfilename>`

Show command history = `q + :`, press `:q` to exit cmd history

-------------------------------

Enter Insert mode before cursor = `i`
Enter Insert mode after cursor = `a`
Insert at beginning of line = `I`
Insert at end of line = `A`

Insert new line below = `o`
Insert new line above = `O`
Delete character = `x`
Delete line = `dd`

-----------------------------
Multiple/Combination Commands

to delete two lines = `2dd` and so forth
to delete 5 characters = `5x` and so forth
to delete from cursor to end of file = `dG`
to delete from cursor to end of line = `d$`
to delete from cursor to beginning of file = `dgg`

------------------------------

copy text = `y` (yank)
cut text = `c` (cut)
paste text (from Normal mode) = `p`
delete highlighted text = `d` (delete)
copy entire line (from Normal mode) = `yy`

---------------------------------

Undo = `u`
Redo = `Ctrl + R`

Turn off auto-indent = `:set paste`
Turn on auto-indent = `:set nopaste`

Repeat last change = `.`

Search = `/<searchterm>` (search is case-sensistive)
Next item in search = `n`
Previous item in search = `N`
For case-insensitive search = `/<searchterm>\c` or `/\c<searchterm>`

Search backwards = `?<searchterm>`
Go to previous term = `n`
Go to next item = `N`

Search and replace = `:%s/replaceme/withme/g` (g replaces all occurences without prompting)
(If you don't have "g", it will only replace the 1st occurrence on ea. line)

Search and replace with prompt = `:%s/replaceme/withme/gc` (prompts by each term)

--------------------------
Extensions

Vimdiff
Useful for viewing differences between two files.
Open files:
`vimdiff <file1> <file2>` OR
`vim -d <file1> <file2>`
(file1 will be on left and file2 on right)
**COLORS**
- Purple = differing line
- Red = differing chars. in the differing line
- Blue = new block
- Teal = missing block

`Ctrl + W` (twice) switches between windows
Go to next difference = `]c`
Go to prev. difference = `[c`
Put highlighted changes into other file = `dp`
Pull highlighted changes from other file = `do`
Rescan files for changes = `:diffupdate`
