This is my simple dotfile backup. Back up is saved on dropbox as well.

## Installation 

first, make a dotfiles dir in your dropbox path ( ~/dropbox), move all dotfiles into that dir and soft link them to the ~ dir. 

```
cd ~/ 
mv .zshrc  ~/dropbox/dotfiles/zshrc  
ln -s ~/Users/luolei/Dropbox/dotfiles/zshrc .zshrc  
```

To restore backup, pull backup from github and soft link all dotfiles

```
git clone git@github.com:username/dotfiles.git dotfiles  
rm -rf .zshrc
ln -s dotfiles/zshrc .zshrc  
```

## To do

write a shell script to automatic the backup and restore process