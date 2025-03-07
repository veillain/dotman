# Dotman
**Dotman** is a very lightweight and simple Dotfile Manager for GNU/Linux operating systems. \
It uses a [single script](src/dotman), written **fully in bash**, which is auditable, requiring **no build and dependencies**. \
Dotman also inspired by **pacman** that archlinux used, which make all the command easy to remember. \
<br/>
These are the **features** dotman have for now:
| Features | Description                                                         | Status   | 
|----------|---------------------------------------------------------------------|----------|
| ```List```     | Show the list of configuration files and folder inside the dotfiles | Applied  |
| ```Sync```     | Sync/Copy the config files/folder into the dotfiles                 | Applied  |
| ```Syncall```  | Sync all the config files/folder inside the dotfiles                | Applied  |
| ```Remove```   | Remove config files/folder from dotfiles                            | Applied  |
| ```Apply```    | Apply configuration from dotfiles to local                          | Progress |
| ```Appyyall``` | Apply all configuration from dotfiles to local                      | progress |

## Overview
Dotman uses a path that you set to be the dotfiles directories. Then you can manage your configuration into/from dotfiles with simple commands.
<br/>
For example, let say you want to sync neovim configuration from ~/.config/nvim into your dotfiles which default is ~/dotfiles
```dotman sync nvim```
you can also sync bunch of configuration in one time:
```dotman sync nvim obsidian rofi foot hypr dunst```
<br/>
Then, to remove the configuration from the dotfiles:
```dotman remove nvim```
<br/>
Q: But i already sync all configuration that i want inside the dotfiles, how do i easily update it to sync with my currrent configuration?
A: You can use ```dotman syncall``` for this situation, it will update all configuration inside dotfiles to sync with your current configuration. Please be mind that it will overwrite the old configuration inside the dotfiles, deleted file will be deleted, and new file will be synced.

## Install
```
git clone https://github.com/veillain/dotman.git
cd dotman
cp -rf src/dotman /usr/bin/
```

### Archlinux? AUR!
[![dotman](https://img.shields.io/aur/version/dotman?color=1793d1&label=dotman&logo=arch-linux&style=for-the-badge)](https://aur.archlinux.org/packages/dotman/)


