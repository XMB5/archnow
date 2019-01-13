# Archnow
Archnow aims to be an arch linux installer as simple as the ubuntu installer.
It asks 4 questions:
- which drive to install arch on
- a hostname
- a username
- a password.

## Features
- btrfs file system
- automatically finds the fastest arch mirrors with [reflector](https://wiki.archlinux.org/index.php/reflector)
- installs core linux and development tools
- installs [yay](https://aur.archlinux.org/packages/yay/), an AUR helper
- configures [zsh](https://wiki.archlinux.org/index.php/zsh) with the [grml zsh config](https://www.archlinux.org/packages/extra/any/grml-zsh-config/) and sets it as the default shell
- enables openssh server
- ejects the CD and reboots after installing
- includes a script to secure the server from SSH password brute-forces

## Caveats
- designed to work in VirtualBox only
  - it won't work on a real machine
- requires an internet connection

## How to use
1. Boot arch linux off of the official ISO, found [here](https://www.archlinux.org/download/).
2. In the terminal, run `wget https://xmb5.github.io/archnow/get -O- | sh`
3. Answer the questions
4. Wait for arch to install
5. From your computer, run `ssh-copy-id user@server-ip` (replacing user and server IP respectively) and enter your password
6. SSH into the server and run `ssh-secure`, which disables password authentication over SSH

## Credits
Archnow is based off of [archfi](https://github.com/MatMoul/archfi).

## License
Archnow is released under [the GPLv3](LICENSE.md).