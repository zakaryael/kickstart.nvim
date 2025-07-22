# Neovim Sessions Log

## Session: 2025-07-22
### Actions:
- Fixed gitsigns.nvim error: `rm -rf ~/.local/share/nvim/lazy/gitsigns.nvim`
- Reinstalled via `:Lazy sync`
- Identified C-hjkl conflict in `~/.config/skhd/skhdrc` lines 17-18
- Removed ctrl-h/l bindings from skhdrc
- Found vim-tmux-navigator in `.tmux.conf` handles C-hjkl navigation
- Note: Yabai space nav requires SIP disabled