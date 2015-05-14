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
