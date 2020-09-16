![nightfly](https://raw.githubusercontent.com/bluz71/misc-binaries/master/headings/nightfly.png)
==========

_nightfly_ is a dark GUI color scheme for Vim and Neovim heavily inspired by
Sarah Drasner's [Night Owl](https://github.com/sdras/night-owl-vscode-theme)
theme mixed with a dash of my own
[moonfly](https://github.com/bluz71/vim-moonfly-colors) theme.

Be aware, the _nightfly_ color scheme does incrementally change from time to
time, primarily with regard to language and plugin theming.

Prerequisites
-------------

_nightfly_ is a **GUI-only** Vim color scheme.

A GUI client, such as gvim, **or** a modern terminal version of Vim/Neovim, with
`termguicolors` enabled in a true-color terminal, will be required. Details
about true-color terminals are listed below.

_nightfly_ explicitly does **not** support the 256 color `cterm` version of Vim,
due to the number of custom colors required. 256 color terminals only allow 16
custom colors. I encourage terminal users to use a true-color terminal, such as:
[iTerm2](https://iterm2.com), [GNOME
Terminal](https://wiki.gnome.org/Apps/Terminal) or
[Alacritty](https://github.com/alacritty/alacritty), and enable the
`termguicolors` option.

Primary Colors
--------------

| Normal     | Color                                                       | Bright     | Color                                                       |
| ---------- | ----------------------------------------------------------- | -----------| ----------------------------------------------------------- |
| Background | ![background](https://placehold.it/64/011627/000000?text=+) | Foreground | ![foreground](https://placehold.it/64/c3ccdc/000000?text=+) |
| Red        | ![red](https://placehold.it/64/fc514e/000000?text=+)        | Watermelon | ![watermelon](https://placehold.it/64/ff5874/000000?text=+) |
| Green      | ![green](https://placehold.it/64/a1cd5e/000000?text=+)      | Emerald    | ![emerald](https://placehold.it/64/21c7a8/000000?text=+)    |
| Yellow     | ![yellow](https://placehold.it/64/e3d18a/000000?text=+)     | Tan        | ![tan](https://placehold.it/64/ecc48d/000000?text=+)        |
| Blue       | ![blue](https://placehold.it/64/82aaff/000000?text=+)       | Purple     | ![purple](https://placehold.it/64/ae81ff/000000?text=+)     |
| Violet     | ![violet](https://placehold.it/64/c792ea/000000?text=+)     | Turquoise  | ![turquoise](https://placehold.it/64/7fdbca/000000?text=+)  |
| Orange     | ![orange](https://placehold.it/64/f78c6c/000000?text=+)     | Peach      | ![peach](https://placehold.it/64/ffcb8b/000000?text=+)      |

Screenshots
-----------

### Ruby

<img width="800" alt="ruby" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/nightfly/ruby_nightfly.png">

### JavaScript

<img width="800" alt="javascript" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/nightfly/javascript_nightfly.png">

The font in use is [Iosevka](https://github.com/be5invis/Iosevka).

Languages explicitly styled
---------------------------

- C/C++
- Clojure
- CoffeeScript
- Crystal
- Elixir
- Elm
- Dart
- Go
- Haskell
- Java
- [JavaScript](https://github.com/pangloss/vim-javascript)
- Lua
- [Markdown](https://github.com/plasticboy/vim-markdown)
- PHP
- PureScript
- Python
- Ruby
- Rust
- Scala
- Shell
- [TypeScript](https://github.com/HerringtonDarkholme/yats.vim)

Plugins explicity styled
------------------------

- [ALE](https://github.com/w0rp/ale)
- [BufExplorer](https://github.com/jlanzarotta/bufexplorer)
- [CtrlP](https://github.com/ctrlpvim/ctrlp.vim)
- [fern.vim](https://github.com/lambdalisue/fern.vim)
- [GitGutter](https://github.com/airblade/vim-gitgutter)
- [NERDTree](https://github.com/scrooloose/nerdtree)
- [Neomake](https://github.com/neomake/neomake)
- [Signify](https://github.com/mhinz/vim-signify)
- [Tagbar](https://github.com/majutsushi/tagbar)
- [clever-f](https://github.com/rhysd/clever-f.vim)
- [fzf.vim](https://github.com/junegunn/fzf.vim)
- [indentLine](https://github.com/Yggdroot/indentLine) (please set `let g:indentLine_setColors = 0` in your _vimrc_)
- [vimfiler](https://github.com/Shougo/vimfiler.vim)

Installation
------------

Use your favoured plugin manager to install **bluz71/vim-nightfly-guicolors**
then set the colorscheme in your _vimrc_ file.

If using [vim-plug](https://github.com/junegunn/vim-plug) do the following:

1. Add `Plug 'bluz71/vim-nightfly-guicolors'` to your _vimrc_
2. Run `:PlugInstall`
3. Add `colorscheme nightfly` to your _vimrc_, make sure this line appears
   **after** the _Plug_ declaration.

Status line
-----------

The _nightfly_ color scheme supports
[lightline.vim](https://github.com/itchyny/lightline.vim). To enable the
_nightfly_ lightline colorscheme, after the _lightline.vim_ plugin has been
installed, please add the following to your _vimrc_:

```viml
let g:lightline = { 'colorscheme': 'nightfly' }
```

The _nightfly_ color scheme also supports
[vim-airline](https://github.com/vim-airline/vim-airline). With modern versions
of _vim-airline_ the _nightfly_ theme will be automatically loaded.

Alternatively,
[vim-moonfly-statusline](https://github.com/bluz71/vim-moonfly-statusline) is
available for those that want a simple yet informative status line. After the
_vim-moonfly_statusline_ plugin has been installed, please add the following to
your _vimrc_:

```viml
let g:moonflyIgnoreDefaultColors = 1
```

This option will tell _moonfly-statusline_ to not use the default
[moonfly](https://github.com/bluz71/vim-moonfly-colors) colors of that plugin,
but instead use the specified `statusline` colors defined by this _nightfly_
color scheme.

Options
-------

The `g:nightflyCursorColor` option specifies whether to color the cursor or not.
By default the cursor will **NOT** be colored. If you prefer a colored cursor
then add the following to your _vimrc_:

```viml
let g:nightflyCursorColor = 1
```

The `g:nightflyTerminalColors` option specifies whether to use the nightfly
color palette in `:terminal` windows when `termguicolors` is set. By default
this option is **enabled**. If you prefer not to use the nightfly color palette
for the first 16 terminal colors then add the following to your _vimrc_:

```viml
let g:nightflyTerminalColors = 0
```

The `g:nightflyUnderlineMatchParen` option specifies whether to underline
matching parentheses. By default this option is **disabled**. If you want to
underline matching parentheses then add the following to your _vimrc_:

```viml
let g:nightflyUnderlineMatchParen = 1
```

The `g:nightflyUndercurls` option specifies whether to use undercurls for
spelling and linting errors in GUI versions of Vim, including terminal Vim with
`termguicolors` set. By default this option is **enabled**. If you do not like
the appearance of undercurls then add the following to your _vimrc_:

```viml
let g:nightflyUndercurls = 0
```

The `g:nightflyItalics` option specifies whether to use italics for comments and
certain html elements in GUI versions of Vim, including terminal Vim with
`termguicolors` set. By default this option is **enabled**. If you do not like
the appearance of italics then add the following to your _vimrc_:

```viml
let g:nightflyItalics = 0
```

True Color Terminals
--------------------

Many modern terminals support [24-bit true
colors](https://gist.github.com/XVilka/8346728). Current versions of Vim and
Neovim on such terminals support true colors when `set termguicolors` is
enabled.

A list of common terminals that support true colors:

- [iTerm2](http://www.iterm2.com)
- [GNOME Terminal](https://wiki.gnome.org/Apps/Terminal)
- [Windows Terminal](https://github.com/Microsoft/Terminal)
- [Alacritty](https://github.com/alacritty/alacritty)
- [kitty](https://sw.kovidgoyal.net/kitty/index.html)
- [konsole](https://konsole.kde.org)
- [PuTTY](https://putty.org)
- [mintty](https://mintty.github.io)

:bomb: _Terminal.app_ on macOS and _xterm_ on Unix do **not** support true
colors.

On terminals that support true colors, and when `termguicolors` is set, the
_nightfly_ color scheme will emit the correct theme colors.

For the _nightfly_ color scheme to display correctly inside _tmux_ the following
setting will be required in _~/.tmux.conf_:

```
set -ga terminal-overrides ',xterm-256color:Tc'
```

Vim, as against Neovim, inside _tmux_, will also require the following setting
be added to _vimrc:_

```viml
let &t_8f = "\<Esc>[38;2;%lu;%lu;%lum"
let &t_8b = "\<Esc>[48;2;%lu;%lu;%lum"
```

Terminal Themes
---------------

A collection of _nightfly_-flavoured terminal themes are provided:

- _iTerm2_ users on macOS can import
  [this](terminal_themes/nightfly.itermcolors) color scheme

- _GNOME Terminal_ users can run
  [this](terminal_themes/gnome-terminal-nightfly.sh) script to create a
  _Nightfly_ profile. Before executing the script, please install the
  `dconf-cli` command line utility for modern versions of Gnome (3.28 and
  later), for example `sudo apt install dconf-cli`. After executing the script,
  please set the _cursor_ and _selection_ colors by hand, with the appropriate
  color values listed below, in `Preferences` / `Nightfly` / `Colors`.

- [Alacritty](https://github.com/alacritty/alacritty) users can copy
  [this](terminal_themes/alacritty.yml) theme into their `alacritty.yml`
  configuration.

- [kitty](https://sw.kovidgoyal.net/kitty) users can use
  [this](terminal_themes/kitty-theme.conf) theme

For other terminals please configure appropriately with the following colors:

| Type           | Category        | Value     | Color                                                       |
|----------------|-----------------|-----------|-------------------------------------------------------------|
| Background     | Background      | `#011627` | ![background](https://placehold.it/32/011627/000000?text=+) |
| Foreground     | Foreground      | `#acb4c2` | ![background](https://placehold.it/32/acb4c2/000000?text=+) |
| Bold           | Bold            | `#eeeeee` | ![background](https://placehold.it/32/eeeeee/000000?text=+) |
| Cursor         | Cursor          | `#9ca1aa` | ![background](https://placehold.it/32/9ca1aa/000000?text=+) |
| Cursor Text    | Cursor Text     | `#080808` | ![background](https://placehold.it/32/080808/000000?text=+) |
| Selection      | Selection       | `#b2ceee` | ![background](https://placehold.it/32/b2ceee/000000?text=+) |
| Selection Text | Selection Text  | `#080808` | ![background](https://placehold.it/32/080808/000000?text=+) |
| Color 1        | Black (normal)  | `#1d3b53` | ![background](https://placehold.it/32/1d3b53/000000?text=+) |
| Color 2        | Red (normal)    | `#fc514e` | ![background](https://placehold.it/32/fc514e/000000?text=+) |
| Color 3        | Green (normal)  | `#a1cd5e` | ![background](https://placehold.it/32/a1cd5e/000000?text=+) |
| Color 4        | Yellow (normal) | `#e3d18a` | ![background](https://placehold.it/32/e3d18a/000000?text=+) |
| Color 5        | Blue (normal)   | `#82aaff` | ![background](https://placehold.it/32/82aaff/000000?text=+) |
| Color 6        | Purple (normal) | `#c792ea` | ![background](https://placehold.it/32/c792ea/000000?text=+) |
| Color 7        | Cyan (normal)   | `#7fdbca` | ![background](https://placehold.it/32/7fdbca/000000?text=+) |
| Color 8        | White (normal)  | `#a1aab8` | ![background](https://placehold.it/32/a1aab8/000000?text=+) |
| Color 9        | Black (bright)  | `#7c8f8f` | ![background](https://placehold.it/32/7c8f8f/000000?text=+) |
| Color 10       | Red (bright)    | `#ff5874` | ![background](https://placehold.it/32/ff5874/000000?text=+) |
| Color 11       | Green (bright)  | `#21c7a8` | ![background](https://placehold.it/32/21c7a8/000000?text=+) |
| Color 12       | Yellow (bright) | `#ecc48d` | ![background](https://placehold.it/32/ecc48d/000000?text=+) |
| Color 13       | Blue (bright)   | `#82aaff` | ![background](https://placehold.it/32/82aaff/000000?text=+) |
| Color 14       | Purple (bright) | `#ae81ff` | ![background](https://placehold.it/32/ae81ff/000000?text=+) |
| Color 15       | Cyan (bright)   | `#7fdbca` | ![background](https://placehold.it/32/7fdbca/000000?text=+) |
| Color 16       | White (bright)  | `#d6deeb` | ![background](https://placehold.it/32/d6deeb/000000?text=+) |

Color Values
------------

RGB values for the _nightfly_ colors:

| Name       | Value    | Color                                                      | Name       | Value    | Color                                                      |
| ---------- |----------| -----------------------------------------------------------| ---------- |----------| -----------------------------------------------------------|
| Red        | `fc514e` | ![background](https://placehold.it/32/fc514e/000000?text=+)| Background | `011627` | ![background](https://placehold.it/32/011627/000000?text=+)|
| Green      | `a1cd5e` | ![background](https://placehold.it/32/a1cd5e/000000?text=+)| Foreground | `c3ccdc` | ![background](https://placehold.it/32/c3ccdc/000000?text=+)|
| Yellow     | `e3d18a` | ![background](https://placehold.it/32/e3d18a/000000?text=+)| Black Blue | `081e2f` | ![background](https://placehold.it/32/081e2f/000000?text=+)|
| Blue       | `82aaff` | ![background](https://placehold.it/32/82aaff/000000?text=+)| Dark Blue  | `092236` | ![background](https://placehold.it/32/092236/000000?text=+)|
| Violet     | `c792ea` | ![background](https://placehold.it/32/c792ea/000000?text=+)| Deep Blue  | `0e293f` | ![background](https://placehold.it/32/0e293f/000000?text=+)|
| Orange     | `f78c6c` | ![background](https://placehold.it/32/f78c6c/000000?text=+)| Slate Blue | `2c3043` | ![background](https://placehold.it/32/2c3043/000000?text=+)|
| Watermelon | `ff5874` | ![background](https://placehold.it/32/ff5874/000000?text=+)| Regal Blue | `1d3b53` | ![background](https://placehold.it/32/1d3b53/000000?text=+)|
| Emerald    | `21c7a8` | ![background](https://placehold.it/32/21c7a8/000000?text=+)| Cyan Blue  | `296596` | ![background](https://placehold.it/32/296596/000000?text=+)|
| Tan        | `ecc48d` | ![background](https://placehold.it/32/ecc48d/000000?text=+)| Steel Blue | `4b6479` | ![background](https://placehold.it/32/4b6479/000000?text=+)|
| Purple     | `ae81ff` | ![background](https://placehold.it/32/ae81ff/000000?text=+)| Grey Blue  | `7c8f8f` | ![background](https://placehold.it/32/7c8f8f/000000?text=+)|
| Turquoise  | `7fdbca` | ![background](https://placehold.it/32/7fdbca/000000?text=+)| Cadet Blue | `a1aab8` | ![background](https://placehold.it/32/a1aab8/000000?text=+)|
| Peach      | `ffcb8b` | ![background](https://placehold.it/32/ffcb8b/000000?text=+)| White Blue | `d6deeb` | ![background](https://placehold.it/32/d6deeb/000000?text=+)|

Tip: Relative Number Column Highlighting only for the Active Window
-------------------------------------------------------------------

Historically, when `relativenumber` was set whilst `cursorline` was not set,
Vim would automatically highlight the cursor line in the number column with
the `CursorLineNR` highlight group. However, newer versions of Vim no longer
do that by default, not unless `cursorline` is set and the new `cursorlineopt`
option is also set accordingly.

At the same time I also like disabling `relativenumber` for inactive windows.

To achieve all that please add something similar to the following to your
_vimrc_:

```viml
set relativenumber
if exists('&cursorlineopt')
    set cursorlineopt=number
    set cursorline
endif

function! RelativeNumberActivity(active)
    if a:active == v:true
        setlocal relativenumber
        if exists('&cursorlineopt')
            setlocal cursorline
        endif
    else
        setlocal norelativenumber
        if exists('&cursorlineopt')
            setlocal nocursorline
        endif
    endif
endfunction

augroup CustomWindowActivity
    autocmd!
    autocmd WinEnter * call RelativeNumberActivity(v:true)
    autocmd WinLeave * call RelativeNumberActivity(v:false)
augroup END
```

Feel free to change, or ignore, per your needs.

License
-------

[MIT](https://opensource.org/licenses/MIT)
