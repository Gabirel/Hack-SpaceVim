# 在Linux上安装SpaceVim

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

## 安装依赖

### 在线安装依赖

* git: 用于下载和更新SpaceVim的插件
* lua: 用于neocomplete补全
* python2/3: 用于job特性和部分插件。推荐安装python3
* vim/gvim: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: 用于SpaceVim的插件

### 离线安装依赖

* git: 用于下载和更新SpaceVim的插件
* lua: 用于neocomplete补全
* python2/3: 用于job特性和部分插件。推荐安装python3
* vim/gvim: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: 用于SpaceVim的插件
* [Offline plugins package][plugins-download]: SpaceVim的插件
* [SpaceVim][spacevim-download]

## 开始下载

### 在线安装

#### 检查依赖

1. git --version

正确结果✅：
> git version 2.12.2

2. lua -v

正确结果✅：
> Lua 5.3.4  Copyright (C) 1994-2017 Lua.org, PUC-Rio

*注意：不同的操作系统lua执行命令也不同。例如，`lua`，`lua52`, `lua53`等。**

3. python -v

正确结果✅：
> Python 3.6.0

4. vim

正确结果✅：
> You can see vim in your terminal


**注意：你必须要通过相应的软件包管理器来安装它们。例如：**

* Debian/Ubuntu:

    > sudo apt-get install git

* Fedora:

    > sudo dnf install git

* CentOS/RedHat OS:

    > sudo yum install git

* Arch

    > sudo pacman -S git

#### 开始安装

1. 备份你自己的`vimrc`，以防你不喜欢SpaceVim。

2. 执行：`curl -sLf https://spacevim.org/install.sh | bash`

3. 在终端中执行：`vim`

**After finishing downloading plugins, you installed SpaceVim successfully!**

4. Check out whether vim has lua and python's full support, these steps are the same as [Install online](#Installl online)

5. Install fonts, download fonts **in advance**: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

### 离线安装

#### 检查依赖

以下检查项同[在线安装](#在线安装)相同，故不再赘述：

* git
* lua
* python(2/3)
* vim/gvim

#### 开始安装

该部分仍然同[在线安装](#在线安装)相同，所以不再赘述重复的部分，只在不同点详细说明：

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. 把插件离线包解压到：

> ~

dein.vim是SpaceVim的插件管理器。它会在vim启动的时候自动下载插件。所以，你得提前下载好。

**注意：你也可以下载[离线包][plugins-download]。但是我们*强烈建议*自行打包，以确保所有的插件都是最新的。**

3. 在终端中打开：vim

4. 检查vim是否有lua和python的支持，该步同[在线安装](#在线安装)相同。

5. 安装字体，请**提前**下载好： [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

在安装完字体后，状态应该就可以正常工作了。

**恭喜！离线安装已完成！**


[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[plugins-download]: https://github.com/Gabirel/Hack-SpaceVim/releases
[spacevim-download]: https://github.com/spacevim/spacevim
