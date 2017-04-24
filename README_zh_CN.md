[![](https://spacevim.org/img/build-with-SpaceVim.svg)](https://spacevim.org)
[![Build Status](https://travis-ci.org/Gabirel/Hack-SpaceVim.svg?branch=master)](https://travis-ci.org/Gabirel/Hack-SpaceVim)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
[![spacevim-version](https://img.shields.io/badge/spacevim-v0.3.0--dev-ff69b4.svg)](https://spacevim.org)

# Hack-SpaceVim

[SpaceVim][spacevim] | [English Document](README.md) | [Hack-SpaceVim:issue][Hack-SpaceVim:issue-tracker] | [SpaceVim:issue][SpaceVim:issue-tracker]

## 你能从Hack-SpaceVim得到什么

* **手把手**教你如何安装SpaceVim :metal:
* 快速地部署开发环境 :trollface:
* 开发者速成 :sunglasses:
* 帮助你熟悉多到吐的插件 :massage_woman:
* 让你成为专业的vimmer :muscle:
* 用SpaceVim征服整个星球 :new_moon_with_face:
* 告诉你鲜为人知的彩蛋 :scream:
* 一些你永远不会知道的技巧（噢，这好像矛盾了 :smirk:）

---------------------------

Table of Contents
=================

1. [在Windows上的SpaceVim][1]
    * [在Windows上安装SpaceVim][1-1]
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
3.  [常见问题][faq]
    * [Windows][faq-windows]
      * [配置环境变量][set-up-your-path]
      * [python不支持][without-python-support]
      * [SpaceVim卡顿][spacevim-gets-frozen-easily]
      * [vcruntime140.dll错误][vcruntime140dll-error]
      * [Windows上安装繁琐][installing-on-windows-is-too-complicated]
      * [Exuberant ctags未找到][exuberant-ctags-not-found-windows]
    * [Linux][faq-linux]
      * [Exuberant ctags未找到][exuberant-ctags-not-found-linux]

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

[faq]: zh_CN/FAQ.md#常见问题
[faq-windows]: zh_CN/FAQ.md#windows
[set-up-your-path]: zh_CN/FAQ.md#配置环境变量
[without-python-support]: zh_CN/FAQ.md#python不支持
[spacevim-gets-frozen-easily]: zh_CN/FAQ.md#spacevim卡顿
[vcruntime140dll-error]: zh_CN/FAQ.md#vcruntime140dll错误
[installing-on-windows-is-too-complicated]: zh_CN/FAQ.md#windows上安装繁琐
[exuberant-ctags-not-found-windows]: zh_CN/FAQ.md#exuberant-ctags未找到
[faq-linux]: zh_CN/FAQ.md#linux
[exuberant-ctags-not-found-linux]: zh_CN/FAQ.md#exuberant-ctags未找到-1

[vim-galore]: https://github.com/mhinz/vim-galore
[spacevim]: https://github.com/spacevim/spacevim
[Hack-SpaceVim:issue-tracker]: https://github.com/Gabirel/Hack-SpaceVim/issue
[SpaceVim:issue-tracker]: https://github.com/spacevim/spacevim/issue
