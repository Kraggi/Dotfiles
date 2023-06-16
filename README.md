# Links setup

### Clone repository to root directory
```bash
cd ~/
git clone https://github.com/Kraggi/Dotfiles.git
```

### If you clone in another directory do this
Set Link to Dotfiles 
```bash
ln -s [Path to this git] ~/Dotfiles
```

Example:
```bash
ln -s ~/Projects/Dotfiles ~/Dotfiles
```

### Then set links to all necessary files
```bash
ln -s ~/Dotfiles/nvim ~/.config/nvim
ln -s ~/Dotfiles/i3 ~/.config/i3
ln -s ~/Dotfiles/alacritty ~/.config/alacritty
```

#### Install Initial Programs and delete default folders to linking
```bash
sudo pacman -Syu
sudo pacman -S alacritty neovim flameshot
sudo yay -S xkblayout-state-git

rm -fr ~/.config/i3
rm -fr ~/.config/rofi
rm -fr ~/.config/alacritty
rm ~/.Xresources 
```

#### Clipboard setup
```bash
sudo pacman -S xsel
```

#### Fuzzy Finder setup
```bash
sudo pacman -S fzf
echo 'source /usr/share/fzf/key-bindings.bash' >> ~/.bashrc
echo 'source /usr/share/fzf/completion.bash' >> ~/.bashrc
```

#### Install VPN
```bash
sudo pacman -Sy lib32-pam lib32-libx11 lib32-gcc-libs lib32-nss nss
yay -Sy lib32-libstdc++5
sudo ~/Dotfiles/snx/snx_install.sh
echo 'MY_VPN_USERNAME=' >> ~/.bashrc
echo 'MY_VPN_SERVER=' >> ~/.bashrc
echo "alias vpn='snx -s $MY_VPN_SERVER -u $MY_VPN_USERNAME'" >> ~/.bashrc
```

#### Install Font
```bash
wget https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/Iosevka.zip
unzip ~/Iosevka.zip -d ~/.fonts
rm ~/Iosevka.zip
```

#### Install Discord
```bash
sudo pacman -S discord noto-fonts-emoji
```

#### Install Intellij Idea
```bash
yay -S intellij-idea-ultimate-edition intellij-idea-ultimate-edition-jre
```

#### Install Virtual Machine
```bash
yay -S vmware-horizon-client
```
#### Install Tools for Web Development
```bash
sudo pacman -S nodejs npm lazygit
sudo npm install -g yarn eslint typescript typescript-language-server
```

#### Electric Guitar setup
https://nayak.io/posts/guitar-to-linux/

#### Zsh setup
https://medium.com/tech-notes-and-geek-stuff/install-zsh-on-arch-linux-manjaro-and-make-it-your-default-shell-b0098b756a7a

#### Create Links
```bash
ln -s ~/Dotfiles/.ideavimrc ~/.ideavimrc
ln -s ~/Dotfiles/.Xresources ~/.Xresources
ln -s ~/Dotfiles/i3 ~/.config/i3
ln -s ~/Dotfiles/alacritty ~/.config/alacritty
ln -s ~/Dotfiles/nvim ~/.config/nvim
ln -s ~/Dotfiles/rofi ~/.config/rofi
```
