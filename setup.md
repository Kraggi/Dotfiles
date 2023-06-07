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

Alacritty
ln -s ~/Dotfiles/alacritty ~/.config/alacritty
```
#### Install Initial Programs and delete default folders to linking
```
sudo pacman -Syu
sudo pacman -S alacritty polybar neovim 
rm -fr ~/.config/i3
rm -fr ~/.config/polybar
rm -fr ~/.config/rofi
rm -fr ~/.config/alacritty
rm ~/.Xresources 
```

#### Install VPN
```
sudo pacman -Sy lib32-pam lib32-libx11 lib32-gcc-libs lib32-nss nss
yay -Sy lib32-libstdc++5
sudo ~/Dotfiles/snx/snx_install.sh
```

#### Install Font
```
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/Iosevka.zip
unzip ~/Iosevka.zip -d ~/.fonts
rm ~/Iosevka.zip
```

#### Install Discord
```
sudo pacman -S discord noto-fonts-emoji
```

#### Install Intellij Idea
```
yay -S intellij-idea-ultimate-edition intellij-idea-ultimate-edition-jre
```

#### Install Virtual Machine
```
yay -S vmware-horizon-client
```
#### Install Tools for Web Development
```
sudo pacman -S nodejs npm lazygit
sudo npm install yarn eslint typescript typescript-language-server
```
#### Create Links
```
ln -s ~/Dotfiles/.ideavimrc ~/.ideavimrc
ln -s ~/Dotfiles/.Xresources ~/.Xresources
ln -s ~/Dotfiles/i3 ~/.config/i3
ln -s ~/Dotfiles/alacritty ~/.config/alacritty
ln -s ~/Dotfiles/nvim ~/.config/nvim
ln -s ~/Dotfiles/polybar ~/.config/polybar
ln -s ~/Dotfiles/rofi ~/.config/rofi
```
