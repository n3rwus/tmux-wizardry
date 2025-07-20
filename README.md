# ⚡ My Tmux Configuration for Supreme Terminal Power

A personalized tmux setup featuring:

- 🧭 Vim-style navigation and editing
- 🖱️ Mouse support with click-to-copy clipboard integration (via `xsel`)
- 🎨 Catppuccin theming for a modern terminal look
- 🎛️ Plugin-driven enhancements for smooth pane/window management
- 🧠 Ergonomic keybindings and intuitive workflows

Perfectly optimized for productivity in X11 environments.

---

## 🔧 Plugins Used

| Plugin                                 | Purpose                                   |
|----------------------------------------|-------------------------------------------|
| `tmux-plugins/tpm`                     | Plugin manager                            |
| `tmux-plugins/tmux-sensible`          | Smart default settings                    |
| `christoomey/vim-tmux-navigator`      | Seamless navigation between Vim & tmux    |
| `dreamsofcode-io/catppuccin-tmux`     | Elegant Catppuccin theme styling          |
| `tmux-plugins/tmux-yank`              | Clipboard copy integration                |

> 💡 Tip: Only one Catppuccin plugin is needed—`dreamsofcode-io/catppuccin-tmux` is preferred.

---

## 🛠️ Key Features

### 🖱️ Mouse Bindings
- Double-click to select a word and copy it (`xsel`)
- Triple-click to copy entire lines
- Middle-click pastes from primary selection

### ⚙️ Navigation
- `Shift + Alt + h` — Previous window  
- `Shift + Alt + l` — Next window  
- Prefix remapped from `Ctrl + b` → `Ctrl + Space`

### 📋 Clipboard Integration
- Uses `xsel -i --clipboard` for system-wide copy
- Vi-mode keybinds:
  ```tmux
  bind-key -T copy-mode-vi v send-keys -X begin-selection
  bind-key -T copy-mode-vi C-v send-keys -X rectangle-toggle
  bind-key -T copy-mode-vi y send-keys -X copy-selection-and-cancel
