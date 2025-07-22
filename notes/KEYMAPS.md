# Neovim Configuration Keymaps

*Current working keymaps as of initial setup*

## Leader Key
- `<space>` - Leader key

## File Explorer (Neo-tree)
- `\` - Toggle Neo-tree

## File Search (Telescope)
- `<space>sf` - Search files in project
- `<space>sg` - Search by grep (find text in files)
- `<space>sw` - Search current word under cursor
- `<space><space>` - Search open buffers
- `<space>s.` - Search recent files
- `<space>sh` - Search help
- `<space>sk` - Search keymaps
- `<space>/` - Fuzzy search in current buffer
- `<space>sn` - Search Neovim config files

## LSP (Language Server Protocol)
*Note: LSP keymaps use `gr` prefix for grouping*
- `grd` - Go to definition
- `grD` - Go to declaration  
- `grr` - Go to references
- `gri` - Go to implementation
- `grt` - Go to type definition
- `grn` - Rename symbol
- `gra` - Code actions
- `gO` - Document symbols
- `gW` - Workspace symbols
- `<C-t>` - Jump back from definition
- `K` - Hover documentation
- `<space>f` - Format buffer

## Window Management
- `<C-h/j/k/l>` - Navigate between windows

## Git (Gitsigns)
*Currently only visual indicators (keymaps disabled):*
- `+` in gutter - Added lines
- `~` in gutter - Changed lines  
- `_` in gutter - Deleted lines

## Diagnostics (Errors/Warnings)
- `<space>q` - Open diagnostic quickfix list
- `<space>e` - Show diagnostic error (may not work)

## Other
- `<Esc>` - Clear search highlights

## Notes
- Some keymaps may not work yet (diagnostic navigation, gitsigns navigation)
- See TODO.md for planned keymap fixes