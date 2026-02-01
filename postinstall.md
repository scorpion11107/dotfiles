# Configure monitors
- Copy content of `.config/hypr/monitors.conf` into the corresponding file

# Set firefox as main browser
- Install firefox: `sudo pacman -S firefox`
- Copy content of `.config/mimeapps.list` into the corresponding file

# Add SSH key
- Create SSH key: `ssh-keygen -t ed25519 -C "soleyannp@gmail.com"`
- Start SSH agent: `eval "$(ssh-agent -s)"`
- Add SSH key: `ssh-add ~/.ssh/id_ed25519`
- Copy SSH public key: `cat ~/.ssh/id_ed25519.pub`
- Add public key to github
