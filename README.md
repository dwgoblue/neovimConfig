# How to install Neovim and plugins
> This note is mainly for myself in case I need to install Neovim in new machines. Current plugins are compatible with Neovim 8.

## Download the appImage of Neovim

```
$ curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
$ chmod u+x nvim.appimage
$ ./nvim.appimage
```

## Download the plugin manager vim-plug


### install vim-plug for vim
```
$ curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```
### install vim-plug for neovim

```
$ sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

## Enable vim-plug and install plugins

### configuration file for vim or neovim
```
$ touch ~/.vimrc
$ touch ~/.config/nvim/init.vim
```

### add commands in init.vim

```
" init.vim 

call plug#begin()

" List your plugins here
Plug 'tpope/vim-sensible'

call plug#end()
```

## Common commands to manage plugins
```
:PlugInstall to install plugins
:PlugUpdate  to update plugins
:PlugDiff    to review the changes from the last update
:PlugClean   to remove plugins no longer in the list
```

# Reference
1. Neovim. https://github.com/neovim/neovim/blob/master/INSTALL.md
2. vim-plug. https://github.com/junegunn/vim-plug


