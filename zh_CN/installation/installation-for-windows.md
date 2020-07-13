# 在Windows上安装SpaceVim

## Table of Contents

* [在Windows上安装SpaceVim](#在windows上安装spacevim)
   * [Table of Contents](#table-of-contents)
   * [基础环境](#基础环境)
      * [在线安装基本要求](#在线安装基本要求)
      * [离线安装基本要求](#离线安装基本要求)
   * [开始安装](#开始安装)
      * [在线安装](#在线安装)
         * [检查基础环境](#检查基础环境)
         * [正式安装](#正式安装)
      * [离线安装](#离线安装)
         * [检查基础环境](#检查基础环境-1)
         * [正式安装](#正式安装-1)
         * [离线状态如何更新？](#离线状态如何更新？)
   * [安装Neovim](#安装neovim)

## 基础环境

### 在线安装基本要求

* [git][]: 用于下载与更新插件
* [lua][]: 用于neocomplete补全
* [python(2/3)][]: 用于job与部分插件支持，推荐全部安装
* [gvim][]: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
* [vimproc_win64(32).dll][]: vimporc插件依赖，**必须**
* [vcruntime140.dll][]: 针对vimruntime140 Error（当必要时下载）

### 离线安装基本要求

* [git][]: 用于下载与更新插件
* [lua][]: 用于neocomplete补全
* [python(2/3)][]: 用于job与部分插件支持，推荐全部安装
* [gvim][]: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Airline所需字体
* [vimproc_win64(32).dll][]: vimporc插件依赖，**必须**
* [vcruntime140.dll][]: 针对vimruntime140 Error（当必要时下载）
* [插件压缩包][plugins-zip]: SpaceVim的插件离线包（**建议自行打包下载**）
* [SpaceVim][SpaceVim-download]

## 开始安装

### 在线安装

#### 检查基础环境

1. git --version

正确结果✅：
> git version 2.12.2.windows.2

2. lua53 -v

正确结果✅：
> Lua 5.3.3 Copyright (C) 1994-2016 Lua.org, PUC-Rio

3. python -V

正确结果✅：
> Python 3.6.1

4. gvim

正确结果✅：
> 打开一个窗口

**注意：如果命令找不到等情况请安装好环境并配置环境变量，如何配置环境变量见：** [常见问题：配置环境变量][set-up-your-path]

#### 正式安装

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. 双击桌面的gvim图标，或打开cmd.exe后运行gvim，正常情况下会打开一个新的终端克隆`dein.vim`，如图所示：

![dein.vim-clone][clone-dein.vim]

3. SpaceVim会自动触发下载插件模式(SpaceVim-v0.3.0-dev是如此)，等待完成即可

![download-plugins][download-plugin]

4. 检查vim是否有Lua和python(2/3)特性支持，输命令：`:version`以查看：

![vim-version][vim-version-check]

5. 检查Lua和python(2/3)支持是否真的在起作用，通过两个命令：`echo has('lua')`，`echo has('python2')`和`echo has('python3')`:
    * Lua返回值为：1
    * python返回值：1
    * python3返回值：1

**注意：`echo has('python2')`和`echo has('python3')`的值均会返回`1`**

*若，`echo has('python')`返回值均为0，请查看：* [常见问题：python不支持][without-python-support]

6. 安装字体，字体下载：[DejaVu Sans Mono for PowerLine.ttf][font-download]，安装完字体后状态栏即可正常显示

7. 解决`vimproc.dll错误`，错误如下图：

![vimproc-dll][vimproc_dll-error]

[点我下载][vimproc_win64(32).dll]，位置放在：`C:\Users\<Your Name>\.cache\vimfiles\repos\github.com\Shougo\vimproc.vim\lib`


**恭喜，安装完成！**

### 离线安装

#### 检查基础环境

检查列表同[在线安装: 检查基础环境](#检查基础环境)相同，故不再赘述：

* git
* lua
* python(2/3)
* gvim

#### 正式安装

因[在线安装： 正式安装](#正式安装)中已有详细说明，故不赘述重复部分，只对不同点作出详细说明：

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. 解压打包好的插件列表至：

> C:\Users\<Your Name>

dein.vim是SpaceVim的插件管理器，原本是通过在线方式自动触发下载的，因当前的离线安装环境，就必须要提前下载下来

**注意：你也可以下载打包好的插件离线包，但是官方强烈建议自行在本地下载后打包以便于使让各个插件处于最新的状态，让各个插件能为你高效地工作。**

**新人看这里的时候眼睛请睁大，需要打包的位置是：`~/.cache/vimfiles`**

3. 打开gvim查看SpaceVim是否正常启动

**注意：如果是自行打包的插件离线包，请注意vimproc_dll是否存在。**

若有`vimproc's dll`，请按照[在线安装：正式安装](#正式安装)中的安装手册来进行修补。

4. 检查lua和python是否完全支持，步骤如[在线安装：正式安装](#正式安装)相同

5. 安装字体，请**提前下载好**: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

在安装完字体后，状态栏应该就可以正常工作了。

**恭喜，离线安装完成！**

#### 离线状态如何更新？

[@TamaMcGlinn](https://github.com/TamaMcGlinn) 提出了使用 [`git bundle`](https://git-scm.com/docs/git-bundle) 想法。这个想法十分适合插件的增量更新。

这样一来，你就不需要通过**U盘**或者**内部邮件**的方式来进行全量拷贝。

不过，不幸的是，目前为止使用这种增量更新的方式，你必须要写脚本来达到你的增量更新的目的。官方并没有提供相关的操作。

具体的细节请看： [Instructions For Installing SpaceVim - OFFLINE](https://github.com/Gabirel/Hack-SpaceVim/issues/12#issuecomment-654206784)

## 安装Neovim


1. 根据施主的操作系统，选择下载[Neovim][Neovim-download]

2. 把Neovim的`bin`目录加入path中

3. 运行neovim

4. 如果缺少`vcruntime140.dll`，请[点我下载][vcruntime140.dll]

5. 安装python2或者python3或者均安装，Neovim支持python2/3同时存在

6. 添加neovim-python

* python2: 

> py -2 pip install --user --upgrade neovim

* python3

> py -3 pip install --user --upgrade neovim

7. 在neovim-qt.exe中，执行命令：`:CheckHealth` 来查看python2/3是否支持，支持的结果如图所示：

有python2支持：
![nvim-python2-support-success][]

没有python3支持：
![nvim-python3-support-failure][]

若施主想要有python3支持，请按照第6步进行安装；同样，如果想要有ruby支持按照建议的命令执行即可


8. 安装SpaceVim

> git clone https://github.com/SpaceVim/SpaceVim.git %userprofile%\AppData\Local\nvim\


**注意：neovim中施主不需要安装Lua支持，因为neovim(v0.2)目前不支持Lua，因此SpaceVim不会使用neocomplete，而会使用deopelete**

--------------

[Linux指南](installation-for-linux.md##在linux上安装spacevim) | [常见问题](../FAQ.md#faq) | [索引](../README.md#table-of-contents) | [English Document](../../README.md#hack-spacevim)

[git]: https://git-scm.com/download
[lua]: http://luabinaries.sourceforge.net/download.html
[python(2/3)]: https://www.python.org/downloads
[gvim]: https://github.com/vim/vim-win32-installer/releases
[vimproc_win64(32).dll]: https://github.com/Shougo/vimproc.vim/releases
[vcruntime140.dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[Neovim-download]: https://github.com/neovim/neovim/wiki/Installing-Neovim#windows
[nvim-python2-support-success]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/5aff57c9397cd26dba23dd0d81b94fa9cf061b56/nvim-python2-support-success.PNG
[nvim-python3-support-failure]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/5aff57c9397cd26dba23dd0d81b94fa9cf061b56/nvim-python3-support-failure.PNG
[plugins-zip]: https://github.com/Gabirel/Hack-SpaceVim/releases
[SpaceVim-download]: https://github.com/SpaceVim/SpaceVim.git
[clone-dein.vim]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/2ac0304f46db1c6470f8f4982296d08875de2894/clone-dein.vim.PNG
[download-plugin]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/a6de44e130d2c5ec1dec28601b8d952c8231f0a0/download-plugins.PNG
[vim-version-check]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/1711e0d2ca9e22d8e3b4942498b0a77f9b25dd2c/vim-version-check.PNG
[vimproc_dll-error]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/e7f27e84947f13bc9c91812881e47f2961162fc2/vimproc-dll-error.PNG
[wsdjeg]: https://github.com/wsdjeg

[set-up-your-path]: ../FAQ.md#配置环境变量
[without-python-support]: ../FAQ.md#python不支持
