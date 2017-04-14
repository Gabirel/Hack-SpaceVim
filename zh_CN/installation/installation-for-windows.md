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
    - [dein.vim][]: SpaceVim的插件管理器（**必须**）
    - [SpaceVim][SpaceVim-download]

## 开始安装

    1. git --version
    2. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles
    3. vcruntime140.dll

[git]: https://git-scm.com/download
[lua]: http://luabinaries.sourceforge.net/download.html
[python(2/3)]: https://www.python.org/downloads
[gvim]: https://github.com/vim/vim-win32-installer/releases
[vimproc_win64(32).dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[dein.vim]: https://github.com/Shougo/dein.vim.git
[SpaceVim-download]: https://github.com/SpaceVim/SpaceVim.git
