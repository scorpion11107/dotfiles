# Configure system
- Copy content of `.config/hypr/monitors.conf` into the corresponding file
- Copy content of `.config/hypr/hypridle.conf` into the corresponding file
- Copy `.config/omarchy/backgrounds/nord/arch.png` into the corresponding folder
- Set power profile to `performance`

# Set firefox as main browser
- Install firefox: `sudo pacman -S firefox`
- Copy content of `.config/mimeapps.list` into the corresponding file

# Update system and install required packages
- In the `install` menu, run `Steam` and `Xbox controller`
- In the `update` menu, run `Omarchy` and `Firmware`
- Reboot

# Add SSH key
- Create SSH key: `ssh-keygen -t ed25519 -C "soleyannp@gmail.com"`
- Start SSH agent: `eval "$(ssh-agent -s)"`
- Add SSH key: `ssh-add ~/.ssh/id_ed25519`
- Copy SSH public key: `cat ~/.ssh/id_ed25519.pub`
- Add public key to github
