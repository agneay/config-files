# config-files  [![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
my personal configuration files    

![](https://img.shields.io/badge/maintained-yes-green?style=for-the-badge)
![](https://img.shields.io/github/forks/agneay/config-files?style=for-the-badge)
![](https://img.shields.io/github/issues/agneay/config-files?style=for-the-badge)
![](https://img.shields.io/github/stars/agneay/config-files?style=for-the-badge)
![](https://img.shields.io/github/license/agneay/config-files?style=for-the-badge)


## Icon Themes:

- The icon theme I use ![Candy Icon Theme](https://github.com/EliverLara/candy-icons?tab=readme-ov-file)
- The ones I recommend
- ![Ubuntu yaru Theme](https://github.com/ubuntu/yaru)
- ![Windows Icon Theme](https://github.com/yeyushengfan258/We10X-icon-theme)
- ![MacOS Icon Theme](https://github.com/vinceliuice/WhiteSur-gtk-theme)
- ![Kora Icon Theme](https://github.com/bikass/kora)
- ![Papirus Icon Theme](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)
- ![Qogir Icon Theme](https://github.com/vinceliuice/Qogir-theme)

## /etc/issue cheatsheet

The /etc/issue is a text file which contains a message or system identification to be printed before the login prompt. It may contain various `@char` and `\char` sequences, if supported by getty.
-  `\b` : Insert the baudrate of the current line.
- `\d` : Insert the current date.
- `\s` : Insert the system name, the name of the operating system.
- `\l` : Insert the name of the current tty line.
-  `\m` : Insert the architecture identifier of the machine, eg. i486
- `\n` : Insert the nodename of the machine, also known as the hostname.
- `\o` : Insert the domainname of the machine.
- `\r` : Insert the release number of the OS, eg. 1.1.9.
- `\t` : Insert the current time.
- `\u` : Insert the number of current users logged in.
- `\U` : Insert the string “1 user” or “ users” where is the number of current users logged in.
- `\v` : Insert the version of the OS, eg. the build-date etc

## Aliases I use for my `.bashrc` file

```
# -----------------------------------------------------
# ALIASES
# -----------------------------------------------------

#Display ISO version and distribution information in short
alias version="sed -n 1p /etc/os-release && sed -n 11p /etc/os-release && sed -n 12p /etc/os-release"

#Pacman Shortcuts
alias sync="sudo pacman -Syyy"
alias install="sudo pacman -S"
alias update="sudo pacman -Syyu"
alias search="sudo pacman -Ss"
alias search-local="sudo pacman -Qs"
alias pkg-info="sudo pacman -Qi"
alias local-install="sudo pacman -U"
alias clr-cache="sudo pacman -Scc"
alias unlock="sudo rm /var/lib/pacman/db.lck"
alias remove="sudo pacman -R"
alias autoremove="sudo pacman -Rns"

alias c='clear'
alias nf='fastfetch'
alias pf='fastfetch'
alias ff='fastfetch'
alias ls='eza -a --icons'
alias ll='eza -al --icons'
alias lt='eza -a --tree --level=1 --icons'
alias shutdown='systemctl poweroff'
alias v='$EDITOR'
alias vim='$EDITOR'
alias ts='~/dotfiles/scripts/snapshot.sh'
alias wifi='nmtui'
alias dot="cd ~/dotfiles"
alias cleanup='~/dotfiles/scripts/cleanup.sh'

# -----------------------------------------------------
# ML4W Apps
# -----------------------------------------------------
alias ml4w='~/dotfiles/apps/ML4W_Welcome-x86_64.AppImage'
alias ml4w-settings='~/dotfiles/apps/ML4W_Dotfiles_Settings-x86_64.AppImage'
alias ml4w-sidebar='~/dotfiles/eww/ml4w-sidebar/launch.sh'
alias ml4w-hyprland='~/dotfiles/apps/ML4W_Hyprland_Settings-x86_64.AppImage'
alias ml4w-diagnosis='~/dotfiles/hypr/scripts/diagnosis.sh'
alias ml4w-hyprland-diagnosis='~/dotfiles/hypr/scripts/diagnosis.sh'
alias ml4w-qtile-diagnosis='~/dotfiles/qtile/scripts/diagnosis.sh'
alias ml4w-update='~/dotfiles/update.sh'

# -----------------------------------------------------
# Window Managers
# -----------------------------------------------------

alias Qtile='startx'
# Hyprland with Hyprland

# -----------------------------------------------------
# GIT
# -----------------------------------------------------
alias gs="git status"
alias ga="git add"
alias gc="git commit -m"
alias gp="git push"
alias gpl="git pull"
alias gst="git stash"
alias gsp="git stash; git pull"
alias gcheck="git checkout"
alias gcredential="git config credential.helper store"

# -----------------------------------------------------
# SCRIPTS
# -----------------------------------------------------
alias ascii='~/dotfiles/scripts/figlet.sh'

# -----------------------------------------------------
# SYSTEM
# -----------------------------------------------------
alias update-grub='sudo grub-mkconfig -o /boot/grub/grub.cfg'

# -----------------------------------------------------
# QTILE
# -----------------------------------------------------
alias res1='xrandr --output DisplayPort-0 --mode 2560x1440 --rate 120'
alias res2='xrandr --output DisplayPort-0 --mode 1920x1080 --rate 120'
alias setkb='setxkbmap de;echo "Keyboard set back to de."
```
