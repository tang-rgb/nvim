## <center> **QWERTY**用户使用的 [NeoVim](https://neovim.io) 配置文件</center>

**Fork in theniceboy/nvim


<center><img src="https://raw.githubusercontent.com/theniceboy/nvim/master/demo.png"></center>

[English Version](./README.md)

请不要只复制这份配置文件夹而不认真看它！请至少阅读一下这份自述文件！

---

第一版翻译: [**EvanMeek**](https://github.com/EvanMeek)

第二版翻译 (当前版本): [**KiteAB**](https://github.com/KiteAB)

<!-- TOC GFM -->

* [安装此配置后你需要做的事](#安装此配置后你需要做的事)
* [安装此配置后你可能想做的事](#安装此配置后你可能想做的事)
	- [首先](#首先)
	- [Python 程序调试 (通过 `vimspector` 实现)](#python-程序调试-通过-vimspector-实现)
	- [配置 `Python` 路径](#配置-python-路径)
	- [标签表](#标签表)
	- [FZF](#fzf)
	- [其它...](#其它)
* [一些奇怪的东西](#一些奇怪的东西)
	- [按 `tx` 然后输入你想要的文字](#按-tx-然后输入你想要的文字)
	- [自定义垂直光标移动](#自定义垂直光标移动)

<!-- /TOC -->

## 安装此配置后你需要做的事
- [ ] 安装 `pynvim` (使用 `pip`)
- [ ] 安装 `nodejs`, 然后在终端输入 `npm install -g neovim`
- [ ] 安装 nerd-fonts (尽管它是可选的，但是安装之后看上去十分地酷)

## 安装此配置后你可能想做的事
### 首先
- [ ] 执行 `:checkhealth`

### Python 程序调试 (通过 `vimspector` 实现)
- [ ] 安装 `debugpy` (使用 `pip`)

### 配置 `Python` 路径
- [ ] 确保你安装了 Python
- [ ] 查看 `_machine_specific.vim` 文件

### 标签表
- [ ] 安装 `ctags` 以获得类/函数/变量的三重支持

### FZF
- [ ] 安装 `fzf`
- [ ] 安装 `ag` (`the_silver_searcher` 需要)

### 其它...
- [ ] 安装 `figlet` 以输入 ASCII 艺术字
- [ ] 安装 `xclip` 以获得系统剪切板访问支持 (仅 `Linux` 与 `xorg` 需要)

## 一些奇怪的东西
### 按 `tx` 然后输入你想要的文字
`tx Hello<Enter>`
```
 _   _      _ _
| | | | ___| | | ___
| |_| |/ _ \ | |/ _ \
|  _  |  __/ | | (_) |
|_| |_|\___|_|_|\___/
```

### 自定义垂直光标移动

此 NeoVim 配置包含了一套对 Colemak 用户量身定制的垂直光标移动, 它位于 `cursor.vim` 中, 并且可以替代 “数字 + 上 / 下” 的案件组合

为了将光标向上移至 `x` 行, 可以按下 `[` 键, 并将 Colemak 键盘布局的中间行 (“arstdhneio”) 视为从 1 到 0 的数字, 按所需的数字, 再按下空格键以跳转至 `x` 行之上

要向下移动光标, 按 `'` 键而不是 `[` 键, 其余部分相同

例:
| 快捷键                  | 行为                  |
| ----------------------- | --------------------- |
| `[` `a` `o` `o` `SPACE` | 将光标向上移动 100 行 |
| `'` `a` `r` `s` `SPACE` | 将光标向下移动123行   |
| `[` `d` `o` `SPACE`     | 将光标向上移动50行    |

**注意: 目前, 使用此移动方式, 你最多只能垂直移动 199 行!**
