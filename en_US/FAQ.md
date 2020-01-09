# FAQ

## Table of Contents

* [FAQ](#faq)
   * [Windows](#windows)
      * [Set up your PATH](#set-up-your-path)
      * [without python support](#without-python-support)
      * [SpaceVim gets frozen easily](#spacevim-gets-frozen-easily)
      * [vcruntime140.dll Error](#vcruntime140dll-error)
      * [Installing on Windows is too complicated](#installing-on-windows-is-too-complicated)
      * [Exuberant ctags not found](#exuberant-ctags-not-found)
   * [Linux](#linux)
      * [Building vim from source](#building-vim-from-source)
      * [Exuberant ctags not found](#exuberant-ctags-not-found-1)

## Windows

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
* If all above doesn't work, please add config below into your `init.vim`:

First, you have to know what your python exact version is.

Here's test command:

> py -2 --version

> py -3 --version

According to your python version, add config like this:

```viml
set pythonthreedll=python36.dll
set pythondll=python27.dll
```

**More details: [#17][issue-17]**

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

**5. Why installing SpaceVim on Windows is so complicated? Is there more simple way to do this?**

A: I'm sorry! Nope. Setting up developing environments is killing yourself. I'm HIGHLY RECOMMEND leaving Windows alone.
If you have to, please DO NOT touch Neovim. Please use vim for your mental and physicial helath.

### Exuberant ctags not found

**6. Tagbar: Exuberant ctags not found? What should I do?**

As it shows here:
![ctags-error][ctags-not-found]

A: 

1. You should go to this: https://github.com/universal-ctags/ctags#windows

2. Add the binary folder to your PATH.

My situation is `C:\Program Files\ctagas\ctags.exe`

3. Add config according to your own PATH:

```viml
let g:tagbar_ctags_bin = 'C:\Program Files\ctagas\ctags.exe'
```

## Linux

### Building vim from source

Some distros maybe doesn't have the latest vim. So, some have to build vim from source. 

This section is for building vim from source:

Please go to here: [Build vim from source][build-vim-from-source]

### Exuberant ctags not found

**1. Tagbar: Exuberant ctags not found? What should I do?**

A:

Arch/Manjaro

> sudo pacman -S ctags

Debian/Ubuntu/Linux Mint

> sudo apt-get install ctags

Fedora

> sudo dnf install ctags

CentOS/RHEL

> sudo yum install ctags

*That's all. Done!*

---------------

[Index](README.md#table-of-contents) | [中文文档](../README_zh_CN.md#hack-spacevim)

[path-config]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/08946a3643606420776fcc3fc4d43da6444806cc/path-config.PNG
[vcruntime140.dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[spacevim-issue-tracker]: https://github.com/spacevim/spacevim/issues
[ctags-not-found]: https://cloud.githubusercontent.com/assets/12933851/25282302/a868f3e0-26e2-11e7-8cfb-037f884a4702.png
[issue-17]: https://github.com/Gabirel/Hack-SpaceVim/issues/17
[build-vim-from-source]: https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source
