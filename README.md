<div align="center">
<img src="https://raw.githubusercontent.com/Everblush/assets/main/logo.png" height="200px" width="200px">
</div> 

<h2 align="center">Neovim Lua Colorscheme</h2>
<p>
<h4 align="center" <i>Everblush Lua Port for Neovim</i></h4>
</p>

 <p align="center">
<img src="https://img.shields.io/github/stars/Everblush/everblush.nvim?color=e5c76b&labelColor=22292b&style=for-the-badge">
<img src="https://img.shields.io/static/v1?label=license&message=MIT&color=8ccf7e&labelColor=22292b&style=for-the-badge">
<img src="https://img.shields.io/github/forks/Everblush/everblush.nvim?color=e74c4c&labelColor=1b2224&style=for-the-badge">
</p>


> ** IMPORTANT NOTE **: You need the latest version of neovim to use this, because this is totally written in lua!

## Screenshots
<div align="center">
<img width="700px" height="500px" src="https://github.com/Everblush/assets/blob/main/nvim/nvim-output.png"> 
</div> 

<details>
<summary>More Language Screenshots</summary>

### Bash
<img align="center" width="700px" height="500px" src="https://github.com/Everblush/assets/blob/main/nvim/nvim-shell.png?raw=true"> 
<br>

### Rust 
<img align="center" width="700px" height="500px" src="https://github.com/Everblush/assets/blob/main/nvim/nvim-rust.png?raw=true">
<br> 

### Go 
<img align="center" width="700px" height="500px" src="https://github.com/Everblush/assets/blob/main/nvim/nvim-go.png?raw=true">
<br> 

### css
<img  align="center" width="700px" height="500px" src="https://github.com/Everblush/assets/blob/main/nvim/nvim-css.png?raw=true">
<br> 

</details>

## External Plugin Support

- Telescope
- Nvim Tree
- Tresitter
- Lsp
- Lsp saga
- Coc
- Bufferline
- Illuminate
- Diff
- Git signs
- Git gutter
- Lualine
- Ident-BlankLine

## Installation

You can install this plugin with packer:

```lua
use { 'Everblush/everblush.nvim', as = 'everblush' }
```

Or with vim-plug:

```vim
Plug 'Everblush/everblush.nvim', { 'as': 'everblush' }
```

## Active theme

- To active the theme call this in your neovim config:

### Lua 
```lua
local everblush = require('everblush')

everblush.setup({ nvim_tree = { contrast = true } }) -- or use contrast = false to not apply contrast
```

### Vim script:

```vim
colorscheme everblush
```

> It will set automatically the `vim.opt.termguicolors` to true

## Activating lualine theme

Place this in your lualine config:

```lua
local lualine = require('lualine')

lualine.setup {
  options = {
    theme = 'everblush',
  },
}
```

## Set transparent background

To disable background color use `transparent_background` option

```lua
local everblush = require('everblush')

everblush.setup({ transparent_background = true })
```

## Using the core to get the colors

If you want to get the colors into a lua dictionary

```lua
local everblush = require('everblush.core')
local colors = everblush.get_colors()
```

## Overriding colors

If you want to override and customize the colors for various parts of the theme check out the [config](/lua/everblush/config.lua) and override like so:

```lua
local colors = require('everblush.core').get_colors()

require('everblush').setup({
  override = {
    CursorLineNr = { fg = colors.foreground },
    LineNr = { fg = colors.comment },
  },
})
```

Any other colors can be overriden in a similar way.

## Credits 💝
- [AlphaTechnolog](https://github.com/AlphaTechnolog).
- ]Mangeshrex](https://github.com/Mangeshrex).
