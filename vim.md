# Basics

Inserting text, saving and closing the buffer

`i` - Insert Text at the cursor
`a` - Append Text after the cursor
`I` - Insert text at the beginning of the line
`A` - Insert text at the end of the line

`:w` - Write to file
`:q` - Quit file

`Ctrl + ZZ` - Write and quit (`:wq`)
`Ctrl + ZQ` - Force quit (`:q!`)

# Movement

These can also be used with other commands, such as dw to delete to next word

# Search
`/<search>` - Search forwards
`?<search>` - Search backwards

`n` - Next search result
`N` - Previous search result

# Replace/Change

c Change
cw 
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

