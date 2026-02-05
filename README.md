# Intructions to run after installing CachyOS

## Install and configure Neovim
- Install neovim with `sudo pacman -S neovim lazygit wl-clipboard`
- Run `git clone https://github.com/LazyVim/starter ~/.config/nvim && rm -rf ~/.config/nvim/.git && nvim`

## Configure terminal
- Install kitty with `sudo pacman -S kitty`
- Copy the content of `.config/kitty/kitty.conf` into the corresponding file
- Remove the `fastfetch` fish_greeting in `/usr/share/cachyos-fish-config/cachyos-config.fish`

## Add SSH key
- Create SSH key: `ssh-keygen -t ed25519 -C "soleyannp@gmail.com"`
- Start SSH agent: `eval "$(ssh-agent -s)"`
- Add SSH key: `ssh-add ~/.ssh/id_ed25519`
- Copy SSH public key: `cat ~/.ssh/id_ed25519.pub`
- Add public key to github
