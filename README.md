# Overview

This ansible action for vim sets up vim with a plugin installer and several plugins, as well as a general config file

There are two playbooks, a `vim-playbook-dev.yml` and `vim-playbook-ops.yml`, The difference between the two is that dev.yml file includes the vim-emmet plugin, and the ops file contains a terraform syntax and linter plugin

## General Settings

In the config, there are several helpful keymappings
S = a better keymap for search and replace
jk in insert mode will exit to normal mode
E goes to end of line
B goes to beginning of line
ctrl G opens the file explorer plugin
ctrl j, k, l h navigates split windows


## Included Plugins

vim-lightline: a status bar at the bottom of the window
nerdtree: a file explorer opened with either :NERDTreeToggle or ctrl g
vim-polyglot: a syntax highlighter for many languages
gruvbox: a simple colorscheme
vim-surround: a gamechanger plugin that makes for dealing with '"(){} and many other characters much easier
vim-commentary: a plugin to visually select a block of code and hit `gc` which will comment the selection

### Plugins For Development
if the dev.yml file is run, this extension will be installed

emmet: a plugin to make writing html quick and simple, to get started type in insert mode div>a>li>em>strong.strong and then ctrl y + ,

### Plugins For Dev-Ops

vim-terraform: a plugin by hashicorp that does syntax highlighting and code validation
NOTE: this plugin requires that the terraform binary is in the system $PATH variable

### Note worthy plugin
If you really want to get into vim, a great plugin is the coc.nvim plugin, which forks vs-code plugins into vim

This plugin is a gamechanger, but because it requires vim8, python3, and nodejs and npm, it was not included in this general vim setup

However, this autocompletion plugin is the best plugin for web-developers and programmers looking for fast code editing and extensibilty, and plugins like prettier and eslint are very easily integrated
