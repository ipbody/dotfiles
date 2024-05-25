# Ipbody dotfiles
This repo holds the dotfiles to install hyprland on arch

## Installation
1. Start with a fresh install of arch linux.
2. Use chezmoi to clone the repo :
    ```
    cd $HOME
    chezmoi init git@github.com:ipbody/dotfiles.git
    chezmoi cd
    ```
5. Install all packages from the lists:
    ```
    grep -v "#" package_list.txt | sudo pacman -S --needed -
    grep -v "#" package_list_aur.txt | paru -S --needed -
    ```
6. Install fonts
    ```
    grep -v "#" fonts_list.txt | paru -S --needed -
    ```
7. Use `chezmoi` to set dotfiles:
    ```
   chezmoi apply
    ```
 
