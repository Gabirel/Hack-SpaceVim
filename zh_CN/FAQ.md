# 常见问题 

## Table of Contents

   * [常见问题](#常见问题)
      * [Windows](#windows)
         * [配置环境变量](#配置环境变量)
         * [python不支持](#python不支持)
         * [SpaceVim卡顿](#spacevim卡顿)
         * [vcruntime140.dll错误](#vcruntime140dll错误)
         * [Windows上安装繁琐](#windows上安装繁琐)

## Windows

### 配置环境变量

**1. 如何配置环境变量？**

A: *位置：此电脑->属性->高级系统设置->环境变量->系统变量->找到Path->编辑*

![path][path-config]

### python不支持

**2. `echo has('python')`返回值均为0，我该怎么办？**

A: 请检查是否满足以下条件：

* 在cmd.exe中，查看python命令是否存在
* vim是64位，python就必须安装64位；反之亦然
* vim必须要有`+python/dyn`或`+python3/dyn`或者`+python/dyn;+python3/dyn`

### SpaceVim卡顿

**3. 我觉得SpaceVim用起来有点卡顿，怎么回事？**

A: 目前有以下可能性：

* 查看你的Lua本地是否支持，vim是否有+lua支持，如果没有lua支持，neocomplete就不会其作用，而是neocomplcache，这就会造成你的卡顿
* 你所使用的SpaceVim有功能性的bug，可以尝试使用SpaceVim的[issue tracker][spacevim-issue-tracker]来帮助你解决
* 你的配置文件可能不恰当，导致占用了大量的内存和磁盘使用。譬如，nodejs里使用ternjs时候对于`loadEagerly`赋值为`**/*.js`就会造成这种现象
* 某一个插件的bug或者某一个插件和另一个插件产生了冲突，若你怀疑有这种现象，请在[issue tracker][spacevim-issue-tracker]提交来修复该问题

### vcruntime140.dll错误

**4. 我运行gvim后无法启动，报缺少vcruntime140.dll的错误，我该怎么解决？**

A: [点我下载][vcruntime140.dll]，根据自己的操作系统类型选择相应的文件夹：

32位系统位置：`C:\Windows\System32\`

64位系统位置：`C:\Windows\SysWOW64\`


### Windows上安装繁琐

**5. 为什么Windows上安装SpaceVim如此麻烦？有更加简单的步骤吗？**

A: 抱歉！没有！Windows搭建开发环境真的是很麻烦，很不友好，完全不建议在Windows上安装；若安装，请不要去碰Neovim，这是一个禁忌领域！请为了自己的身心健康，请安装Vim

----------------

[索引](README.md#table-of-contents) | [English Document](../README.md#hack-spacevim)

[vcruntime140.dll]: https://www.dllme.com/dll/download/29939/vcruntime140.dll
[path-config]: https://gist.githubusercontent.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/08946a3643606420776fcc3fc4d43da6444806cc/path-config.PNG
[spacevim-issue-tracker]: https://github.com/spacevim/spacevim/issues
