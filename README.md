# Intro

Test loading order for Vim plugins

## Vim scripts loading order

**When Vim started**

1. .vimrc 
1. ftdetect/*.vim 
1. after/ftdetect/*.vim 
1. plugin/*.vim 
1. after/plugin/*.vim

**When `set filetype=foobar`**

1. ftplugin/foobar.vim 
1. after/ftplugin/foobar.vim 
1. indent/foobar.vim 
1. after/indent/foobar.vim 
1. syntax/foobar.vim 
1. after/syntax/foobar.vim

**When `call foo#bar#hello_world()`**

1.  autoload/foo/bar.vim

**NOTE: autoload never check after/ folders**

**When `:compiler foobar`**

1. compiler/foobar.vim
1. after/compiler/foobar.vim

**When `:colorscheme foobar`**

1. colors/foobar.vim 

**When `:colorscheme foobar` with exvim/ex_aftercolors installed**

1. colors/foobar.vim 
1. after/colors/foobar.vim
