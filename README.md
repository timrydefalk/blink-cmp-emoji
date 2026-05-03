# blink-cmp-emoji

A [blink.cmp](https://github.com/Saghen/blink.cmp) completion source for Unicode Emoji v17.0 glyphs.

## Requirements

- Neovim 0.10+
- [blink.cmp](https://github.com/Saghen/blink.cmp)

## Installation

#### [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
    'saghen/blink.cmp',
    dependencies = { 'timrydefalk/blink-cmp-emoji' },
    opts = {
        sources = {
            default = { 'emoji' },
            providers = {
                emoji = {
                    module = "blink-cmp-emoji",
                    name = "blink-cmp-emoji",
                    max_items = 10,
                    min_keyword_length = 1,
                    score_offset = 10,
                    opts = {
                        trigger = ":"
                    }
                },
            }
        }
    }
}
```

## Options

| Option | Type | Default | Description |
|---|---|---|---|
| `trigger` | `string` | `:` | Trigger string that activates the source |

```lua
opts = {
    trigger = ':'
}
```

## Usage

Type the trigger character (default `:`) followed by a part of the glyph name to search for an emoji glyph.

<img width="1349" height="1100" alt="emoji" src="https://github.com/user-attachments/assets/b50fd19a-3ebf-4293-85b4-44ac5aed3cdc" />
