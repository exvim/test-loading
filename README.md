# Intro

Test loading order for Vim plugins

## Vim scripts loading order

### When Vim started

```
.vimrc -> ftdetect/*.vim -> after/ftdetect/*.vim -> plugin/*.vim -> after/plugin/*.vim
```

### When 'set filetype=foobar'

```
ftplugin/foobar.vim -> after/ftplugin/foobar.vim -> indent/foobar.vim -> after/indent/foobar.vim -> syntax/foobar.vim -> after/syntax/foobar.vim
```

### When 'call foo#bar#hello_world()'

```
autoload/foo/bar.vim
```

### When ':compiler foobar'

```
compiler/foobar.vim -> after/compiler/foobar.vim
```

### When ':colorscheme foobar'

```
color/foobar.vim 
```

### When ':colorscheme foobar' with exvim/ex_aftercolors installed

```
:colorscheme foobar => color/foobar.vim -> after/color/foobar.vim
```
