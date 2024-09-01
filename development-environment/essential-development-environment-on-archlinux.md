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

mkdir -p "$HOME/.config"
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

## Wake-on-LAN via NetworkManager

https://wiki.archlinux.org/title/Wake-on-LAN#NetworkManager

NetworkManager provides [Wake-on-LAN ethernet support](https://www.phoronix.com/scan.php?page=news_item&px=NetworkManager-WoL-Control). One way to enable Wake-on-LAN by magic packet is through _nmcli_.
First, search for the name of the wired connection:
```shell
nmcli con show

NAME    UUID                                  TYPE            DEVICE
wired1  612e300a-c047-4adb-91e2-12ea7bfe214e  802-3-ethernet  enp0s25
```

By following, one can view current status of Wake-on-LAN settings:
```shell
nmcli c show "wired1" | grep 802-3-ethernet.wake-on-lan

802-3-ethernet.wake-on-lan:             default
802-3-ethernet.wake-on-lan-password:    --
```

Enable Wake-on-LAN by magic packet on that connection:
```shell
nmcli c modify "wired1" 802-3-ethernet.wake-on-lan magic
```

Then reboot, possibly two times.

## Install Mosh
https://mosh.org

> for mobile devices

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
sudo pacman -S ripgrep
```

## Install ntp
https://wiki.archlinux.org/title/Network_Time_Protocol_daemon

>  Network Time Protocol daemon

```shell
sudo pacman -S ntp
sudo systemctl enable ntpd.service
```