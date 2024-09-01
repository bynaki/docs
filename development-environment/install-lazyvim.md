# Install LazyVim

## Requirements

### Install Neovim

**on Ubuntu:**
```shell
sudo apt install neovim
```

**on Mac:**
```shell
brew install neovim
```

### Install Git

**on Ubuntu:**
```shell
sudo apt install git
```

**on Mac:**
- type ‘git’ in terminal to install it

### a Nerd Font

https://www.nerdfonts.com

### Install gcc

> a **C** compiler for [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter).

**on Ubuntu:**
```shell
sudo apt install gcc
```

### Install ripgrep

[https://github.com/BurntSushi/ripgrep](https://github.com/BurntSushi/ripgrep)

> for [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)

**on Ubuntu:**
```shell
sudo apt install ripgrep
```

### Install fd

https://github.com/sharkdp/fd

> for [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)

**on Ubuntu:**
```shell
sudo apt install fd-find
```

**on Mac:**
```shell
brew install fd
```


## Configure LazyVim

forked the [LazyVim Starter](https://github.com/LazyVim/starter)

- **Make a backup of your current Neovim files:**
```shell
# required
mv ~/.config/nvim{,.bak}

# optional but recommended
mv ~/.local/share/nvim{,.bak}
mv ~/.local/state/nvim{,.bak}
mv ~/.cache/nvim{,.bak}
```

- **Configure symbol link**
```shell
ln -sf $DEVENV/config/lazy.vim $XDG_CONFIG_HOME/nvim
```

- **Start Neovim!**
```shell
nvim
```

> It is recommended to run `:LazyaHealth` after installation. Thist will load all plugins and check if everything is working correctly.


