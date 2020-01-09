# IDE for JavaScript

## Table of Contents

   * [IDE for JavaScript](#ide-for-javascript)
      * [Table of Contents](#table-of-contents)
      * [基本要求](#基本要求)
      * [安装](#安装)
         * [SpaceVim](#spacevim)
         * [安装 npm 或 cnpm](#安装-npm-或-cnpm)
         * [安装 tern](#安装-tern)
         * [将配置加到 ~/.SpaceVim.d/init.vim](#将配置加到-spacevimdinitvim)
      * [配置](#配置)
      * [感谢](#感谢)


## 基本要求

* SpaceVim
* tern
* tern_for_vim
* nodejs
* npm/cnpm

## 安装

### SpaceVim

请确认你的SpaceVim是最新的。

### 安装 `npm` 或 `cnpm`

对于国内的环境来说，建议使用`cnpm`的环境。
以下是几个安装例子：

**Arch:**
> sudo pacman -S npm nodejs

**Fedora:**
> sudo dnf install npm nodejs

**Ubuntu:**
> sudo apt install npm nodejs

### 安装 `tern`

你必须要安装tern，因为[tern_for_vim](https://github.com/ternjs/tern_for_vim)是使用[tern](http://ternjs.net/) 来作为自动补全的后端代码的。
（如果我错了，请告诉我。我并不是写nodejs或者前端的高手，这方面不是我的完全领域。）

通过以下命令安装：
> cd ~/.cache/vimfiles/repos/github.com/ternjs/tern_for_vim
> npm install tern

**或者**

> cnpm install tern

_注意: 如果你要使用`cnpm`来安装tern，请先安装 `cnpm`._

### 将配置加到 `~/.SpaceVim.d/init.vim`

```viml
call SpaceVim#layers#load('lang#javascript')
```

并且重启vim，让SpaceVim自己会你安装插件。

_如果SpaceVim花了很久的时间来安装`tern_for_vim`，请通过以下三步进行手动安装：_

> $ cd ~/.cache/vimfiles/repos/github.com/ternjs
> $ git clone https://github.com/ternjs/tern_for_vim
> $ cd tern_for_vim; npm install

## 配置

最重要的一步是怎么配置你的环境。

官方文档是我见过写的最差的文档，特别烦人，说白了，就两点要注意：

对于大部分人来说，主要有两种情况：

* 情况一: `.tern-project`（改文件是在当前或者是在当前文件夹上层里，**只适用于当前的工程文件**)
* 情况二: `.tern-config`(**默认**存在你的家目录下)

**更多细节见 [这里](http://ternjs.net/doc/manual.html#server)**

以下是示例，仅供参考：

```json
{
  "plugins": {
    "node": {},
    "node_resolve": {},
    "es_modules": {},
    "modules": {}
  },
  "libs": [
    "browser",
    "ecma5",
    "ecma6",
    "react"
  ],
  "ecmaVersion": 6
}
```

**Okay，完了！！简单吧**

## 感谢

![ghosting](https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/ac26a110fc873b06d810641f13882f2879821888/meme-ghosting.jpg)

很感谢[@RenChunhui](https://github.com/RenChunhui)无私的帮助，要是没有TA的帮助，我肯定无法完成这个。因为这个tern真的很让人头疼。 

---------------

[IDE](../IDE) | [FAQ](../FAQ.md#faq) | [Index](../README.md#table-of-contents) | [English Document](../../README.md#hack-spacevim)
