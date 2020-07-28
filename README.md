# Useful-vim-commands  

Insert current date or time, in normal and insert mode respectively  
`:nnoremap <F5> "=strftime("%Y-%m-%d %H:%M")<CR>P`  
`:inoremap <F5> <C-R>=strftime("%Y-%m-%d %H:%M")<CR>`

Random useful commands  
`:set nowrap`  
`:split`  
`:vsplit`  
`:syntax on`  
`:set ignorecase`  

One place to store the map commands is the $HOME/.vimrc or $HOME/_vimrc or $VIM/_vimrc file  
`vim $HOME/.vimrc`

If command window background is dark, use this  
`:set background=dark`  

Write to file even though you forgot "sudo"  
`:w !sudo tee %`  

Resize windows automatically (center split line)  
`CTRL+w =`

Indentation  
`>>` ⁠– indents a line  
`<<` ⁠– unindents a line  
`=G` – fix indentation for rest of file  
`:set ts=4 sw=4` – set tabs to 4 spaces
  
Working with tabs  
`:tabnew` creates a new tab  
`gt` - go to next tab  
`gT` - go to previous tab  
`:tabo` - close all other tabs besides the active one  

## How to diff recovered file with original 
(from https://vi.stackexchange.com/questions/15584/how-do-you-view-the-diff-of-a-swap-file-without-quitting-vim)

from the command line open the file

    vim path/to/file

all the rest of the commands are inside of vim

recover the file 

    r

save the recovered file (if the destination file exists, then overwrite)

    :sav! ~/.recovered

open the original (not-recovered file) in a new window

    :vsplit
    ctrl-w w
    :bn
    e

now we have the recovered file on the left and the un-recovered file on the right
diff the two files

    :diffthis
    ctrl-w w
    :diffthis

now we have a diff of the two files (see man vimdiff)
resolve any conflicts (see man vimdiff for more info)
save off any changes made to the unresolved file
delete the swap file -- :!rm -v path/to/.file.swp
quit vim

    :q
