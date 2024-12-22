# Setup New Personal Pop!_OS

## Update System
```bash
sudo apt update && sudo apt upgrade -y
```

## Install Ansible
```bash
sudo apt install ansible -y
```

## Download this repository
```bash
curl -L -o setup.zip https://codeload.github.com/EnochMtzR/setup/zip/refs/heads/main && unzip setup.zip -d ~/.setup && mv ~/.setup/setup-main/* ~/.setup/ && rmdir ~/.setup/setup-main && rm setup.zip
```

## Run Ansible Playbook
```bash
ansible-playbook ~/.setup/setup_linux.yml --ask-become-pass
```

## Restore terminal settings

1. Add a new Profile and name it `temp`
2. Load dconf backup
```bash
dconf load /org/gnome/terminal/legacy/profiles:/{profile_UUID}/ < ./terminal-profile.dconf
```

## Logout and back in for terminal configuration reset.
```bash
gnome-session-quit
```

