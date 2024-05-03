# Ipbody dotfiles
This repo holds the dotfiles to install hyprland on arch

## Installation
1. Start with a fresh install of arch os with hyprland using archinstall.
2. Copy this repo in the HOME folder and `cd` to the dotfiles:
    ```
    cd $HOME
    git clone https://github.com/ipbody/dotfiles-cz
    cd dotfiles-cz
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
    $ sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply git@github.com:ipbody/dotfiles-cz.git
    ```
 
