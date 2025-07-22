# Gitsigns Practice Guide

## Prerequisites
1. Restart Neovim or source init.lua (`:source %`)
2. Make sure you have uncommitted changes in a file

## Create Test Changes
1. Open any tracked file (e.g., `notes/TODO.md`)
2. Make some changes:
   - Add a new line
   - Modify an existing line
   - Delete a line

## Practice Navigation
- `]c` - Jump to next change (repeat to cycle through all changes)
- `[c` - Jump to previous change

## Practice Actions
With cursor on a changed line:
- `<space>hp` - Preview what changed (popup window)
- `<space>hs` - Stage this specific change
- `<space>hr` - Undo/reset this specific change

## Visual Indicators
Look for these in the left gutter:
- `+` Green - Added lines
- `~` Blue - Modified lines
- `_` Red - Deleted lines indicator

## Advanced Features
- `<space>hb` - See who last changed this line (git blame)
- `<space>tb` - Toggle inline blame (shows on every line)
- `<space>hd` - Show full file diff

## Quick Exercise
1. Edit this file - add your name below:
   - Name: [Your name here]
2. Use `]c` to jump to your change
3. Use `<space>hp` to preview it
4. Use `<space>hs` to stage just that change
5. Check with `git status` in terminal

## Tips
- Changes must be saved to file (`:w`) to see git hunks
- Staged changes won't show as hunks anymore
- Use `<space>hu` to unstage if needed