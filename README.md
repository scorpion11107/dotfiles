# Intructions to run after installing CachyOS

## Install and configure Neovim
- Install neovim with `sudo pacman -S neovim`
- 

## Configure terminal
- Copy the contents of `.config/alacritty/alacritty.toml` into the corresponding file
- Copy the contents of `.config/fish` into the corresponding file

## Add SSH key
- Create SSH key: `ssh-keygen -t ed25519 -C "soleyannp@gmail.com"`
- Start SSH agent: `eval "$(ssh-agent -s)"`
- Add SSH key: `ssh-add ~/.ssh/id_ed25519`
- Copy SSH public key: `cat ~/.ssh/id_ed25519.pub`
- Add public key to github
