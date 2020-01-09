[![](https://spacevim.org/img/build-with-SpaceVim.svg)](https://spacevim.org)
[![Build Status](https://travis-ci.org/Gabirel/Hack-SpaceVim.svg?branch=master)](https://travis-ci.org/Gabirel/Hack-SpaceVim)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
[![spacevim-version](https://img.shields.io/badge/spacevim-v1.4.0--dev-FF00CC.svg)](https://spacevim.org)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/Gabirel/Hack-SpaceVim.svg)](http://isitmaintained.com/project/Gabirel/Hack-SpaceVim "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/Gabirel/Hack-SpaceVim.svg)](http://isitmaintained.com/project/Gabirel/Hack-SpaceVim "Percentage of issues still open")

# Hack-SpaceVim

[SpaceVim][spacevim] | [Hack-SpaceVim 中文版](README_zh_CN.md) | [Ask questions][Hack-SpaceVim:issue-tracker] | [Bug report & Feature request][SpaceVim:issue-tracker]


## What can you get from Hack-SpaceVim

* :metal: Introductions about how to install SpaceVim with **step by step** 
* :trollface: Set up developing environments very fast 
* :sunglasses: Become a developer very quickly 
* :massage_woman: Help you get acquainted with mountains of plugins 
* :muscle: Make you a professional vimmer 
* :new_moon_with_face: Let you hack this planet with SpaceVim 
* :scream: Tell you some facts somebody else won't tell you 
* :smirk: Tricks you will never know(contradictory statements)

Table of Contents
=================

1. [SpaceVim on Windows][1]
    * [Install SpaceVim on Windows][1-1]
      * [Table of Contents][1-1-0]
      * [Install prerequisites][1-1-1]
         * [Install online prerequisites][1-1-1-1]
         * [Install offline prerequisites][1-1-1-2]
      * [Start to install][1-1-2]
         * [Install online][1-1-2-1]
            * [Check prerequisites][1-1-2-1-1]
            * [Start to install][1-1-2-1-2]
         * [Install offline][1-1-2-2]
            * [Check prerequisites][1-1-2-2-1]
            * [Start to install][1-1-2-2-2]
      * [Install Neovim][1-1-3]
2. [SpaceVim on Linux][2]
   * [Install SpaceVim on Linux][2-1]
      * [Table of Contents][2-1-0]
      * [Install prerequisites][2-1-1]
         * [Install online prerequisites][2-1-1-1]
         * [Install offline prerequisites][2-1-1-2]
      * [Start to install][2-1-2]
         * [Install online][2-1-2-1]
            * [Check prerequisites][2-1-2-1-1]
            * [Start to install][2-1-2-1-2]
         * [Install offline][2-1-2-2]
            * [Check prerequisites][2-1-2-2-1]
            * [Start to install][2-1-2-2-2]
3. [IDE][ide]
   * [IDE for JavaScript][ide-for-javascript]
      * [Table of Contents][ide-for-js-table-of-contents]
      * [Requirements][ide-for-js-requirements]
      * [Installation][ide-for-js-installation]
         * [SpaceVim][ide-for-js-spacevim]
         * [Install npm or cnpm][ide-for-js-install-npm-or-cnpm]
         * [Install tern][ide-for-js-install-tern]
         * [Add config into your ~/.SpaceVim.d/init.vim][ide-for-js-add-config-into-your-spacevimdinitvim]
      * [Config][ide-for-js-config]
      * [Credits &amp; Thanks][ide-for-js-thanks]
3. [FAQ][faq]
    * [Windows][faq-windows]
      * [Set up your PATH][set-up-your-path]
      * [without python support][without-python-support]
      * [SpaceVim gets frozen easily][spacevim-gets-frozen-easily]
      * [vcruntime140.dll Error][vcruntime140dll-error]
      * [Installing on Windows is too complicated][installing-on-windows-is-too-complicated]
      * [Exuberant ctags not found][exuberant-ctags-not-found-windows]
    * [Linux][faq-linux]
      * [Building vim from source][building-vim-from-source]
      * [Exuberant ctags not found][exuberant-ctags-not-found-linux]
4. [Hidden Egg Hunt][hidden-egg-hunt]
    * [Play games on SpaceVim][play-games-on-spacevim]
      * [Game Lists][game-lists]
      * [Vim2048][vim2048]
        * [Instruction][vim2048-instruction]

---------------------------

# Reference

New to Vim: [vim-galore][]


[spacevim]: https://github.com/spacevim/spacevim
[Hack-SpaceVim:issue-tracker]: https://github.com/Gabirel/Hack-SpaceVim/issues
[SpaceVim:issue-tracker]: https://github.com/spacevim/spacevim/issues
[vim-galore]: https://github.com/mhinz/vim-galore

[1]: en_US/installation/installation-for-windows.md#install-spacevim-on-windows
[1-1]: en_US/installation/installation-for-windows.md#install-spacevim-on-windows
[1-1-0]: en_US/installation/installation-for-windows.md#table-of-contents
[1-1-1]: en_US/installation/installation-for-windows.md#install-prerequisites
[1-1-1-1]: en_US/installation/installation-for-windows.md#install-online-prerequisites
[1-1-1-2]: en_US/installation/installation-for-windows.md#install-offline-prerequisites
[1-1-2]: en_US/installation/installation-for-windows.md#start-to-install
[1-1-2-1]: en_US/installation/installation-for-windows.md#install-online
[1-1-2-1-1]: en_US/installation/installation-for-windows.md#check-prerequisites
[1-1-2-1-2]: en_US/installation/installation-for-windows.md#start-to-install-1
[1-1-2-2]: en_US/installation/installation-for-windows.md#install-offline
[1-1-2-2-1]: en_US/installation/installation-for-windows.md#check-prerequisites-1
[1-1-2-2-2]: en_US/installation/installation-for-windows.md#start-to-install-2
[1-1-3]: en_US/installation/installation-for-windows.md#install-neovim

[2]: en_US/installation/installation-for-linux.md#install-spacevim-on-linux
[2-1]: en_US/installation/installation-for-linux.md#install-spacevim-on-linux
[2-1-0]: en_US/installation/installation-for-linux.md#table-of-contents
[2-1-1]: en_US/installation/installation-for-linux.md#install-prerequisites
[2-1-1-1]: en_US/installation/installation-for-linux.md#install-online-prerequisites
[2-1-1-2]: en_US/installation/installation-for-linux.md#install-offline-prerequisites
[2-1-2]: en_US/installation/installation-for-linux.md#start-to-install
[2-1-2-1]: en_US/installation/installation-for-linux.md#install-online
[2-1-2-1-1]: en_US/installation/installation-for-linux.md#check-prerequisites
[2-1-2-1-2]: en_US/installation/installation-for-linux.md#start-to-install-1
[2-1-2-2]: en_US/installation/installation-for-linux.md#install-offline
[2-1-2-2-1]: en_US/installation/installation-for-linux.md#check-prerequisites-1
[2-1-2-2-2]: en_US/installation/installation-for-linux.md#start-to-install-2

[ide]: en_US/IDE
[ide-for-javascript]: en_US/IDE/JavaScript.md#ide-for-javascript
[ide-for-js-table-of-contents]: en_US/IDE/JavaScript.md#table-of-contents
[ide-for-js-requirements]: en_US/IDE/JavaScript.md#requirements
[ide-for-js-installation]: en_US/IDE/JavaScript.md#installation
[ide-for-js-spacevim]: en_US/IDE/JavaScript.md#spacevim
[ide-for-js-install-npm-or-cnpm]: en_US/IDE/JavaScript.md#install-npm-or-cnpm
[ide-for-js-install-tern]: en_US/IDE/JavaScript.md#install-tern
[ide-for-js-add-config-into-your-spacevimdinitvim]: en_US/IDE/JavaScript.md#add-config-into-your-spacevimdinitvim
[ide-for-js-config]: en_US/IDE/JavaScript.md#config
[ide-for-js-thanks]: en_US/IDE/JavaScript.md#credits--thanks

[faq]: en_US/FAQ.md#faq
[faq-windows]: en_US/FAQ.md#windows
[set-up-your-path]: en_US/FAQ.md#set-up-your-path
[without-python-support]: en_US/FAQ.md#without-python-support
[spacevim-gets-frozen-easily]: en_US/FAQ.md#spacevim-gets-frozen-easily
[vcruntime140dll-error]: en_US/FAQ.md#vcruntime140dll-error
[installing-on-windows-is-too-complicated]: en_US/FAQ.md#installing-on-windows-is-too-complicated
[exuberant-ctags-not-found-windows]: en_US/FAQ.md#exuberant-ctags-not-found
[faq-linux]: en_US/FAQ.md#linux
[building-vim-from-source]: en_US/FAQ.md#building-vim-from-source
[exuberant-ctags-not-found-linux]: en_US/FAQ.md#exuberant-ctags-not-found-1

[hidden-egg-hunt]: en_US/hidden_Egg_Hunt
[play-games-on-spacevim]: en_US/hidden_Egg_Hunt/play-games.md#play-games-on-spacevim
[game-lists]: en_US/hidden_Egg_Hunt/play-games.md#game-lists
[vim2048]: en_US/hidden_Egg_Hunt/play-games.md#vim2048
[vim2048-instruction]: en_US/hidden_Egg_Hunt/play-games.md#instruction
