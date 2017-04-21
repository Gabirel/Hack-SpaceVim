# Install SpaceVim on Linux

## Table of Contents

   * [Install SpaceVim on Linux](#install-spacevim-on-linux)
      * [Install prerequisites](#install-prerequisites)
         * [Install online prerequisites](#install-online-prerequisites)
         * [Install offline prerequisites](#install-offline-prerequisites)
      * [Start to install](#start-to-install)
         * [Install online](#install-online)
            * [Check prerequisites](#check-prerequisites)
            * [Start to install](#start-to-install-1)
         * [Install offline](#install-offline)
            * [Check prerequisites](#check-prerequisites-1)
            * [Start to install](#start-to-install-2)

## Install prerequisites

### Install online prerequisites

* git: For downloading and updating plugins of SpaceVim
* lua: For neocomplete
* python2/3: Support job and part of plugins. Recommend to install both
* vim/gvim: Vim's program
* [DejaVu Sans Mono for PowerLine][font-download]: Used by the plugins of SpaceVim

### Install offline prerequisites

* git: For downloading and updating plugins of SpaceVim
* lua: For neocomplete
* python2/3: Support job and part of plugins. Recommend to install both
* vim/gvim: Vim's program
* [DejaVu Sans Mono for PowerLine][font-download]: Used by the plugins of SpaceVim
* [Offline plugins package][plugins-download]: All plugins used by SpaceVim
* [SpaceVim][spacevim-download]

## Start to install

### Install online

#### Check prerequisites

1. git --version

The correct result✅：
> git version 2.12.2

2. lua -v

The correct result✅：
> Lua 5.3.4  Copyright (C) 1994-2017 Lua.org, PUC-Rio

*Notice: Different Operating system may has different names of lua. For example, `lua` or `lua53` or `lua52`.*

3. python -v

The correct result✅：
> Python 3.6.0

4. vim

The correct result✅：
> You can see vim in your terminal


**Notice: You have to install them by corresponding package manager. For expample:**

* Debian/Ubuntu:

    > sudo apt-get install git

* Fedora:

    > sudo dnf install git

* CentOS/RedHat OS:

    > sudo yum install git

* Arch

    > sudo pacman -S git

#### Start to install

1. Back up your own `.vimrc`. Just in case you don't like SpaceVim

2. Execute: `curl -sLf https://spacevim.org/install.sh | bash`

3. Launch: vim

**After finishing downloading plugins, you installed SpaceVim successfully!**

4. Check whether your vim has +Lua and +python feature. Use `vim --version | grep -E 'lua|python'` to check out:

![linux-check-lua-python][linux-check-lua-python]

**Notice: If your vim doesn't have `+lua` and `+python` support, please install vim that has them or build vim from source.**

5. Check whether your Lua and python2/3 really works by tow command: `echo has('lua')`, `echo has('python3')` and `echo has('python2')`
    * Lua returns: 1
    * Python returns: 1
    * Python3 returns: 1

**Notice: `echo has('python2') and `echo has('python3')` , both of them could return `1` instead of returning `0`.**

6. Install fonts, download fonts **in advance**: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

### Install offline

#### Check prerequisites

List is the same as [Install online: Check prerequisites](#check-prerequisites). So I won't repeat it:

* git
* lua
* python(2/3)
* vim/gvim

#### Start to install

Still this part has the same introductions in [Install online: Start to install](#start-to-install-1). I will skip the same part. Only explain at different parts.

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. Extract the package to:

> ~

dein.vim is the plugins manager of SpaceVim. It is downloaded automatically by starting vim the first time. So you have to download it in advance.

**Notice: You could download [the offline package][plugins-download]. But we HIGHLY RECOMMEND packing it up by yourself to make sure that all plugins is up-to-date to make you more powerful.**

3. Open vim in your terminal

4. Check out whether vim has lua and python's full support, these steps are the same as [Install online: Start to install](#start-to-install-1)

5. Install fonts, download fonts **in advance**: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

After finishing installing fonts, the status bar should work very well.

**Congratulations! Install offline successfully!**

------------

[Instructions for Windows](installation-for-windows.md#install-spacevim-on-windows) | [FAQ](../FAQ.md#faq) | [Index](../README.md#table-of-contents) | [中文文档](../../README_zh_CN.md#hack-spacevim)

[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[plugins-download]: https://github.com/Gabirel/Hack-SpaceVim/releases
[linux-check-lua-python]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/8bdd0d9f30a0f22e68ce8e3a2f1c2888a37c3cff/linux-check-lua-python.png
[spacevim-download]: https://github.com/spacevim/spacevim
