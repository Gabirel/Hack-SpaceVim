# Play games on SpaceVim

## Table of Contents

* [Play games on SpaceVim](#play-games-on-spacevim)
   * [Game Lists](#game-lists)
   * [Vim2048](#vim2048)
      * [Instruction](#instruction)


## Game Lists

* vim2048

## Vim2048

### Instruction

1. Add config below into your `~/.SpaceVim.d/init.vim`:

```viml
call SpaceVim#layers#load('games')
```

2. Open your vim/neovim, and then you should see this:

![vim2048-install][vim2048-install-ui]

3. Restart vim, and Press `<Space> g 2`:

![vim2048-space][vim2048-space]

![vim2048-space-g][vim2048-space-g]

4. DONE!

![vim2048-finish][vim2048-done]

Reference: [#24][issue-24]


[vim2048-install-ui]: https://cloud.githubusercontent.com/assets/12933851/25666818/33f2b91c-3054-11e7-89e4-2ffdcb6efb35.png
[vim2048-space]: https://cloud.githubusercontent.com/assets/12933851/25666850/51a9faa6-3054-11e7-9807-172841f3721b.png
[vim2048-space-g]: https://cloud.githubusercontent.com/assets/12933851/25666978/a75640d6-3054-11e7-9bc1-97e234460074.png
[vim2048-done]: https://cloud.githubusercontent.com/assets/12933851/25666993/b10681cc-3054-11e7-9872-b0889f7caa6f.png
[issue-24]: https://github.com/Gabirel/Hack-SpaceVim/issues/24

------------

[FAQ](../FAQ.md#faq) | [Index](../../README.md#table-of-contents) | [中文文档](../../README_zh_CN.md#hack-spacevim)
