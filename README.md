# Dotman
**Dotman** is a very lightweight and simple Dotfile Manager for GNU/Linux operating systems.\
It uses a single script, written fully in bash, which is auditable, requiring no dependencies. \
Dotman also inspired by pacman that archlinux used, which make all the command easy to remember. \
<br/>
These are the **features** dotman have for now:
| Features | Description                                                         | Status   | 
|----------|---------------------------------------------------------------------|----------|
| List     | Show the list of configuration files and folder inside the dotfiles | Applied  |
| Sync     | Sync/Copy the config files/folder into the dotfiles                 | Applied  |
| Syncall  | Sync all the config files/folder inside the dotfiles                | Applied  |
| Remove   | Remove config files/folder from dotfiles                            | Applied  |
| Apply    | Apply configuration from dotfiles to local                          | Progress |
| Appyyall | Apply all configuration from dotfiles to local                      | progress |

## Overview
Dotman uses a path that you set to be the dotfiles directories. Then you can manage your configuration into/from dotfiles with simple command.

## Install
```
git clone https://github.com/veillain/dotman.git
cd dotman
cp -rf src/dotman /usr/bin/
```

### Archlinux? AUR!
[![dotman](https://img.shields.io/aur/version/dotman?color=1793d1&label=dotman&logo=arch-linux&style=for-the-badge)](https://aur.archlinux.org/packages/dotman/)


