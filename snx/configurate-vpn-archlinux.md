# Configure CheckPoint VPN ArchLinux

### First install this packages:

```r
sudo pacman -Sy lib32-pam lib32-libx11 lib32-gcc-libs lib32-nss nss
```

### Then install this package from AUR:

```r
yay -Sy lib32-libstdc++5
```

### Then download SNX install script:
[SNX Script](./snx_install.sh)

### Change script permission:

```r
sudo chmod +x snx_install.sh
```

### Install snx:

```r
sudo ./snx_install.sh
```

### Then connect to your VPN:

```r
snx -s [VPN IP OR NAME] -u [USERNAME]
```

If you don't want type this every time you can create an alias in your .bashrc or .zshrc:

```r
MY_VPN_USERNAME=USERNAME
MY_VPN_SERVER=SERVER_NAME_OR_IP

alias vpn='snx -s $MY_VPN_SERVER -u $MY_VPN_USERNAME'
```

### For disconnect:

```r
snx -d
```

#vpn #checkpoint #snx #archlinux

[Original Author](https://gist.github.com/FernandoLoureiroDeAraujo/def7b9cd1d404938d156aeea6867f2fb)