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
      * [Install Neovim](#install-neovim)
      * [FAQ](#faq)
         * [Set up your PATH](#set-up-your-path)
         * [without python support](#without-python-support)
         * [SpaceVim gets frozen easily](#spacevim-gets-frozen-easily)
         * [vcruntime140.dll Error](#vcruntime140dll-error)
         * [Installing on Windows is too complicated](#installing-on-windows-is-too-complicated)

## Install prerequisites

### Install online prerequisites

* [git][]: For downloading and updating plugins of SpaceVim
* [lua][]: For neocomplete
* [python(2/3)][]: Support job and part of plugins. Recommend to install `python3`
* [gvim][]: Vim's main program
* [DejaVu Sans Mono for PowerLine][font-download]: Used by the plugins of SpaceVim
* [vimproc_win64(32).dll][]: vimporc needs this, **NECESSARY**
* [vcruntime140.dll][]: Fix vimruntime140 Error(download it when you really need)

### Install offline prerequisites

* [git][]: For downloading and updating plugins of SpaceVim
* [lua][]: For neocomplete
* [python(2/3)][]: Support job and part of plugins. Recommend to install `python3`
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

3. python -v

The correct result✅：
> Python 3.6.1

4. gvim

The correct result✅：
> Opened a program

**Notice：If you happen to command not find, please install them correctly and set up your path correctly. 
See how to set up your path:**[FAQ-Set up your PATH](#set-up-your-path)

#### Start to install

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. Double-click Gvim's icon, or open a new `cmd.exe` and execute `gvim`. Normally it should open a new terminal to clone `dein.vim`. As it shows below:

![dein.vim-clone][clone-dein.vim]

3. SpaceVim will trigger downloading plugins mode(SpaceVim-v0.3.0 is so that). Wait to finish downloading plugins.

![download-plugins][download-plugin]

4. Check whether your vim has `+Lua` and `+python` feature. Use `:version` to check out:

![vim-version][vim-version-check]

5. Check whether your Lua and python2/3 really works by tow command: `echo has('lua')` and `echo has('python3')` or `echo has('python2')`
    * Lua returns: 1
    * Python returns: 1

**Notice: `echo has('python2') and `echo has('python3')` , only one of them returns `1` instead of returning `0` at the same time. This depends on vim.**

*If `echo has('python2/3')` returns 0 both, check this: * [FAQ: Without-python-support](#without-python-support)

6. Install fonts, download fonts: [DejaVu Sans Mono for PowerLine.ttf][font-download]. 

After finishing installing fonts, your status bar should work very well.

7. Fix `vimproc.dll error`. As it shows below:

![vimproc-dll][vimproc_dll-error]

[Click me to download][vimproc_win64(32).dll]. Copy it to: `C:\Users\<Your Name>\.cache\vimfiles\repos\github.com\Shougo\vimproc.vim\lib`


**Congratulations. You'are done!**

### Install offline

#### Check prerequisites

List is the same as [Install online](#Install online). So I won't repeat it:

* git
* lua
* python(2/3)
* gvim

#### Start to install

Still this part has the same introductions in [Install online](#Install online). I will skip the same part. Only explain at different parts.

1. git clone https://github.com/SpaceVim/SpaceVim.git vimfiles

2. Open a new `cmd.exe`, and execute:

> mkdir .cache\vimfiles\repos\github.com\Shougo

After finishing this, please make sure that that folder really exists.

3. Extract the package to:

> C:\Users\<Your Name>

dein.vim is the plugins manager of SpaceVim. It is downloaded automatically by starting gvim the first time. So you have to download it in advance.

**Notice: You could download the offline package. But we HIGHLY RECOMMEND packing it up by yourself to make sure that all plugins is up-to-date to make you more powerful.

4. Open gvim to check out whether SpaceVim could start without any errors.

**Notice: Please make sure that vimproc_dll exists if you are using your own package.**

If you have `vimproc's dll`, please fix this according to the manual of [Install online](#Install online).

5. Check whether gvim has lua and python's full support, these steps are the same as [Install online](#Installl online)

**Congratulations! Install online successfully!**

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

If you want to has python3 support, please install it according to step 6; Also, use commands suggested by neovim to has ruby support.

8. Install SpaceVim

> git clone https://github.com/SpaceVim/SpaceVim.git %userprofile%\AppData\Local\nvim\


**Congratulations! You've installed it successfully. You've reached the boundless sea of suffering. Congratulations again.**

**Notice: Neovim doesn't support lua(For now) in neovim-v0.2. So, SpaceVim uses deopelete for auto-completing code instead of neocomplete.**

## FAQ

### Set up your PATH

**1. How to set up my PATH on Windows?**

A: *Location: My computer->properties->Advance System Setting->Environment variables->System variables->Find Path->Edit*

*I'm sorry. I don't use Windows. I can't use English on my VirtualOS. Windows won't let me do this. ):*

![path][path-config]

### without python support

**2. `echo has('python')` always returns 0. What should I do?**

A: Please check out whether you meet all these requirements:

* Open a new `cmd.exe` to check out whether you can execute command: python
* If you install 64bit-gvim, make sure you install 64bit python as well. Vice Versa.
* Gvim must has `+python/dyn` or `+python3/dyn` or `+python/dyn;+python3/dyn`

### SpaceVim gets frozen easily

**3. I can feel my SpaceVim gets frozen a little bit. What's exactly going on?**

A: There are 4 kind of possibilities:

* Check out whether you can execute `lua` command in your new terminal and your gvim has `+lua` feature.
    SpaceVim will use `neocomplcache` instead of `neocomplete` without lua support, which makes SpaceVim gets frozen or have some delay.

* You may encounter bugs of SpaceVim. Feel free to use [issue tracker][spacevim-issue-tracker] to solve this.
* Your config file is probably the problem. For example, your SpaceVim will get frozen totally if you make `loadEagerly` as `**/*.js` when writing nodejs file.
* Maybe one of plugins has some conflicts with another plugin. Please open a new [issue][spacevim-issue-tracker] to help you fix this problem if you suspect.

### vcruntime140.dll Error

**4. I can't start gvim. It says that vcruntime140.dll errors. What should I do?**

A: [Click me to download][vcruntime140.dll]. Copyt it to the corresponding folder according to your own OS:

32bit OS: `C:\Windows\System32\`

64bit OS: `C:\Windows\SysWOW64\`


### Installing on Windows is too complicated

**5. Why installing SpaceVim on Windows is so complicated? Is there more simple wat to do this?**

A: I'm sorry! Nope. Setting up developing environments is killing yourself. I'm HIGHLY RECOMMEND leaving Windows alone.
If you have to, please DO NOT touch Neovim. Please use vim for your mental and physicial helath.

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
