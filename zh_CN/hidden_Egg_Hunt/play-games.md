# 在SpaceVim上玩游戏
![+1s](https://gist.github.com/Gabirel/b71a01cce86df216abd4fd0968864942/raw/4418cda66a8170e73b0ee8afbd4383db6be057e9/meme-shining-me.jpg)

## Table of Contents

   * [在SpaceVim上玩游戏](#在spacevim上玩游戏)
      * [游戏列表](#游戏列表)
      * [Vim2048](#vim2048)
         * [安装](#安装)

## 游戏列表

* vim2048

## Vim2048

### 安装

1. 把以下配置加入到：`~/.SpaceVim.d/init.vim`

```viml
call SpaceVim#layers#load('games')
```

2. 打开你的vim/neovim，然后你应该会看到这个：

![vim2048-install][vim2048-install-ui]

3. 重启vim，然后按下`<Space> g 2`:

![vim2048-space][vim2048-space]

![vim2048-space-g][vim2048-space-g]

4. 完成！

![vim2048-finish][vim2048-done]

参考: [#24][issue-24]


[vim2048-install-ui]: https://cloud.githubusercontent.com/assets/12933851/25666818/33f2b91c-3054-11e7-89e4-2ffdcb6efb35.png
[vim2048-space]: https://cloud.githubusercontent.com/assets/12933851/25666850/51a9faa6-3054-11e7-9807-172841f3721b.png
[vim2048-space-g]: https://cloud.githubusercontent.com/assets/12933851/25666978/a75640d6-3054-11e7-9bc1-97e234460074.png
[vim2048-done]: https://cloud.githubusercontent.com/assets/12933851/25666993/b10681cc-3054-11e7-9872-b0889f7caa6f.png
[issue-24]: https://github.com/Gabirel/Hack-SpaceVim/issues/24

------------

[常见问题](../FAQ.md#常见问题) | [索引](../../README.md#table-of-contents) | [English Document](../../../README.md#hack-spacevim)
