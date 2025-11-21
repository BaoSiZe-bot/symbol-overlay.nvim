# Introduction

This is an unofficial port of the emacs package [symbols-overlay](https://github.com/wolray/symbol-overlay) in neovim.

# Feature

- Toggle highlight pattern under cursor
- Goto next/prev highlight
- Goto next/prev same pattern
- Query and replace pattern under cursor
- Clear all patterns

# Installation

By [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
    'baosize-bot/symbol-overlay.nvim'
    opts = {},
    keys = {
        {"<leader>ho", require("symbol-overlay").add, desc = "Overlay: add current word" },
        {"<leader>hd", require("symbol-overlay").remove, desc = "Overlay: delete current" },
        {"<leader>hn", require("symbol-overlay").next, desc = "Overlay: next" },
        {"<leader>hN", require("symbol-overlay").prev, desc = "Overlay: prev" },
        {"<leader>hr", require("symbol-overlay").rename, desc = "Overlay: rename (buffer only)" },
        {"<leader>ht", require("symbol-overlay").toggle, desc = "Overlay: toggle current word" },
        {"<leader>h]", require("symbol-overlay").switch_forward, desc = "Overlay: switch to next nearby" },
        {"<leader>h[", require("symbol-overlay").switch_backward, desc = "Overlay: switch to prev nearby" },
    },
}

```

# Configuration

```lua
require("symbol-overlay").setup{
    colors = { -- 10 preset colors
        "SymbolsOverlay1",
        "SymbolsOverlay2",
        "SymbolsOverlay3",
        "SymbolsOverlay4",
        "SymbolsOverlay5",
        "SymbolsOverlay6",
        "SymbolsOverlay7",
        "SymbolsOverlay8",
        "SymbolsOverlay9",
    },
}
```

## Todo

- [ ] Highlight pattern in a text object only
