### Install
[Vim-plug](https://github.com/junegunn/vim-plug)

Run this script for NeoVim Windows
```ps1
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim/autoload/plug.vim" -Force
```
>Note: Vim-plug docs point to `/nvim-data/site/autoload/plug.vim`, but changed to `/nvim/autolaod/plug.vim` to have everything in one place

Add this to `init.vim` file,
```vim
call plug#begin(stdpath('config')/autoload/plug)
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
call plug#end()
```

Test by running vim command `:Pl`, then either press `tab` or `Ctrl+d` the plug commands suggestion should appear.
