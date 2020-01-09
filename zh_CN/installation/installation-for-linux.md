# 在Linux上安装SpaceVim

## Table of Contents

   * [在Linux上安装SpaceVim](#在linux上安装spacevim)
      * [Table of Contents](#table-of-contents)
      * [安装依赖](#安装依赖)
         * [在线安装依赖](#在线安装依赖)
         * [离线安装依赖](#离线安装依赖)
      * [开始安装](#开始安装)
         * [在线安装](#在线安装)
            * [检查依赖](#检查依赖)
            * [开始安装](#开始安装-1)
         * [离线安装](#离线安装)
            * [检查依赖](#检查依赖-1)
            * [开始安装](#开始安装-2)

## 安装依赖

### 在线安装依赖

* git: 用于下载和更新SpaceVim的插件
* lua: 用于neocomplete补全
* python2/3: 用于job特性和部分插件。推荐都安装
* vim/gvim: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: 用于SpaceVim的插件

### 离线安装依赖

* git: 用于下载和更新SpaceVim的插件
* lua: 用于neocomplete补全
* python2/3: 用于job特性和部分插件。推荐都安装
* vim/gvim: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: 用于SpaceVim的插件
* [Offline plugins package][plugins-download]: SpaceVim的插件
* [SpaceVim][spacevim-download]

## 开始安装

![shocking](https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/4418cda66a8170e73b0ee8afbd4383db6be057e9/meme-shocking.jpg)

### 在线安装

#### 检查依赖

1. git --version

正确结果✅：
> git version 2.12.2

2. lua -v

正确结果✅：
> Lua 5.3.4  Copyright (C) 1994-2017 Lua.org, PUC-Rio

*注意：不同的操作系统lua执行命令也不同。例如，`lua`，`lua52`, `lua53`等。**

3. python -V

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

* CentOS/RHEL:

    > sudo yum install git

* Arch

    > sudo pacman -S git

#### 开始安装

1. 备份你自己的`vimrc`，以防你不喜欢SpaceVim。

2. 执行：`curl -sLf https://spacevim.org/install.sh | bash`

3. 在终端中执行：`vim`

**在完成下载插件后，你就完成安装SpaceVim了。**

4. 检查你的vim是否有`+lua`和`+python`支持。用命令：`vim --version | grep -E 'lua|python'`：

![linux-check-lua-python][linux-check-lua-python]

**注意：如果你的vim没有`+lua`和`+python`支持，请重新安装有lua和python支持的vim，或者从源码安装。**

5. 检查你是否真的有lua和python2/3支持，通过两个命令： `echo has('lua')`，`echo has('python2')`和`echo has('python3')`
    * Lua 返回: 1
    * Python 返回: 1
    * Python3 返回: 1

**注意：`echo has('python2') 和 `echo has('python3')`，所有的都可以返回1。**

6. 安装字体，请**提前**下载好字体： [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

### 离线安装

#### 检查依赖

以下检查项同[在线安装](#在线安装)相同，故不再赘述：

* git
* lua
* python(2/3)
* vim/gvim

#### 开始安装

离线安装在SpaceVim-v0.9.0-dev中已经变得很简单。是的，你现在可以非常简单地安装SpaceVim而且不需要任何英特网连接。

来试试吧！

1. 从release界面下载： https://github.com/Gabirel/Hack-SpaceVim/releases

2. 解压到：

> ~

3. 链接到SpaceVim代码到vim中：

```bash 
mkdir .vim
ln -svf ~/.SpaceVim/* ~/.vim/
```

3. 打开终端尝试吧！

**恭喜！离线安装已完成！**

**PS: 一些layer需要你自己编译或者下载二进制文件或者联网下载依赖，具体情况请查看默认的配置文件，否则无法工作。**

------------

[Windows指南](installation-for-windows.md#在windows上安装spacevim) | [常见问题](../FAQ.md#faq) | [索引](../README.md#table-of-contents) | [English Document](../../README.md#hack-spacevim)

[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[plugins-download]: https://github.com/Gabirel/Hack-SpaceVim/releases
[linux-check-lua-python]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/8bdd0d9f30a0f22e68ce8e3a2f1c2888a37c3cff/linux-check-lua-python.png
[spacevim-download]: https://github.com/spacevim/spacevim
