# Install Python with Anaconda

## on Arch Linux
> https://docs.anaconda.com/free/anaconda/install/linux/#installing-on-linux

### Prerequisites

```shell
pacman -S libxau libxi libxss libxtst libxcursor libxcomposite libxdamage libxfixes libxrandr libxrender mesa-libgl alsa-lib libglvnd
```

### Installation

1. In your browser, download the [Anaconda installer for Linux](https://www.anaconda.com/download).

2. Search for “terminal” in your applications and click to open.

3. (Recommended) [Verify the installer’s data integrity with SHA-256](https://docs.anaconda.com/free/anaconda/reference/hashes/). For more information on hash verification, see [cryptographic hash validation](https://conda.io/projects/conda/en/latest/user-guide/install/download.html#cryptographic-hash-verification).
    - In the terminal, run the following:
```shell
shasum -a 256 /PATH/FILENAME
# Replace /PATH/FILENAME with your installation's path and filename.
```

4. Install for Python 3.7, enter the following:
```shell
# Include the bash command regardless of whether or not you are using the Bash shell
bash ~/Downloads/Anaconda3-2020.05-Linux-x86_64.sh
# Replace ~/Downloads with your actual path
# Replace the .sh file name with the name of the file you downloaded
```    

5. Press Enter to review the license agreement. Then press and hold Enter to scroll.

6. Enter “yes” to agree to the license agreement.

7. Use Enter to accept the default install location, use CTRL+C to cancel the installation, or enter another file path to specify an alternate installation directory. If you accept the default install location, the installer displays `PREFIX=/home/<USER>/anaconda<2/3>` and continues the installation. It may take a few minutes to complete.
    > Note
    > Anaconda recommends you accept the default install location. Do not choose the path as `/usr` for the Anaconda/Miniconda installation.

8. Anaconda recommends you enter “yes” to initialize Anaconda Distribution by running `conda init`. If you enter “no”, then conda will not modify your shell scripts at all. In order to initialize conda after the installation process is done, run the following commands:
```shell
# Replace <PATH_TO_CONDA> with the path to your conda install
# 
source <PATH_TO_CONDA>/bin/conda init fish
```
 For more information, see the [FAQ](https://docs.anaconda.com/free/anaconda/reference/faq/#distribution-faq-linux-path).
 
9. The installer finishes and displays, “Thank you for installing Anaconda<2/3>!”

10. Close and re-open your terminal window for the installation to take effect, or enter the command `source ~/.config/fish/config.fish` to refresh the terminal.

11. You can also control whether or not your shell has the base environment activated each time it opens.
```shell
# The base environment is activated by default
conda config --set auto_activate_base True

# The base environment is not activated by default
conda config --set auto_activate_base False

# The above commands only work if conda init has been run first
# conda init is available in conda versions 4.6.12 and later
``` 

12. [Verify your installation](https://docs.anaconda.com/free/anaconda/install/verify-install/).
    > Note
    > If you install multiple versions of Anaconda, the system defaults to the most current version, as long as you haven’t altered the default install path.

## on macOS

```shell
brew install --cask anaconda
/usr/local/anaconda3/bin/conda init fish
```
