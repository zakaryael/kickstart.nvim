# 🎯 Neovim Learning Roadmap

## Phase 1: Master the Basics (Week 1)

### 1. Complete Neovim Tutor
- Run `:Tutor` first thing
- This interactive tutorial covers essential vim motions

### 2. Learn Core Navigation
- **Basic movement**: `h/j/k/l` (left/down/up/right)
- **Word movements**: `w` (next word), `b` (back word), `e` (end of word)
- **Line movements**: `0` (start), `$` (end), `^` (first non-blank)
- **Text objects**: 
  - `iw` (inner word), `aw` (around word)
  - `ip` (inner paragraph), `ap` (around paragraph)
  - `i"` (inside quotes), `a"` (around quotes)
- Reference your keymaps cheatsheet: `notes/KEYMAPS.md`

### 3. Understand Your File Structure
- `init.lua` - Main configuration file (well-commented!)
- `lua/kickstart/plugins/` - Individual plugin configurations
- `notes/` - Your documentation directory

## Phase 2: Essential Features (Week 2)

### 1. File Navigation
- **Neo-tree file explorer**: `\` to toggle
- **Telescope fuzzy finder**:
  - `<space>sf` - Search files in project
  - `<space>sg` - Search by grep (find text in files)
  - `<space>sw` - Search current word under cursor
  - `<space><space>` - Search open buffers
  - `<space>s.` - Search recent files

### 2. LSP & Code Intelligence
Already configured for: C++ (clangd), Python (pyright), TypeScript (ts_ls)
- **Navigation**:
  - `grd` - Go to definition
  - `grr` - Find references
  - `gri` - Go to implementation
  - `K` - Hover documentation
- **Refactoring**:
  - `grn` - Rename symbol
  - `gra` - Code actions
- **Symbols**:
  - `gO` - Document symbols
  - `gW` - Workspace symbols

### 3. Enable Key Plugins
From your TODO list - uncomment these in init.lua:
- Line 978: `require 'kickstart.plugins.indent_line'` - Visual indent guides
- Line 979: `require 'kickstart.plugins.autopairs'` - Auto-close brackets
- Line 981: `require 'kickstart.plugins.gitsigns'` - Git integration keymaps

## Phase 3: Productivity Boost (Week 3-4)

### 1. Text Manipulation
- **Mini.surround** (already enabled):
  - `saiw)` - Surround word with parentheses
  - `sd'` - Delete surrounding quotes
  - `sr)"` - Replace parentheses with quotes
- **Mini.ai** - Enhanced text objects:
  - `vaf` - Select around function
  - `diq` - Delete inside quotes (any type)

### 2. Git Integration
After enabling gitsigns keymaps:
- `]c` / `[c` - Navigate between git changes
- `<leader>hs` - Stage hunk
- `<leader>hr` - Reset hunk
- `<leader>hp` - Preview hunk

### 3. Autocompletion (Blink.cmp)
- `<C-n>` / `<C-p>` - Navigate completion items
- `<C-y>` - Accept completion
- `<C-space>` - Trigger completion/documentation
- `<Tab>` / `<S-Tab>` - Navigate snippet placeholders

## Phase 4: Advanced Customization (Week 5+)

### 1. Language-Specific Setup
- **Formatters** (Conform.nvim):
  - `<leader>f` - Format buffer
  - Configure per-language formatters in init.lua:769-776
- **Linters**: Enable lint.lua for code quality checks
- **Debugging**: Enable debug.lua for DAP support

### 2. Personal Workflow
- **Custom keymaps**: Add your own in init.lua after line 169
- **Theme customization**: Modify Tokyo Night settings (init.lua:884-899)
- **Additional plugins**: Add to the lazy.nvim setup (init.lua:248)

### 3. Advanced Features
- **Diagnostic navigation**: 
  - Add `[d` / `]d` keymaps for error navigation
- **Terminal integration**: 
  - `:terminal` or custom keymaps
- **Session management**: 
  - Consider adding a session plugin

## 📚 Key Resources

- `:help` - Neovim's built-in documentation
- `<space>sh` - Search help topics with Telescope
- `:checkhealth` - Diagnose configuration issues
- `:Mason` - Manage language servers and tools
- `:Lazy` - Manage plugins

## 💡 Pro Tips

1. **Read the comments**: Your init.lua has excellent inline documentation
2. **Discover keymaps**: Use `<space>sk` to search all keymaps
3. **Track progress**: Update notes/TODO.md as you complete tasks
4. **Version control**: Commit changes frequently for easy rollback
5. **Learn incrementally**: Don't try to memorize everything at once
6. **Practice deliberately**: Pick one feature per day to master

## 🎓 Learning Resources

- [Learn Lua in Y minutes](https://learnxinyminutes.com/docs/lua/) - Quick Lua primer
- `:help lua-guide` - Neovim's Lua integration guide
- [Neovim documentation](https://neovim.io/doc/)
- Kickstart.nvim discussions on GitHub

## 🚀 Tmux + Neovim Integration

Since you're using tmux, here are some powerful combinations:

### Essential Tmux + Neovim Workflows
- **Project switching**: Use tmux sessions per project
- **Split workflows**: Tmux panes for terminal/tests, Neovim for editing
- **Background processes**: Run servers/watchers in tmux panes
- **Copy/paste integration**: Ensure clipboard works between tmux/nvim/system

### Recommended Tmux Config Additions
- Set vi-mode for consistency: `set-window-option -g mode-keys vi`
- Better prefix key: `set -g prefix C-a`
- Smart pane switching with vim-like keys
- Consider tmux plugins: resurrect, continuum for session persistence

### Advanced Integration
- Look into `vim-tmux-navigator` for seamless pane navigation
- Use `tmux send-keys` for test runners
- Create project-specific tmux layouts

Remember: Use TODO.md to track what you want to learn next!