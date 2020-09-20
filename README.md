## <center>The Ultimate NeoVim Config for [QWERTY] Users</center>

**Fork in theniceboy/nvim**

<center><img src="https://raw.githubusercontent.com/theniceboy/nvim/master/demo.png"></center>

[中文版](./README_cn.md)

Please **DO NOT** just copy this configuration folder without really looking at it! Please, at least, read this README file!

<!-- TOC GFM -->

* [After Installation, You Need To](#after-installation-you-need-to)
* [After Installation, You Might Want To](#after-installation-you-might-want-to)
	- [First of all](#first-of-all)
	- [For Python Debugger (via `vimspector`)](#for-python-debugger-via-vimspector)
	- [Config `Python` path](#config-python-path)
	- [For Taglist:](#for-taglist)
	- [For FZF](#for-fzf)
	- [And also...](#and-also)
* [Keyboard Shortcuts](#keyboard-shortcuts)
	- [1 Basic Editor Features](#1-basic-editor-features)
		+ [1.1 The Most Basics](#11-the-most-basics)
		+ [1.2 Remapped Cursor Movement](#12-remapped-cursor-movement)
		+ [1.3 Remapped Insert Mode Keys](#13-remapped-insert-mode-keys)
		+ [1.4 Remapped Text Manipulating Commands in Normal Mode](#14-remapped-text-manipulating-commands-in-normal-mode)
		+ [1.5 Other Useful Normal Mode Remappings](#15-other-useful-normal-mode-remappings)
		+ [1.6 Remapped Commands in Visual Mode](#16-remapped-commands-in-visual-mode)
	- [2 Window Management](#2-window-management)
		+ [2.1 Creating Window Through Split Screen](#21-creating-window-through-split-screen)
		+ [2.2 Moving the Cursor Between Different Windows](#22-moving-the-cursor-between-different-windows)
		+ [2.3 Resizing Different Windows](#23-resizing-different-windows)
		+ [2.4 Closing Windows](#24-closing-windows)
	- [3 Tab Management](#3-tab-management)
	- [4 Terminal Keyboard Shortcuts](#4-terminal-keyboard-shortcuts)
* [Plugins Keybindings (Screenshots/GIF provided!)](#plugins-keybindings-screenshotsgif-provided)
	- [AutoCompletion](#autocompletion)
		+ [COC (AutoCompletion)](#coc-autocompletion)
		+ [Ultisnips](#ultisnips)
	- [Debugger](#debugger)
		+ [vimspector (debugger-plugin)](#vimspector-debugger-plugin)
	- [File Navigation](#file-navigation)
		+ [coc-explorer (file browser)](#coc-explorer-file-browser)
		+ [rnvimr - file browser](#rnvimr---file-browser)
		+ [FZF - the fuzzy file finder](#fzf---the-fuzzy-file-finder)
		+ [xtabline (the fancy tab line)](#xtabline-the-fancy-tab-line)
	- [Text Editing Plugins](#text-editing-plugins)
		+ [vim-table-mode](#vim-table-mode)
		+ [Undotree](#undotree)
		+ [vim-multiple-cursors](#vim-multiple-cursors)
		+ [vim-surround](#vim-surround)
		+ [vim-subversive](#vim-subversive)
		+ [vim-easy-align](#vim-easy-align)
		+ [AutoFormat](#autoformat)
		+ [vim-markdown-toc (generate table of contents for markdown files)](#vim-markdown-toc-generate-table-of-contents-for-markdown-files)
	- [Navigation Within Buffer](#navigation-within-buffer)
		+ [vim-easy-motion](#vim-easy-motion)
		+ [Vista.vim](#vistavim)
		+ [vim-signiture - Bookmarks](#vim-signiture---bookmarks)
	- [Find and Replace](#find-and-replace)
		+ [Far.vim - find and replace](#farvim---find-and-replace)
	- [Git Related](#git-related)
		+ [vim-gitgutter](#vim-gitgutter)
		+ [fzf-gitignore](#fzf-gitignore)
	- [Others](#others)
		+ [vim-calendar](#vim-calendar)
		+ [Goyo - Work without distraction](#goyo---work-without-distraction)
		+ [suda.vim](#sudavim)
		+ [coc-translator](#coc-translator)
* [Custom Snippets](#custom-snippets)
	- [Markdown](#markdown)
* [Some Weird Stuff](#some-weird-stuff)
	- [Press `tx` and enter your text](#press-tx-and-enter-your-text)
	- [Customized Vertical Cursor Movement](#customized-vertical-cursor-movement)

<!-- /TOC -->

## After Installation, You Need To
- [ ] Install `pynvim` (pip)
- [ ] Install `nodejs`, and do `npm install -g neovim`
- [ ] Install nerd-fonts (actually it's optional but it looks real good)

## After Installation, You Might Want To
### First of all
- [ ] Do `:checkhealth`

### For Python Debugger (via `vimspector`)
- [ ] Install `debugpy` (`pip`)

### Config `Python` path
- [ ] Well, make sure you have python
- [ ] See `_machine_specific.vim`

### For Taglist:
- [ ] Install `ctags` for function/class/variable list

### For FZF
- [ ] Install `fzf`
- [ ] Install `ag` (`the_silver_searcher`)

### And also...
- [ ] Install `figlet` for inputing text ASCII art
- [ ] Install `xclip` for system clipboard access (`Linux` and `xorg` only)

## Keyboard Shortcuts
### 1 Basic Editor Features
#### 1.1 The Most Basics
**`k`** : switchs to **`INSERT`** : mode (same as key `i` in vanilla vim)

**`Q`** : quits current vim window (same as command `:q` in vanilla vim)

**`S`** : saves the current file (same as command `:w` in vanilla vim)

**_IMPORTANT_**

  Since the `i` key has been mapped to `k`, every command (combination) that involves `i` should use `k` instead (for example, `ciw` should be `ckw`).



<img alt="Gif" src="https://raw.githubusercontent.com/terryma/vim-multiple-cursors/master/assets/example1.gif" width="60%" />
<img alt="Gif" src="https://raw.githubusercontent.com/terryma/vim-multiple-cursors/master/assets/example2.gif" width="60%" />
<img alt="Gif" src="https://raw.githubusercontent.com/terryma/vim-multiple-cursors/master/assets/example3.gif" width="60%" />
<img alt="Gif" src="https://raw.githubusercontent.com/terryma/vim-multiple-cursors/master/assets/example4.gif" width="60%" />

#### [vim-surround](https://github.com/tpope/vim-surround)
To add surround (`string` -> `"string"`):
```
string
```
press: `yskw'`:
```
'string'
```

To change surround
```
'string'
```
press: `cs'"`:
```
"string"
```

<img alt="Gif" src="https://two-wrongs.com/image/surround_vim.gif" width="60%" />

#### [vim-subversive](https://github.com/svermeulen/vim-subversive)
New operator: `s`:

You can execute `s<motion>` to substitute the text object provided by the motion with the contents of the default register (or an explicit register if provided). For example, you could execute `skw` to replace the current word under the cursor with the current yank, or `skp` to replace the paragraph, etc.



#### [vim-easy-align](https://github.com/junegunn/vim-easy-align)
Press `ga` + **symbol** in normal or visual mode to align text based on **symbol**

<img alt="Gif" src="https://raw.githubusercontent.com/junegunn/i/master/easy-align/equals.gif" width="60%" />

#### [AutoFormat](https://github.com/Chiel92/vim-autoformat)
Press `\` `f` to format code

#### [vim-markdown-toc (generate table of contents for markdown files)](https://github.com/mzlogin/vim-markdown-toc)
In `markdown` files, type `:Gen` then tab, you'll see your options.

<img alt="Gif" src="https://raw.githubusercontent.com/mzlogin/vim-markdown-toc/master/screenshots/english.gif" width="60%" />

### Navigation Within Buffer
#### [vim-easy-motion](https://github.com/easymotion/vim-easymotion)
Press `'` and a `character` jump to `character` (similar to Emacs' [AceJump](https://www.emacswiki.org/emacs/AceJump))

<img alt="Gif" src="https://f.cloud.github.com/assets/3797062/2039359/a8e938d6-899f-11e3-8789-60025ea83656.gif" width="60%" />

#### [Vista.vim](https://github.com/liuchengxu/vista.vim)
Press `T` to toggle function and variable list

<img alt="Gif" src="https://user-images.githubusercontent.com/8850248/56469894-14d40780-6472-11e9-802f-729ac53bd4d5.gif" width="60%" />

#### [vim-signiture - Bookmarks](https://github.com/kshenoy/vim-signature)
| Shortcut    | Action                          |
|-------------|---------------------------------|
| `m<letter>` | Add/remove mark at current line |
| `m/`        | List all marks                  |
| `mSPACE`    | Jump to the next mark in buffer |
| `mt`        | Add/remove mark at current line |
| `ma`        | Add annotation at current line  |
| `ml`        | Show all bookmarks              |
| `mi`        | Next bookmark                   |
| `mn`        | Previous bookmark               |
| `mC`        | Clear bookmarks                 |
| `mX`        | Clear all bookmarks             |
| `mu`        | Move bookmark up a line         |
| `me`        | Move bookmark down a line       |
| `SPC` `g`   | Move bookmark to line...        |

<img alt="Gif" src="https://camo.githubusercontent.com/bc2bf1746e30c72d7ff5b79331231e8c388d068a/68747470733a2f2f7261772e6769746875622e636f6d2f4d617474657347726f656765722f76696d2d626f6f6b6d61726b732f6d61737465722f707265766965772e676966" width="60%" />

### Find and Replace
#### [Far.vim - find and replace](https://github.com/brooth/far.vim)
Press `SPACE` `f` `r` to search in cwd.

<img alt="Gif" src="https://cloud.githubusercontent.com/assets/9823254/20861878/77dd1882-b9b4-11e6-9b48-8bc60f3d7ec0.gif" width="60%" />

### Git Related
#### [vim-gitgutter](https://github.com/airblade/vim-gitgutter)
| Shortcut        | Action                            |
|-----------------|-----------------------------------|
| `H`             | **Show git hunk at current line** |
| `SPACE` `g` `-` | Go to previous git hunk           |
| `SPACE` `g` `+` | Go to next git hunk               |
| `SPACE` `g` `f` | Fold everything except hunks      |

#### [fzf-gitignore](https://github.com/fszymanski/fzf-gitignore)
Press `Space` `g` `i` to create a `.gitignore` file

<img alt="Png" src="https://user-images.githubusercontent.com/25827968/42945393-96c662da-8b68-11e8-8279-5bcd2e956ca9.png" width="60%" />

<img alt="Png" src="https://raw.githubusercontent.com/airblade/vim-gitgutter/master/screenshot.png" width="60%" />

### Others
#### [vim-calendar](https://github.com/itchyny/calendar.vim)
| Shortcut | Action        |
|----------|---------------|
| `\` `\`  | Show clock    |
| `\` `c`  | Show calendar |

<img alt="Png" src="https://raw.githubusercontent.com/wiki/itchyny/calendar.vim/image/image.png" width="60%" />

#### [Goyo - Work without distraction](https://github.com/junegunn/goyo.vim)
Press `g` `y` to toggle Goyo

<img alt="Png" src="https://raw.github.com/junegunn/i/master/goyo.png" width="60%" />

#### [suda.vim](https://github.com/lambdalisue/suda.vim)
Forgot to `sudo vim ...`? Just do `:sudowrite` or `:sw`

#### [coc-translator](https://github.com/voldikss/coc-translator)
Press `ts` to **translate word under cursor**.

<img alt="Png" src="https://user-images.githubusercontent.com/20282795/72232547-b56be800-35fc-11ea-980a-3402fea13ec1.png" width="60%" />

## Custom Snippets
### Markdown
| Shortcut | What it creates     |
|----------|---------------------|
| `,n`     | ---                 |
| `,b`     | **Bold** text       |
| `,s`     | ~~sliced~~ text     |
| `,i`     | *italic* text       |
| `,d`     | `code block`        |
| `,c`     | big `block of code` |
| `,m`     | - [ ] check mark    |
| `,p`     | picture             |
| `,a`     | [link]()            |
| `,1`     | # H1                |
| `,2`     | ## H2               |
| `,3`     | ### H3              |
| `,4`     | #### H4             |
| `,l`     | --------            |

`,f` to go to the next `<++>` (placeholder)

`,w` to go to the next `<++>` (placeholder) and then press `Enter` for you

## Some Weird Stuff
### Press `tx` and enter your text
`tx Hello<Enter>`
```
 _   _      _ _
| | | | ___| | | ___
| |_| |/ _ \ | |/ _ \
|  _  |  __/ | | (_) |
|_| |_|\___|_|_|\___/
```

### Customized Vertical Cursor Movement

This NeoVim configuration includes a customized vertical cursor movement tailored for Colemak users. It can be located in `cursor.vim`, and it serves as an alternative to the "number + up/down" key combination.

In order to move the cursor up `x` lines, press the `[` key, and treat the middle row of the Colemak keyboard layout ("arstdhneio") as number 1 to 0. Press the numbers that you'd like your cursor to move (`x`) and press the space bar.

To move the cursor down, press the `'` key instead of the `[` key, and the rest would be the same.

Example:
| Shortcut                | Action                         |
|-------------------------|--------------------------------|
| `[` `a` `o` `o` `SPACE` | Move the cursor up 100 lines   |
| `'` `a` `r` `s` `SPACE` | Move the cursor down 123 lines |
| `[` `d` `o` `SPACE`     | Move the cursor up 50 lines    |

**Note: As of now, you may only move vertically up to 199 lines with this key configuration!**

