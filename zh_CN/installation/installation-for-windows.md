Table of Contents
=================

   * [在Windows上安装SpaceVim](#在windows上安装spacevim)
      * [基础环境](#基础环境)
         * [在线安装基本要求](#在线安装基本要求)
         * [离线安装基本要求](#离线安装基本要求)
      * [开始安装](#开始安装)
         * [在线安装](#在线安装)
            * [检查基础环境是否已安装](#检查基础环境是否已安装)
            * [正式安装](#正式安装)

# 在Windows上安装SpaceVim

## 基础环境

### 在线安装基本要求

- [git][]: 用于下载与更新插件
- [lua][]: 用于neocomplete补全
- [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
- [gvim][]: Vim主要程序
- [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
- [vimproc_win64(32).dll][]: 针对vimruntime140 Error（当必要时下载）

### 离线安装基本要求

- [git][]: 用于下载与更新插件
- [lua][]: 用于neocomplete补全
- [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
- [gvim][]: Vim主要程序
- [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
- [vimproc_win64(32).dll][]: 针对vimruntime140 Error（当必要时下载）
- [dein.vim][]: SpaceVim的插件管理器（**没错！这也是必须的):D**）
- [SpaceVim][SpaceVim-download]

## 开始安装

### 在线安装

#### 检查基础环境是否已安装

1. git --version

正确结果✅：
> git version 2.12.2.windows.2

2. lua53 -v

正确结果✅：
> Lua 5.3.3 Copyright (C) 1994-2016 Lua.org, PUC-Rio

3. python -v

正确结果✅：
> Python 3.6.1

4. gvim

正确结果✅：
> 打开一个窗口

**注意：如果命令找不到等情况请安装好环境并配置环境变量，如何配置环境变量见下图：**

*位置：此电脑->属性->高级系统设置->环境变量->系统变量->找到Path->编辑*

![path][path-config]

#### 正式安装

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

[git]: https://git-scm.com/download
[lua]: http://luabinaries.sourceforge.net/download.html
[python(2/3)]: https://www.python.org/downloads
[gvim]: https://github.com/vim/vim-win32-installer/releases
[vimproc_win64(32).dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[dein.vim]: https://github.com/Shougo/dein.vim.git
[SpaceVim-download]: https://github.com/SpaceVim/SpaceVim.git
[path-config]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/08946a3643606420776fcc3fc4d43da6444806cc/path-config.PNG
