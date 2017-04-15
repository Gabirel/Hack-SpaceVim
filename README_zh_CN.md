[![](https://spacevim.org/img/build-with-SpaceVim.svg)](https://spacevim.org)
[![Build Status](https://travis-ci.org/Gabirel/Hack-SpaceVim.svg?branch=master)](https://travis-ci.org/Gabirel/Hack-SpaceVim)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
[![spacevim-version](https://img.shields.io/badge/spacevim-v0.3.0--dev-ff69b4.svg)](https://spacevim.org)

# Hack-SpaceVim

[SpaceVim][spacevim] | [English Document](README.md) | [Hack-SpaceVim:issue][Hack-SpaceVim:issue-tracker] | [SpaceVim:issue][SpaceVim:issue-tracker]

## 你能从Hack-SpaceVim得到什么

* **手把手**教你如何安装SpaceVim
* 快速地部署开发环境
* 开发者速成
* 帮助你熟悉多到吐的插件
* 让你成为专业的vimmer
* 用SpaceVim征服整个星球
* 告诉你鲜为人知的彩单
* 一些你永远不会知道的技巧（噢，这好像矛盾了 |-:D ）

---------------------------

Table of Contents
=================

1. [在Windows上安装SpaceVim][1]
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
      * [常见问题][1-1-4]
         * [配置环境变量][1-1-4-1]
         * [python不支持][1-1-4-2]
         * [SpaceVim卡顿][1-1-4-3]
         * [vcruntime140.dll错误][1-1-4-4]
         * [Windows上安装繁琐][1-1-4-5]

[1]: zh_CN/installation/installation-for-windows.md
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
[1-1-4]: zh_CN/installation/installation-for-windows.md#%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98
[1-1-4-1]: zh_CN/installation/installation-for-windows.md#%E9%85%8D%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F
[1-1-4-2]: zh_CN/installation/installation-for-windows.md#python%E4%B8%8D%E6%94%AF%E6%8C%81
[1-1-4-3]: zh_CN/installation/installation-for-windows.md#spacevim%E5%8D%A1%E9%A1%BF
[1-1-4-4]: zh_CN/installation/installation-for-windows.md#vcruntime140dll%E9%94%99%E8%AF%AF
[1-1-4-5]: zh_CN/installation/installation-for-windows.md#windows%E4%B8%8A%E5%AE%89%E8%A3%85%E7%B9%81%E7%90%90

[vim-galore]: https://github.com/mhinz/vim-galore
[spacevim]: https://github.com/spacevim/spacevim
[Hack-SpaceVim:issue-tracker]: https://github.com/Gabirel/Hack-SpaceVim/issue
[SpaceVim:issue-tracker]: https://github.com/spacevim/spacevim/issue
