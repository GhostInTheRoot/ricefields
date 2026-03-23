# My Nord XFCE Rice

## Programs to install

' yay -S fish neovim brave-bin localsend telegram-desktop zapzap sublime-text-4 xournalpp xp-pen-tablet krita auto-cpufreq bat eza '

## Mega sync

Install Megasync from it's website.

' https://mega.io/desktop '

## Chaotic aur

Install chaotic aur from it's website.

' https://aur.chaotic.cx/ '

## Fonts for Rice

' yay -S ttf-jetbrains-mono-nerd '

## NVChad Edit

### Installing NVChad

' git clone https://github.com/NvChad/starter ~/.config/nvim && nvim '

All other things left untouched only minor Edit in -

~/.config/nvim/lua/chadrc.lua

' transparency = "true" '

under theme

and statusline config

' M.ui = {
    statusline = { theme = "minimal"}
} '


## Removing fish shell greeting

add this line to 

' set fish_greeting '

~/.config/fish/config.fish


## Fish Shell Alias

'
alias cat="bat --theme=base16"
alias ls='eza --icons=always --color=always -a'
alias ll='eza --icons=always --color=always -la'
alias install='sudo pacman -S'
alias search='yay -Ss'
alias pacsearch='sudo pacman -Ss'
alias update='sudo pacman -Syu'
alias upgrade='sudo pacman -Syyu'
alias yayup='yay -Syu'
alias yayupg='yay -Syyu'

,

## Themeing

' yay -S papirus-icon-theme papirus-nord nordic-theme-git chaotic-aur/bibata-cursor-theme '


## XFCE Panel

### Only clock customization needed

%a %d/%m/%Y  %I:%M %p

## XFCE Cursor 

xfconf-query --channel xsettings --property /Gtk/CursorThemeSize --set 13

## XFCE Screenshot




# AwesomeWM Rice Feat Calla Desktop

## Packages neede to install

' yay -S awesome-git xorg pipewire pipewire-pulse wireplumber brightnessctl inotify-tools picom maim papirus-icon-theme xsettingsd  network-manager-applet polkit-gnome playerctl lua-pam-git upower xclip --needed '

## Optional pakages to install 

'yay -S lollypop gvim'


## Theming 

' yay -S adw-gtk-theme chaotic-aur/bibata-cursor-theme --needed '

## Build Call for Arch

Official calla github
https://github.com/Stardust-kyun/calla.git

' git clone https://github.com/Stardust-kyun/calla.git '

cd calla

makepkg -si

# Edit calla to resolve some error 


## Bluetuth error 

' sudo systemctl enable --now bluetooth '

## picom error

Goto this file 

' sudo nano /usr/share/calla/compositor.conf '

then add this line

' backend = "glx" '

## Control Panel overlapping error 

Goto this file 

' sudo nano /usr/share/calla/desktop/theme/control/init.lua '

then add edit this line bottom = dpi(430) to bottom = dpi(360) 
