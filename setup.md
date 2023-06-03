# Links setup

### Clone repository to root directory
```
cd ~/
git clone https://github.com/Kraggi/Dotfiles.git
```

### If you clone in another directory do this
Set Link to Dotfiles 
```
ln -s [Path to this git] ~/Dotfiles
```

Example:
```
ln -s ~/Projects/Dotfiles ~/Dotfiles
```

### Then set links to all necessary files
```
Neovim
ln -s ~/Dotfiles/nvim ~/.config/nvim

i3wm
ln -s ~/Dotfiles/i3 ~/.config/i3

Polybar
ln -s ~/Dotfiles/polybar ~/.config/polybar
```
