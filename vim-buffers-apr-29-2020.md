# Plugin Management with [vim-plug](https://github.com/junegunn/vim-plug)

1. Setup

```bash
cd ~/.vim/autoload
git clone https://github.com/junegunn/vim-plug
ln -s vim-plug/plug.vim
```

2. In your vimrc

```
call plug#begin()

Plug 'githubuser/githubrepo'
Plug 'anotheruser/anotherrepo'

call plug#end()
```

3. Then run in vim

* `:PlugInstall`


# Working with multiple buffers in vim

## Important Options

```
set hidden  " Allow to hide changed buffers!
set nomore  " Do not prompt for 'more' during bufdo
```

## Look at buffer help page

:h :b

## Useful commands

:e path-to-file  # open a file on disk for edit
:ls              # List all open buffers
:b str           # str can be the buffername or a substring thereof
:sb str          # Same, but split window
:bn              # Go to next buffer in list
:bp              # Go to previous buffer in list
:b#              # Go to the previously openend buffer
:bufdo cmd       # Execute command in all buffers, e.g. replace (:s)

## Useful Plugins

[BufGrep](https://github.com/vim-scripts/GrepCommands)

* `:BufGrep string`  # Grep for string in all open buffers
* `:copen` # Open list of all matches (quickfix window)
* `:cn`    # Go to next match
* `:cp`    # Go to previous match

[fswitch](https://github.com/derekwyatt/vim-fswitch)

# Window Management Minimal

* `ctrl+w h/j/k/l`     # Moving to window
* `ctrl+w q`           # Close window

# Topics for future devtools meetings

## Vim
* Window Management
* Mappings / Remappings
* Language Servers / Auto Completion
* Folding
* Yaml Linting (Ale?)
* Compiling from Vim
* Navigation: `ctrl+o` `ctrl+i` markers
* Latex Setup
* Colors / Highlighting

## Other Tools
* Tmux Basics
* ...
