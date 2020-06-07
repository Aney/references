# Vim Reference

This is intended as a brief reference for beginners.

Vim does have a built in reference for each key, that can be accessed via

    :h <key>

# Basics

## Inserting Text

`i` - Insert Text at the cursor

`a` - Append Text after the cursor

`I` - Insert text at the beginning of the line

`A` - Insert text at the end of the line

`o` - Insert a new line below the current line

`O` - Inserts a new line above the current line

## Saving and Quitting

`esc` - Pressing escape will put you in normal mode, then pressing `:` 
will put you into command mode 

`:w` - Write to file  
`:q` - Quit file

`Ctrl + ZZ` - Write and quit (`:wq`)  
`Ctrl + ZQ` - Force quit (`:q!`)

# Motions for Movement

Motions can also be used with other commands, such as dw to delete to next word
or while selecting a visual block.

Vim reference `:h motion.txt`

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

`f<character>` - Moves to the next occurance of that character, good for quotes

`%` - Jump to matching parenthesis, either forwards or back

# Visual Selection

Visually highlight the selection being made

`v` - Select characters

`V` - Select entire lines

`Ctrl + v` - Visual block selection

Visual mode, can also be used with motions

`vi(` - Visually select the inside of some parenthesis

`va{` - Visual select the the {} and their contents

# Deleting and Clipboard

Deleting, yanking, and pasting. Like other commands, can use motions too!

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

# Replace/Change/Substitute

## Replace

`r<character>` - Replaces the whatever is at the cursor with the character

`R` - Replace mode. This enters an insert mode that writes over everything.

## Change

The more powerful alternative of replace

`c` - Change. This will delete the selection, and put you into insert mode

Yet again, this command can make use of, and gets its power from  motions!

`cw` - Change word    
`c$` - Change contents to the end of the line    
`ci(` - Change inside ( { "

## Substitute

This is the "change and replace" of vim. It makes use of regex.

`:s/x/y` - Replace the first instance of x to y on the selected line

`:s/x/y/g` - Replace globally all instances of x to y on the current line.

`:%s/x/y/g` -  Replace all instances of x to y on each line

`:s/x/y/gc` - Replace all instances on the line, but prompt for each change

# Cool stuff

`.` - Repeats the last command. Eg. ci( will occur again

# Buffers Splits Multitasking

Vim can open numerous files/buffers at the same time.    
These can be in tab like buffers, or in a splitscreen view.

:r 
:e filename
:bn
:bp
:bd
:split 
:vs

Ctrl + ww
Ctrl + wr Switch the splits around

# Setting variables in Vim

Vim has extra features disabled by default, that can be very useful!

`:set lines` - This adds line numbers

`:syntax on` - Turns syntax highlighting on

These variables can be added into a file called ~/.vimrc to automatically run    
every time vim opens.
