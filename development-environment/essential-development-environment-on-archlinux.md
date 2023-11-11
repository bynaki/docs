# Essential Development Environment on ArchLinux

## Install Sudo

```bash
pacman -S sudo
```

## Install base-devel

```bash
sudo pacman -S base-devel
```

## Set Path Environments

```bash
# devenv path
export DEVENV="$HOME/devenv"

# XDG Base Directory
# https://wiki.archlinux.org/index.php/XDG_Base_Directory
export XDG_CONFIG_HOME="$HOME/.config"
export XDG_DATA_HOME="$HOME/.local/share"

mkdir "$HOME/.config"
mkdir -p "$HOME/.local/share"
```

## Install OpenSSH
```shell
sudo pacman -S openssh
```

## Generate a new SSH key

[Generating a new SSH key and adding it to the ssh-agent - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

## Add a new SSH key to your GitHub account

[Adding a new SSH key to your GitHub account - GitHub Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Install Git

[Git](https://git-scm.com/)

```bash
sudo pacman -S git
```

## Clone DevEnv Git Repository

```shell
git clone https://github.com/bynaki/devenv.git $DEVENV
```

## Git Configure Symbolic Link

```bash
ln -sf $DEVENV/.gitconfig ~/.gitconfig
```

## Install & Configure netctl

> for wol and static ip

```shell
sudo pacman -S netctl
sudo ln -sf $DEVENV/config/netctl-profile /etc/netctl/netctl-profile
sudo netctl restart netctl-profile
sudo netctl reenable netctl-profile
```

## Install Mosh
https://mosh.org

```shell
sudo pacman -S mosh
```

## Install Neofetch

```shell
sudo pacman -S neofetch
```

## Install ripgrep
[https://github.com/BurntSushi/ripgrep](https://github.com/BurntSushi/ripgrep)

> It’s necessary for Neovim.

```bash
brew install ripgrep
```