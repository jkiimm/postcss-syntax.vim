# Vim Syntax File for PostCSS

Shamelessly forked from the excellent [`cakebaker/scss-syntax.vim`](https://github.com/cakebaker/scss-syntax.vim).  All credit for highlighting rules goes to that repo.

The key differences from the SCSS repo are that you no longer have to run `:set ft=scss` on every CSS file to support nested blocks, etc.

## Installation

I recommend to use a plugin manager like [Vundle](https://github.com/gmarik/vundle) for the installation.

### Vundle

Open your `~/.vimrc` file and add the following line(s):

```vim
Plugin 'JulesWang/css.vim' " only necessary if your Vim version < 7.4
Plugin 'alexlafroscia/postcss-syntax.vim'
```

Afterwards, run `:PluginInstall` in Vim.

## Configuration

Usually no configuration is necessary.

### Function names starting with a keyword

Function names starting with a keyword (e.g. `baseline-unit()`) are not highlighted correctly by default. It can be fixed by adding the following line to your `~/.vimrc` file:

```vim
autocmd FileType css set iskeyword+=-
```

Please be aware that this setting also affects the behavior of the motion keys.
