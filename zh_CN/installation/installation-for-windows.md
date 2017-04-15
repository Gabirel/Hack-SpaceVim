# 在Windows上安装SpaceVim

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
      * [常见问题](#常见问题)


## 基础环境

### 在线安装基本要求

- [git][]: 用于下载与更新插件
- [lua][]: 用于neocomplete补全
- [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
- [gvim][]: Vim主要程序
- [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
- [vimproc_win64(32).dll][]: vimporc插件依赖，**必须**
- [vcruntime140.dll][]: 针对vimruntime140 Error（当必要时下载）

### 离线安装基本要求

- [git][]: 用于下载与更新插件
- [lua][]: 用于neocomplete补全
- [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
- [gvim][]: Vim主要程序
- [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
- [vimproc_win64(32).dll][]: vimporc插件依赖，**必须**
- [vcruntime140.dll][]: 针对vimruntime140 Error（当必要时下载）
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

**注意：如果命令找不到等情况请安装好环境并配置环境变量，如何配置环境变量见：**[常见问题-1](#常见问题)

#### 正式安装

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. 双击桌面的gvim图标，或打开cmd.exe后运行gvim，正常情况下会打开一个新的终端克隆`dein.vim`，如图所示：
![dein.vim-clone][clone-dein.vim]

3. SpaceVim会自动出发下载插件模式(SpaceVim-v0.3.0-dev是如此)，等待完成即可
![download-plugins][download-plugin]

4. 检查vim是否有Lua和python(2/3)特性支持，输命令：`:version`以查看：
![vim-version][vim-version-check]

5. 检查Lua和python(2/3)支持是否真的在起作用，通过两个命令：`echo has('lua')`和`echo has('python3')`或者`echo has('python2')`:
    * Lua返回值为：1
    * python返回值：1

**注意：`echo has('python2')`和`echo has('python3')`的值只会返回一个，不会同时为1，这是由vim的特性决定的**

*若，`echo has('python')`返回值均为0，请查看：* [常见问题-2](#常见问题)

6. 安装字体，字体下载：[DejaVu Sans Mono for PowerLine.ttf][font-download]，安装完字体后状态栏即可正常显示

7. 解决`vimproc.dll错误`，错误如下图：
![vimproc-dll][vimproc_dll-error]

[点我下载][vimproc_win64(32).dll]，位置放在：`C:\Users\<Your Name>\.cache\vimfiles\repos\github.com\Shougo\vimproc.vim\lib`


**恭喜，完成！**


## 常见问题 
1. 如何配置环境变量？

A: *位置：此电脑->属性->高级系统设置->环境变量->系统变量->找到Path->编辑*

![path][path-config]

2. `echo has('python')`返回值均为0，我该怎么办？

A: 请检查是否满足以下条件：

- 在cmd.exe中，查看python命令是否存在
- vim是64位，python就必须安装64位；反之亦然
- vim必须要有`+python/dyn`或`+python3/dyn`或者`+python/dyn;+python3/dyn`

3. 我觉得SpaceVim用起来有点卡顿，怎么回事？

A: 目前有以下可能性：

- 查看你的Lua本地是否支持，vim是否有+lua支持，如果没有lua支持，neocomplete就不会其作用，而是neocomplcache，这就会造成你的卡顿
- 你所使用的SpaceVim有功能性的bug，可以尝试使用SpaceVim的[issue tracker][spacevim-issue-tracker]来帮助你解决
- 你的配置文件可能不恰当，导致占用了大量的内存和磁盘使用。譬如，nodejs里使用ternjs时候对于`loadEagerly`赋值为`**/*.js`就会造成这种现象
- 某一个插件的bug或者某一个插件和另一个插件产生了冲突，若发生了这种现象，请在提交[issue tracker][spacevim-issue-tracker]来修复该问题

[git]: https://git-scm.com/download
[lua]: http://luabinaries.sourceforge.net/download.html
[python(2/3)]: https://www.python.org/downloads
[gvim]: https://github.com/vim/vim-win32-installer/releases
[vimproc_win64(32).dll]: https://github.com/Shougo/vimproc.vim/releases
[vcruntime140.dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[font-download]: https://github.com/wsdjeg/DotFiles/blob/master/fonts/DejaVu%20Sans%20Mono%20for%20Powerline.ttf
[dein.vim]: https://github.com/Shougo/dein.vim.git
[SpaceVim-download]: https://github.com/SpaceVim/SpaceVim.git
[path-config]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/08946a3643606420776fcc3fc4d43da6444806cc/path-config.PNG
[clone-dein.vim]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/2ac0304f46db1c6470f8f4982296d08875de2894/clone-dein.vim.PNG
[download-plugin]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/a6de44e130d2c5ec1dec28601b8d952c8231f0a0/download-plugins.PNG
[vim-version-check]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/1711e0d2ca9e22d8e3b4942498b0a77f9b25dd2c/vim-version-check.PNG
[vimproc_dll-error]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/e7f27e84947f13bc9c91812881e47f2961162fc2/vimproc-dll-error.PNG
[spacevim-issue-tracker]: https://github.com/spacevim/spacevim/issues
