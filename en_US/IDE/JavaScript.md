# IDE for JavaScript

## Table of Contents

* [IDE for JavaScript](#ide-for-javascript)
   * [Table of Contents](#table-of-contents)
   * [Requirements](#requirements)
   * [Installation](#installation)
      * [SpaceVim](#spacevim)
      * [Install npm or cnpm](#install-npm-or-cnpm)
      * [Install tern](#install-tern)
      * [Add config into your ~/.SpaceVim.d/init.vim](#add-config-into-your-spacevimdinitvim)
   * [Config](#config)
   * [Credits &amp; Thanks](#credits--thanks)


## Requirements

* SpaceVim
* tern
* tern_for_vim
* nodejs
* npm/cnpm

## Installation

### SpaceVim

Make sure your SpaceVim is up-to-date.

### Install `npm` or `cnpm`

Here are the examples:

**Arch:**

```bash
sudo pacman -S npm nodejs
```

**Fedora:**

```bash
sudo dnf install npm nodejs
```

**Ubuntu:**

```bash
sudo apt install npm nodejs
```

### Install `tern`

You have to install tern since [tern_for_vim](https://github.com/ternjs/tern_for_vim) using [tern](http://ternjs.net/) as a server to provide auto-completion.
(If I was wrong, please tell me. Because I am not a expert of nodejs)

Just Simply run:

```bash
cd ~/.cache/vimfiles/repos/github.com/ternjs/tern_for_vim 
npm install tern
```

**Or**

```bash
cnpm install tern
```

_PS: If you want to execute, please install `cnpm`._

### Add config into your `~/.SpaceVim.d/init.vim`

```viml
call SpaceVim#layers#load('lang#javascript')
```

And restart your vim to let SpaceVim itself to install plugins for you.

_If it takes a long time to install `tern_for_vim`, please install it manually by 3 steps below:_

```bash 
$ cd ~/.cache/vimfiles/repos/github.com/ternjs
$ git clone https://github.com/ternjs/tern_for_vim
$ cd tern_for_vim; npm install
```

## Config

The most important step is about how to configure your environment.

Actually, it's pretty easy.

It has two optinos for config. 

* Option A: `.tern-project`(in the current directory or one of the directories above that **for this project only**)
* Option B: `.tern-config`(**default** in your home directory)

**See more details [here](http://ternjs.net/doc/manual.html#server)**

Here's the example config:

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

**That's it!!!**

## Credits & Thanks

Thanks to [@RenChunhui](https://github.com/renchunhui), I can make this topic happen. I could never reach so for without his unselfish help. 

---------------

[IDE](../IDE) | [FAQ](../FAQ.md#faq) | [Index](../README.md#table-of-contents) | [中文文档](../../README_zh_CN.md#hack-spacevim)
