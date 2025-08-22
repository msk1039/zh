# zh - Zsh History Search

## A fuzzy search tool for your zsh/bash command history using fzf.


https://github.com/user-attachments/assets/cdba73f6-3add-455b-8c7a-cbd7b9bc2b0b



## Features

- **Fuzzy search** through your entire command history
- **Cross-shell support** - works with both zsh and bash
- **Cross-platform support** - words on macos, linux, window(WSL)


## Requirements

- [fzf](https://github.com/junegunn/fzf) - Install with `brew install fzf` (macOS) or `apt install fzf` (Ubuntu)
- [tac](https://www.gnu.org/software/coreutils/) - Install with `brew install coreutils` (macOS) or `apt install coreutils` (Linux)

## Installation

### Manual Installation

1. **Download the script:**
   ```bash
   curl -O https://raw.githubusercontent.com/msk1039/zh/refs/heads/main/zh
   ```

2. **Make it executable:**
   ```bash
   chmod +x zh
   ```

3. **Move to your PATH as `zh`:**
   ```bash
   sudo mv zh /usr/local/bin/zh
   ```

4. **Verify installation:**
   ```bash
   zh
   ```

## Usage

Simply type `zh` in your terminal to open the fuzzy search interface:

```bash
zh
```

- **Search**: Type to filter commands
- **Navigate**: Use arrow keys or Ctrl+J/K
- **Select**: Press Enter to execute the selected command
- **Exit**: Press Esc or Ctrl+C

## How it works

1. Reads your zsh history file (`~/.zhistory`) or bash history (`~/.bash_history`)
2. Removes timestamp prefixes and duplicates (keeping newest)
3. Opens fzf with newest commands first
4. Executes your selected command
