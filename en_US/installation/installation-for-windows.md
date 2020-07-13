# Install SpaceVim on Windows

## Table of Contents

* [Install SpaceVim on Windows](#install-spacevim-on-windows)
   * [Table of Contents](#table-of-contents)
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
         * [How can I update offline if I have no connection to the Internet?](#how-can-i-update-offline-if-i-have-no-connection-to-the-internet)
   * [Install Neovim](#install-neovim)

## Install prerequisites

### Install online prerequisites

* [git][]: For downloading and updating plugins of SpaceVim
* [lua][]: For neocomplete
* [python(2/3)][]: Support job and part of plugins. Recommend to install both
* [gvim][]: Vim's main program
* [DejaVu Sans Mono for PowerLine][font-download]: Used by the plugins of SpaceVim
* [vimproc_win64(32).dll][]: vimporc needs this, **NECESSARY**
* [vcruntime140.dll][]: Fix vimruntime140 Error(download it when you really need)

### Install offline prerequisites

* [git][]: For downloading and updating plugins of SpaceVim
* [lua][]: For neocomplete
* [python(2/3)][]: Support job and part of plugins. Recommend to install both
* [gvim][]: Vim's main program
* [DejaVu Sans Mono for PowerLine][font-download]: Used by the plugins of SpaceVim
* [vimproc_win64(32).dll][]: vimporc needs this, **NECESSARY**
* [vcruntime140.dll][]: Fix vimruntime140 Error(download it when you really need)
* [Plugins Offline package][plugins-zip]: All plugins of SpaceVim（**Recommend packing it by yourself**）
* [SpaceVim][SpaceVim-download]

## Start to install

### Install online

#### Check prerequisites

1. git --version

The correct result✅：
> git version 2.12.2.windows.2

2. lua53 -v

The correct result✅：
> Lua 5.3.3 Copyright (C) 1994-2016 Lua.org, PUC-Rio

3. python -V

The correct result✅：
> Python 3.6.1

4. gvim

The correct result✅：
> Opened a program

**Notice：If you happen to command not find, please install them correctly and set up your path correctly. 
See how to set up your path:**[FAQ-Set up your PATH][set-up-your-path]

#### Start to install

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. Double-click Gvim's icon, or open a new `cmd.exe` and execute `gvim`. Normally it should open a new terminal to clone `dein.vim`. As it shows below:

![dein.vim-clone][clone-dein.vim]

3. SpaceVim will trigger downloading plugins mode(SpaceVim-v0.3.0 is so that). Wait to finish downloading plugins.

![download-plugins][download-plugin]

4. Check whether your vim has `+Lua` and `+python` feature. Use `:version` to check out:

![vim-version][vim-version-check]

5. Check whether your Lua and python2/3 really works by tow command: `echo has('lua')`, `echo has('python3')` and `echo has('python2')`
    * Lua returns: 1
    * Python returns: 1
    * Python3 returns: 1

**Notice: `echo has('python2') and `echo has('python3')` , only one of them returns `1` instead of returning `0` at the same time. This depends on vim.**

If `echo has('python2/3')` returns 0 both, check this:  [FAQ: Without-python-support][without-python-support]

6. Install fonts, download fonts: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

After finishing installing fonts, your status bar should work very well.

7. Fix `vimproc.dll error`. As it shows below:

![vimproc-dll][vimproc_dll-error]

[Click me to download][vimproc_win64(32).dll]. Copy it to: `C:\Users\<Your Name>\.cache\vimfiles\repos\github.com\Shougo\vimproc.vim\lib`


**Congratulations. You'are done!**

### Install offline

#### Check prerequisites

List is the same as [Install online: Check prerequisites](#check-prerequisites). So I won't repeat it:

* git
* lua
* python(2/3)
* gvim

#### Start to install

Still this part has the same introductions in [Install online: Start to install](#start-to-install-1). I will skip the same part. Only explain at different parts.

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. Extract the package to:

> C:\Users\<Your Name>

dein.vim is the plugins manager of SpaceVim. It is downloaded automatically by starting gvim the first time. So you have to download it in advance.

**Notice: You could download the offline package. But we HIGHLY RECOMMEND packing it up by yourself to make sure that all plugins is up-to-date to make you more powerful.**

**For newbie: zip your `~/.cache/vimfiles` to packing SpaceVim**

3. Open gvim to check out whether SpaceVim could start without any errors.

**Notice: Please make sure that vimproc_dll exists if you are using your own package.**

If you have `vimproc's dll`, please fix this according to the manual of [Install online: Start to install](#start-to-install-1).

4. Check whether gvim has lua and python's full support, these steps are the same as [Install online: Start to install](#start-to-install-1)

5. Install fonts, download fonts **in advance**: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

After finishing installing fonts, the status bar should work very well.

**Congratulations! Install offline successfully!**

#### How can I update offline if I have no connection to the Internet?

As [@TamaMcGlinn](https://github.com/TamaMcGlinn) mentions, [`git bundle`](https://git-scm.com/docs/git-bundle) is suitable for incremental updates for plugins.

In this way, you don't have to copy the whole plugins via **USB** or **internal email**.

Unfortunately, for all those plugins with `git bundle` method, you have to write scripts in order to incrementally update or load changes.

More details: [Instructions For Installing SpaceVim - OFFLINE](https://github.com/Gabirel/Hack-SpaceVim/issues/12#issuecomment-654206784)

## Install Neovim

**Notice: You've entered the taboo areas.**

> The sea of suffering is boundless; yet a turn of the gear is the other shore.

*Let's go back to our shore [@wsdjeg][wsdjeg] |:(*

1. According to your own OS, select your version of [Neovim][Neovim-download]

2. Add Neovim's `bin` folder to your `PATH`

3. Execute neovim

4. If you are missing `vcruntime140.dll`, please [click me to download][vcruntime140.dll]

5. Install python2/python3 or both, which is allowed by Neovim

6. Install full support of python of neovim:

* python2: 

> py -2 pip install --user --upgrade neovim

* python3:

> py -3 pip install --user --upgrade neovim

7. Execute neovim-qt.exe, and use `:CheckHealth` to check out whether your neovim supports python2/3. As results shows below:

With python2 support:
![nvim-python2-support-success][]

Without python3 support:
![nvim-python3-support-failure][]

If you want to have python3 support, please install it according to step 6; Also, use commands suggested by neovim to have ruby support.

8. Install SpaceVim

> git clone https://github.com/SpaceVim/SpaceVim.git %userprofile%\AppData\Local\nvim\


**Congratulations! You've installed it successfully.**

**Notice: Neovim doesn't support lua(For now) in neovim-v0.2. So, SpaceVim uses deopelete for auto-completing code instead of neocomplete.**

---------------

[Instructions for Linux](installation-for-linux.md#install-spacevim-on-linux) | [FAQ](../FAQ.md#faq) | [Index](../README.md#table-of-contents) | [中文文档](../../README_zh_CN.md#hack-spacevim)

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
[set-up-your-path]: ../FAQ.md#set-up-your-path
[without-python-support]: ../FAQ.md#without-python-support
