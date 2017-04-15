# 在Windows上安装SpaceVim

## Table of Contents

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

* [git][]: 用于下载与更新插件
* [lua][]: 用于neocomplete补全
* [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
* [gvim][]: Vim主要程序
* [DejaVu Sans Mono for PowerLine][font-download]: SpaceVim的Aireline所需字体
* [vimproc_win64(32).dll][]: vimporc插件依赖，**必须**
* [vcruntime140.dll][]: 针对vimruntime140 Error（当必要时下载）

### 离线安装基本要求

* [git][]: 用于下载与更新插件
* [lua][]: 用于neocomplete补全
* [python(2/3)][]: 用于job与部分插件支持，推荐安装python3，如果你有特殊需求，可以选择安装python2
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


**恭喜，安装完成！**

## 离线安装

### 检查基础环境

检查列表同[在线安装](#在线安装)相同，故不再赘述：

* git
* lua
* python(2/3)
* gvim

### 正式安装

因[在线安装](#在线安装)中已有详细说明，故不赘述重复部分，只对不同点作出详细说明：

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. 打开一个新的cmd.exe，并执行以下命令：

> mkdir .cache\vimfiles\repos\github.com\Shougo

执行完成后，确保文件夹存在再进行第3步

3. 解压打包好的插件列表至：

> C:\Users\<Your Name>

dein.vim是SpaceVim的插件管理器，原本是通过在线方式自动触发下载的，因当前的离线安装环境，就必须要提前下载下来

**注意：你也可以下载打包好的插件离线包，但是官方强烈建议自行在本地下载后打包以便于使让各个插件处于最新的状态，让各个插件能为你高效地工作。**

4. 打开gvim查看SpaceVim是否正常启动

**注意：如果是自行打包的插件离线包，请注意vimproc_dll是否存在。**

若有`vimproc's dll`，请按照[在线安装](#在线安装)中的安装手册来进行修补。

5. 检查lua和python是否完全支持，步骤如[在线安装](#在线安装)相同

**恭喜，离线安装完成！**

## 安装Neovim

**注意：您已进入了一个禁忌领域。施主，苦海无边，回头是岸……([@wsdjeg][wsdjeg])**

1. 根据施主的操作系统，选择下载[Neovim][Neovim-download]

2. 把Neovim的`bin`目录加入path中

3. 运行neovim

4. 如果缺少`vcruntime140.dll`，请[点我下载][vcruntime140.dll]

5. 安装python2或者python3或者均安装，Neovim支持python2/3同时存在

6. 添加neovim-python

* python2: 
> py -2 pip install --user --upgrade neovim

* python3:
> py -3 pip install --user --upgrade neovim

7. 在neovim-qt.exe中，执行命令：`:CheckHealth` 来查看python2/3是否支持，支持的结果如图所示：

有python2支持：
![nvim-python2-support-success][]

没有python3支持：
![nvim-python3-support-failure][]

若想要有python3支持，请按照第6步进行安装；同样，如果想要有ruby支持按照建议的命令执行即可


**恭喜，安装完成**

**注意：neovim中不需要安装Lua支持，因为neovim(v0.2)目前不支持Lua，因此SpaceVim不会使用neocomplete，而会使用deopelete**

## 常见问题 

### 配置环境变量

1. 如何配置环境变量？

A: *位置：此电脑->属性->高级系统设置->环境变量->系统变量->找到Path->编辑*

![path][path-config]

### python不支持

2. `echo has('python')`返回值均为0，我该怎么办？

A: 请检查是否满足以下条件：

* 在cmd.exe中，查看python命令是否存在
* vim是64位，python就必须安装64位；反之亦然
* vim必须要有`+python/dyn`或`+python3/dyn`或者`+python/dyn;+python3/dyn`

### SpaceVim卡顿

3. 我觉得SpaceVim用起来有点卡顿，怎么回事？

A: 目前有以下可能性：

* 查看你的Lua本地是否支持，vim是否有+lua支持，如果没有lua支持，neocomplete就不会其作用，而是neocomplcache，这就会造成你的卡顿
* 你所使用的SpaceVim有功能性的bug，可以尝试使用SpaceVim的[issue tracker][spacevim-issue-tracker]来帮助你解决
* 你的配置文件可能不恰当，导致占用了大量的内存和磁盘使用。譬如，nodejs里使用ternjs时候对于`loadEagerly`赋值为`**/*.js`就会造成这种现象
* 某一个插件的bug或者某一个插件和另一个插件产生了冲突，若你怀疑有这种现象，请在[issue tracker][spacevim-issue-tracker]提交来修复该问题

### vcruntime140.dll错误

4. 我运行gvim后无法启动，报缺少vcruntime140.dll的错误，我该怎么解决？

A: [点我下载][vcruntime140.dll]，根据自己的操作系统类型选择相应的文件夹：

32位系统位置：`C:\Windows\System32\``
64位系统位置：`C:\Windows\SysWOW64\``


### Windows上安装繁琐

5. 为什么Windows上安装SpaceVim如此麻烦？有更加简单的步骤吗？

A: 抱歉！没有！Windows搭建开发环境真的是很麻烦，很不友好，完全不建议在Windows上安装；若安装，请不要去碰Neovim，这是一个禁忌领域！请为了自己的身心健康，请安装Vim

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
[path-config]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/08946a3643606420776fcc3fc4d43da6444806cc/path-config.PNG
[clone-dein.vim]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/2ac0304f46db1c6470f8f4982296d08875de2894/clone-dein.vim.PNG
[download-plugin]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/a6de44e130d2c5ec1dec28601b8d952c8231f0a0/download-plugins.PNG
[vim-version-check]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/1711e0d2ca9e22d8e3b4942498b0a77f9b25dd2c/vim-version-check.PNG
[vimproc_dll-error]: https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/e7f27e84947f13bc9c91812881e47f2961162fc2/vimproc-dll-error.PNG
[spacevim-issue-tracker]: https://github.com/spacevim/spacevim/issues
[wsdjeg]: https://github.com/wsdjeg
