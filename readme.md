# Nanochan - Advanced configurations for GNU nano

This is a personal fork of [scopatz/nanorc](https://github.com/scopatz/nanorc) which is released under GNU GPL v3.0+. The name is derived from GNU nano text editor itself and "changer".

## TOC

* [Features](#features)
	* [Custom Options](#custom-options)
	* [Custom Keybindings](#custom-keybindings)
	* [Syntax Highlighting](#syntax-highlighting)
* [Installation](#installation)
* [Inspiration](#inspiration)
* [Additional Notes](#additional-notes)
* [References](#references)

## Features

* Custom Options

* Custom Keybindings

* Syntax Highlighting

### Custom Options

#### General Options

These options are explicitly turnd on by default. You can modify [nanorc](nanorc) as you wish. You can also turn off some of them with shortcuts without modifying [nanorc](nanorc).

```bash
# wrap lines at blanks when softwrap enabled
set atblanks

# enable autoindent
set autoindent

# display cursor position
set constantshow

# custom color
set errorcolor red,normal

# save search history
set historylog

# display scrollbar
set indicator

# custom color
set keycolor cyan

# show linenumbers
set linenumbers

# mouse support
#set mouse # it doesn't work well on mac

# multibuffer support
set multibuffer

# don't convert files from DOS/Mac format.
set noconvert

# custom color
set numbercolor yellow,normal

# save the positionlog
set positionlog

# enable regex search
set regexp

# enable smarthome
set smarthome

# enable softwrap
set softwrap

# set spellchecker
set speller "aspell -c"

# show stateflags
set stateflags

# custom color
set statuscolor yellow,normal

# tabsize
set tabsize 4

# convert tabs to spaces
set tabstospaces

# custom color
set titlecolor yellow,normal

# these chars are considered as parts of words
set wordchars "_"

# erase marked region
set zap
```

#### Formatter, Linter & Spellchecker

These are optional configurations but default for my own use. You have to install following programs if you use them, but any issues won't occur without installing them.

**Formatter**

* `astyle` (C)

* `go fmt` (Go)

**Linter**

* `clang-format` (C)
* `golangci-lint` (Go)

**Spellchecker**

* `aspell`

### Custom Keybindings

I recommend you to read GNU nano's official document of [nanorc](https://www.nano-editor.org/dist/latest/nanorc.5.html) to understand keybindings and menus.

Custom keybindings written below are only those generally used in the *main* menu. More details are in [nanorc](nanorc)!

#### Policy

* Keep general (semantic) shortcut bindings

* Keep default cursor moving

  * Note that it is difficult to make Vim-like keybindings because users can't change `^H` binding (=backspace)

* Don't use arrow keys

* Don't use Fn keys

* Don't use Insert, Delete, Home, End, PgUp and PgDn keys

#### General Shortcuts

| Shortcuts | Default Keybindings | Nanochan Keybindings |
| --------- | ------------------- | --------------------- |
| copy      | M-6                 | **^C**                |
| paste     | ^U                  | **^V**                |
| cut       | ^K                  | **^X**                |
| exit      | ^X                  | **^Q**                |
| save      | ^S                  | ^S                    |
| undo      | M-U                 | **^Z**                |
| redo      | M-E                 | **^Y**                |

#### Cursor Moving

| Shortcuts | Default Keybindings | Nanochan Keybindings |
| --------- | ------------------- | --------------------- |
| left      | ^B                  | ^B                    |
| right     | ^F                  | ^F                    |
| up        | ^P                  | ^P                    |
| down      | ^N                  | ^N                    |
| pageup    | ^Y                  | **^U** (*up*)         |
| pagedown  | ^V                  | **^D** (*down*)       |
| firstline | M-\                 | **M-Q**               |
| lastline  | M-/                 | **M-W**               |
| prevword  | ^←                  | **^K**                |
| nextword  | ^→                  | **^J**                |

#### A Bit Different From Normal

| Shortcuts    | Default Keybindings | Nanochan Keybindings |
| ------------ | ------------------- | --------------------- |
| wherewas     | ^Q                  | **^\\**               |
| whereis      | ^W                  | **^/**                |
| findprevious | M-Q                 | **M-\\**              |
| findnext     | M-W                 | **M-/**               |
| replace      | M-R                 | **^R**                |
| mark         | M-A                 | **^L**                |
| location     | ^/                  | **^W**                |

#### Additional Tweaks

| Shortcuts  | Default Keybindings | Nanochan Keybindings |
| ---------- | ------------------- | --------------------- |
| select all |  M-\ M-A M-/        | **M-6**               |
| suspend    | ^T ^Z               | **M-Z**               |
| help       | ^G                  | **M-?**               |


### Syntax Highlighting

Syntax highlighting is mainly based on [scopatz/nanorc](https://github.com/scopatz/nanorc) but I may add some additinal syntax highlighting files.

#### Additions

* Hare: [~lmarz/nano-hare](https://git.sr.ht/~lmarz/nano-hare/) released under Unlicense (Public Domain)

## Installation

Please move `$HOME/.nano/` and `$HOME/.nanorc`  to any other directories if exist before installing.

```bash
$ cd $HOME # move to home directory
$ git clone https://github.com/k1s0b3/nanochan.git .nano # clone the repo
$ cp .nano/nanorc .nanorc # copy .nanorc
$ nano # open nano with nanochan!
```

I recommend you to read the [original README](readme-original.md) for reference.

## Inspiration

* [davidhcefx/Modern-Nano-Keybindings](https://github.com/davidhcefx/Modern-Nano-Keybindings)

## Additional Notes

* Neither related to the imageboard *Nanochan* nor other programs named; *Nanochan* or *Nano-chan*.

* Tested on GNU nano v7.2 with iTerm2 on macOS 12.6.1.

## References

* [Cheatsheet for GNU nano](https://www.nano-editor.org/dist/latest/cheatsheet.html)

* [NANORC](https://www.nano-editor.org/dist/latest/nanorc.5.html)
