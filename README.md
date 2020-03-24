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

*Install YCM*
```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
cd ~/.vim/bundle
git clone https://github.com/Valloric/YouCompleteMe.git
cd YouCompleteMe
git submodule update --init --recursive
./install.sh --all
```

with latest vim version if you face following issue:
```
Warning: Failed to set locale category LC_NUMERIC to en_CH.
Warning: Failed to set locale category LC_TIME to en_CH.
Warning: Failed to set locale category LC_COLLATE to en_CH.
Warning: Failed to set locale category LC_MONETARY to en_CH.
Warning: Failed to set locale category LC_MESSAGES to en_CH.
```

add following in you zshrc or bashrc file to solve 
```
export LC_ALL=en_US.UTF-8
```

