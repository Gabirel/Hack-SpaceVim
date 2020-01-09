[![](https://spacevim.org/img/build-with-SpaceVim.svg)](https://spacevim.org)
[![Build Status](https://travis-ci.org/Gabirel/Hack-SpaceVim.svg?branch=master)](https://travis-ci.org/Gabirel/Hack-SpaceVim)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
[![spacevim-version](https://img.shields.io/badge/spacevim-v1.4.0--dev-FF00CC.svg)](https://spacevim.org)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/Gabirel/Hack-SpaceVim.svg)](http://isitmaintained.com/project/Gabirel/Hack-SpaceVim "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/Gabirel/Hack-SpaceVim.svg)](http://isitmaintained.com/project/Gabirel/Hack-SpaceVim "Percentage of issues still open")

# Hack-SpaceVim

[SpaceVim][spacevim] | [Hack-SpaceVim English](README.md) | [Ask questions][Hack-SpaceVim:issue-tracker] | [Bug report & Feature request][SpaceVim:issue-tracker]

## 你能从Hack-SpaceVim得到什么

* :metal: **手把手**教你如何安装SpaceVim 
* :trollface: 快速地部署开发环境 
* :sunglasses: 开发者速成
* :massage_woman: 帮助你熟悉多到吐的插件 
* :muscle: 让你成为专业的vimmer 
* :new_moon_with_face: 用SpaceVim征服整个星球 
* :scream: 告诉你鲜为人知的彩蛋 
* :smirk:一些你永远不会知道的技巧（噢，这好像矛盾了）

---------------------------

Table of Contents
=================

1. [在Windows上的SpaceVim][1]
    * [在Windows上安装SpaceVim][1-1]
      * [Table of Contents][1-1-0]
      * [基础环境][1-1-1]
         * [在线安装基本要求][1-1-1-1]
         * [离线安装基本要求][1-1-1-2]
      * [开始安装][1-1-2]
         * [在线安装][1-1-2-1]
            * [检查基础环境][1-1-2-1-1]
            * [正式安装][1-1-2-1-2]
         * [离线安装][1-1-2-2]
            * [检查基础环境][1-1-2-2-1]
            * [正式安装][1-1-2-2-2]
      * [安装Neovim][1-1-3]
2. [在Linux上的SpaceVim][2]
    * [在Linux上安装SpaceVim][2-1]
      * [Table of Contents][2-1-0]
      * [安装依赖][2-1-1]
         * [在线安装依赖][2-1-1-1]
         * [离线安装依赖][2-1-1-2]
      * [开始安装][2-1-2]
         * [在线安装][2-1-2-1]
            * [检查依赖][2-1-2-1-1]
            * [开始安装][2-1-2-1-2]
         * [离线安装][2-1-2-2]
            * [检查依赖][2-1-2-2-1]
            * [开始安装][2-1-2-2-2]
3. [IDE][ide]
   * [IDE for JavaScript][ide-for-javascript]
      * [Table of Contents][ide-for-js-toc]
      * [基本要求][ide-for-js-requirements]
      * [安装][ide-for-js-installation]
         * [SpaceVim][ide-for-js-spacevim]
         * [安装npm或cnpm][ide-for-js-install-npm-or-cnpm]
         * [安装tern][ide-for-js-install-tern]
         * [将配置加到~/.SpaceVim.d/init.vim][ide-for-js-add-config-into-your-spacevimdinitvim]
      * [配置][ide-for-js-config]
      * [感谢][ide-for-js-thanks]
4.  [常见问题][faq]
    * [Windows][faq-windows]
      * [配置环境变量][set-up-your-path]
      * [python不支持][without-python-support]
      * [SpaceVim卡顿][spacevim-gets-frozen-easily]
      * [vcruntime140.dll错误][vcruntime140dll-error]
      * [Windows上安装繁琐][installing-on-windows-is-too-complicated]
      * [Exuberant ctags未找到][exuberant-ctags-not-found-windows]
    * [Linux][faq-linux]
      * [从源码安装vim][build-vim-from-source]
      * [Exuberant ctags未找到][exuberant-ctags-not-found-linux]
4. [寻觅彩蛋][hidden-egg-hunt]
    * [在SpaceVim上玩游戏][play-games-on-spacevim]
      * [游戏列表][game-lists]
      * [Vim2048][vim2048]
        * [安装][vim2048-instruction]

[1]: zh_CN/installation/installation-for-windows.md#在windows上安装spacevim
[1-1]: zh_CN/installation/installation-for-windows.md#%E5%9C%A8windows%E4%B8%8A%E5%AE%89%E8%A3%85spacevim
[1-1-0]: zh_CN/installation/installation-for-windows.md#table-of-contents
[1-1-1]: zh_CN/installation/installation-for-windows.md#%E5%9F%BA%E7%A1%80%E7%8E%AF%E5%A2%83
[1-1-1-1]: zh_CN/installation/installation-for-windows.md#%E5%9C%A8%E7%BA%BF%E5%AE%89%E8%A3%85%E5%9F%BA%E6%9C%AC%E8%A6%81%E6%B1%82
[1-1-1-2]: zh_CN/installation/installation-for-windows.md#%E7%A6%BB%E7%BA%BF%E5%AE%89%E8%A3%85%E5%9F%BA%E6%9C%AC%E8%A6%81%E6%B1%82
[1-1-2]: zh_CN/installation/installation-for-windows.md#%E5%BC%80%E5%A7%8B%E5%AE%89%E8%A3%85
[1-1-2-1]: zh_CN/installation/installation-for-windows.md#%E5%9C%A8%E7%BA%BF%E5%AE%89%E8%A3%85
[1-1-2-1-1]: zh_CN/installation/installation-for-windows.md#%E6%A3%80%E6%9F%A5%E5%9F%BA%E7%A1%80%E7%8E%AF%E5%A2%83%E6%98%AF%E5%90%A6%E5%B7%B2%E5%AE%89%E8%A3%85
[1-1-2-1-2]: zh_CN/installation/installation-for-windows.md#%E6%AD%A3%E5%BC%8F%E5%AE%89%E8%A3%85
[1-1-2-2]: zh_CN/installation/installation-for-windows.md#%E7%A6%BB%E7%BA%BF%E5%AE%89%E8%A3%85
[1-1-2-2-1]: zh_CN/installation/installation-for-windows.md#%E6%A3%80%E6%9F%A5%E5%9F%BA%E7%A1%80%E7%8E%AF%E5%A2%83-1
[1-1-2-2-2]: zh_CN/installation/installation-for-windows.md#%E6%AD%A3%E5%BC%8F%E5%AE%89%E8%A3%85-1
[1-1-3]: zh_CN/installation/installation-for-windows.md#%E5%AE%89%E8%A3%85neovim

[2]: zh_CN/installation/installation-for-linux.md#在linux上安装spacevim
[2-1]: zh_CN/installation/installation-for-linux.md#在linux上安装spacevim
[2-1-0]: zh_CN/installation/installation-for-linux.md#table-of-contents
[2-1-1]: zh_CN/installation/installation-for-linux.md#安装依赖
[2-1-1-1]: zh_CN/installation/installation-for-linux.md#在线安装依赖
[2-1-1-2]: zh_CN/installation/installation-for-linux.md#离线安装依赖
[2-1-2]: zh_CN/installation/installation-for-linux.md#开始安装
[2-1-2-1]: zh_CN/installation/installation-for-linux.md#在线安装
[2-1-2-1-1]: zh_CN/installation/installation-for-linux.md#检查依赖
[2-1-2-1-2]: zh_CN/installation/installation-for-linux.md#开始安装-1
[2-1-2-2]: zh_CN/installation/installation-for-linux.md#离线安装
[2-1-2-2-1]: zh_CN/installation/installation-for-linux.md#检查依赖-1
[2-1-2-2-2]: zh_CN/installation/installation-for-linux.md#开始安装-2

[ide]: zh_CN/IDE
[ide-for-javascript]: zh_CN/IDE/JavaScript.md#ide-for-javascript
[ide-for-js-toc]: zh_CN/IDE/JavaScript.md#table-of-contents
[ide-for-js-requirements]: zh_CN/IDE/JavaScript.md#基本要求
[ide-for-js-installation]: zh_CN/IDE/JavaScript.md#安装
[ide-for-js-spacevim]: zh_CN/IDE/JavaScript.md#spacevim
[ide-for-js-install-npm-or-cnpm]: zh_CN/IDE/JavaScript.md#安装-npm-或-cnpm
[ide-for-js-install-tern]: zh_CN/IDE/JavaScript.md#安装-tern
[ide-for-js-add-config-into-your-spacevimdinitvim]: zh_CN/IDE/JavaScript.md#将配置加到-spacevimdinitvim
[ide-for-js-config]: zh_CN/IDE/JavaScript.md#配置
[ide-for-js-thanks]: zh_CN/IDE/JavaScript.md#感谢

[faq]: zh_CN/FAQ.md#常见问题
[faq-windows]: zh_CN/FAQ.md#windows
[set-up-your-path]: zh_CN/FAQ.md#配置环境变量
[without-python-support]: zh_CN/FAQ.md#python不支持
[spacevim-gets-frozen-easily]: zh_CN/FAQ.md#spacevim卡顿
[vcruntime140dll-error]: zh_CN/FAQ.md#vcruntime140dll错误
[installing-on-windows-is-too-complicated]: zh_CN/FAQ.md#windows上安装繁琐
[exuberant-ctags-not-found-windows]: zh_CN/FAQ.md#exuberant-ctags未找到
[faq-linux]: zh_CN/FAQ.md#linux
[build-vim-from-source]: zh_CN/FAQ.md#从源码安装vim
[exuberant-ctags-not-found-linux]: zh_CN/FAQ.md#exuberant-ctags未找到-1

[vim-galore]: https://github.com/mhinz/vim-galore
[spacevim]: https://github.com/spacevim/spacevim
[Hack-SpaceVim:issue-tracker]: https://github.com/Gabirel/Hack-SpaceVim/issues
[SpaceVim:issue-tracker]: https://github.com/spacevim/spacevim/issues

[hidden-egg-hunt]: zh_CN/hidden_Egg_Hunt
[play-games-on-spacevim]: zh_CN/hidden_Egg_Hunt/play-games.md#在spacevim上玩游戏
[game-lists]: zh_CN/hidden_Egg_Hunt/play-games.md#游戏列表
[vim2048]: zh_CN/hidden_Egg_Hunt/play-games.md#vim2048
[vim2048-instruction]: zh_CN/hidden_Egg_Hunt/play-games.md#安装
