---
url: https://docs.anaconda.com/anaconda/install/
tags:
  - python
  - anaconda
---

# Install Python with Anaconda

### Install Anaconda on Mac

```bash
brew install anaconda
```

### Install Anaconda on Linux

```shell
# Replace <INSTALLER_VERSION> with the version of the installer file you want to download
# For example, https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh
# All installers can be found at repo.anaconda.com/archive/
curl -O https://repo.anaconda.com/archive/Anaconda3-<INSTALLER_VERSION>-Linux-x86_64.sh

# Include the bash command even if you aren't using the Bash shell
# Replace ~/Downloads with the path to the installer file, if necessary
# Replace <INSTALLER_VERSION> with the version of the installer file
# For example, Anaconda3-2023.09-0-Linux-x86_64.sh
bash ~/Downloads/Anaconda3-<INSTALLER_VERSION>-Linux-x86_64.sh
```

### Add Path Conda

```bash
fish_add_path /opt/homebrew/anaconda3/bin   # sillicon on mac
fish_add_path /usr/local/anaconda3/bin      # intel on mac
fish_add_path $HOME/anaconda3/bin           # linux
```

### Initialize Environment to Fish Shell

```bash
conda init fish
```

### Environment List

```bash
conda env list
```

### Create a Environment

```bash
conda create -n myenv
```

### 가상환경 활성

```bash
conda activate myenv
```

### 가상환경 비활성

```bash
conda deactivate
```

### Login 할때 가상환경 지정

```shell
# in config.fish
conda activate myenv 
```