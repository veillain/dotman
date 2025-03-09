# Dotman
**Dotman** is a very lightweight and simple Dotfile Manager for GNU/Linux operating systems. \
It uses a [single script](src/dotman), written **fully in bash**, which is auditable, requiring **no build and dependencies**. \
Dotman also inspired by **pacman** that archlinux used, which make all the command easy to remember. \
<br/>
These are the **features** dotman have for now:
| Features | Description                                                         | Status   | 
|----------|---------------------------------------------------------------------|-------|
| ```List```     | Show the list of configuration files and folder inside the dotfiles | ✅ |
| ```Sync```     | Sync/Copy the config files/folder into the dotfiles                 | ✅ |
| ```Remove```   | Remove config files/folder from dotfiles                            | ✅ |
| ```Apply```    | Apply configuration from dotfiles to local                          | ✅ |
| ```Syncall```  | Sync all the config files/folder inside the dotfiles                | ✅ |
| ```Applyall``` | Apply all the config from dotfiles into local                       | 🚧 |

## Overview
Dotman uses a path that you set to be the dotfiles directories. Then you can manage your configuration into/from dotfiles with simple commands. \
<br/>

1. Create your directory to store the dotfiles:
    ```sh
    mkdir ~/dotfiles
    ```

2. Set the directory you created to be dotman's dotfile path:
    ```sh
    dotman set ~/dotfiles
    ```

3. Add your configuration into the dotfiles
    ```sh
    dotman sync nvim
    ```

4. To remove configuration from the dotfiles:
    ```
    dotman remove nvim
    ```

5. You can run ```dotman syncall``` to sync all configuration inside dotfiles after making some change in current configuration

> [!NOTE]
> you can also sync or remove bunch of configuration in one time: ```dotman sync nvim obsidian rofi foot hypr dunst```

> [!IMPORTANT]
> dotman doesn't apply symlink way to sync. If you want to, you can use 'stow' that really perfect for it.

> [!CAUTION]
> be in mind if you do ```dotman syncall```, the configuration in the dotfiles will be overwrited with modified current configuration

## Install
Manual Installation
```
git clone https://github.com/veillain/dotman.git
cd dotman
cp -rf src/dotman /usr/bin/
```

Archlinux - AUR
```
paru -S dotman
```
[![dotman](https://img.shields.io/aur/version/dotman?color=1793d1&label=dotman&logo=arch-linux&style=for-the-badge)](https://aur.archlinux.org/packages/dotman/)

