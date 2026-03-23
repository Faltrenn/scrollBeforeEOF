# Scroll Before EOF

[ScrollEOF](https://github.com/Aasim-A/scrollEOF.nvim) broke on my config in Neovim 0.12, so i made this to replace him.

## How this work

The plugin gets the amount of lines of buffer, the height of window, the current row of cursor, considering actual blank spaces, calculates the blank spaces needed, and then, runs `<C-e>` to get a blank line at bottom. Simple as that. If scrollof is higher than half of window height, the plugin will use half of window.

## How to install

### Neovim pack

`` lua
vim.pack.add {{ src="https://github.com/emdrs/scrollBeforeEOF" }}
require("scrollBeforeEOF").setup()
``

### Lazy

`` lua
{ "emdrs/scrollBeforeEOF" }
``

## How to use

This plugin uses `scrolloff` as amount of blank spaces.

`` lua
vim.o.scrolloff = 20
``
