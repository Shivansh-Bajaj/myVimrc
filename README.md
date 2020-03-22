# myVimrc

My Setup for VIM text editor.

# Steps to install 

install vundle(https://github.com/VundleVim/Vundle.vim) 
copy .vimrc
open vim run :PluginInstall 

to configure ack with grep 
```
brew install ack 
# and in vimrc file 
set grepprg=ack 
```
to configure ctags 
```
brew install ctags
which ctags
it should alias to 
`brew --prefix`/bin/ctags
or else add this to bashrc file
alias ctags="`brew --prefix`/bin/ctags"
to create tags 
ctags -R --exclude=.git --exclude=log *

in vimrc file
set tags=./tags

to search CTRL + ]
``` 



