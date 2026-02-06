# Installing Arch/Hyprland with CachyOS repos and kernels

## Archinstall walkthrough
- Run `loadkeys fr` to switch keyboard layout
- In archinstall, follow these steps:
  - In `Locales` change keyboard layout to fr
  - In `Mirrors and repositories` set region to France
  - In `Disk configuration` use best effort partitioning with BTRFS
  - In `Authentication` set root password and create a user with sudo privilegies
  - In `Profile` select desktop => hyprland, Graphics driver => Nvidia (proprietary)
  - In `Applications` enable bluetooth and select pipewire as audio server
  - In `Network configuration` select Network Manager (default backend)
  - In `Additional packages` get git, neovim, firefox and base-devel
  - In `Timezone` select Paris
  - Hit install
- Reboot
- In `.config/hypr/hyprland.conf` change keyboard layout to fr

## CachyOS convertion
- Add the repos:
    - `curl https://mirror.cachyos.org/cachyos-repo.tar.xz -o cachyos-repo.tar.xz`
    - `tar xvf cachyos-repo.tar.xz`
    - `cd cachyos-repo`
    - `sudo ./cachyos-repo.sh`
- Install the kernels and create bootloader entry
    - `sudo pacman -S linux-cachyos linux-cachyos-headers nvidia-dkms`
    - `cd /boot/loader/entries`
    - Copy the existing entry into `cachyos.conf`
    - Modify the new entry:

      ```
      title Arch Linux (cachyos)
      linux /vmlinuz-linux-cachyos
      initrd /initramfs-linux-cachyos.img
      options root=UUID=... (LEAVE THIS ALONE)
      ```

## Configure the system
- Install the necessary tools:
    - First, install paru with `sudo pacman -S paru`
    - Then, use it to install the necessary tools: `paru -S ghostty mako swww waybar network-manager-applet blueman fastfetch ttf-jetbrains-mono-nerd rofi-wayland`
- Copy the content of `.config` into the corresponding files
- Set universal dark themes:
    - Install required packages with `sudo pacman -S gnome-themes-extra qt5ct qt6ct adwaita-qt5 adwaita-qt6`
    - Set cholor scheme `gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark' && gsettings set org.gnome.desktop.interface gtk-theme 'Adwaita-dark'`
    - Run `qt5ct` to configure Qt apps
