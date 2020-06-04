# Basics

Inserting text, saving and closing the buffer

`i` - Insert Text at the cursor

`a` - Append Text after the cursor

`I` - Insert text at the beginning of the line

`A` - Insert text at the end of the line

`esc` - Pressing escape will put you in normal mode, then pressing `:` 
will put you into command mode 

`:w` - Write to file  
`:q` - Quit file

`Ctrl + ZZ` - Write and quit (`:wq`)  
`Ctrl + ZQ` - Force quit (`:q!`)

# Movement

These can also be used with other commands, such as dw to delete to next word
or while selecting a visual block.

`h,l` - Left, Right  
`j,k` - Down, Up

`0` - Jump to the beginning of the line

`$` - Jump up the end of the line

`gg` - Jump to the top of the file

`G` - Jump to the bottom of the file

`:5` - Jump to line 5

`{ }` - Jump up and down paragraphs

`w` - Beginning of next word

`e` - End of next word

`b` - Beginning of last word

`5w` - Move forwards 5 words, this also works with most commands

# Deleting and Clipboard

`x` - Delete/cut character under cursor

`d` - Delete/cut selection  
`dd` - Delete the line

`d5d` - Delete 5 lines  
`d$` - Delete to end of the line

`y` - Yank/copy selection  
`yy` - Yank the line

`p` - Put/Paste at cursor  
`P` - Put/Paste after cursor

# Editor Readibility(?)

`zz` - Center the current line in the editor

`zt` - Align the current line to the top of VIM

`zb` - Align the current line to the bottom of VIM

# Search

`/<search>` - Search forwards

`?<search>` - Search backwards

`n` - Next search result

`N` - Previous search result

# Replace/Change

c Change
cw 
ci( - Change inside ( { "
:s/x/y Replace x for y on the selected line
:%s/x/y Replace x for y on each line

# Buffers Splits Multitasking
:r 
:e filename
:bn
:bp
:bd
:split 
:vs

Ctrl + ww
Ctrl + wr Switch the splits around

# Visual Selection

`v` - Select lines  
`V` - Select the current line  
`Ctrl + v` - Visual selection in characters

