# opensuse-windows-environment
This repo describes how to setup a linux, specifically openSUSE, environment on Windows using WSL.

## Shell Prompt

A colorless shell sucks. [Starship](https://starship.rs/) gives a fast an easy configuration.

Install with
```bash
curl -sS https://starship.rs/install.sh | sh
```
and configure your ```~/.bashrc``` to use it but adding 
```bash
eval "$(starship init bash)"
```

## Text Editor

To be able to edit files and code in linux use [neovim](https://neovim.io/).

Install with
```bash
sudo zypper install neovim
```
The clone you neovim config into ```~/.config```

I use [vimplug](https://github.com/junegunn/vim-plug) for my neovim plugins.
Install it with
```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

## Add ENV Variables to PATH

Sometimes when you install things that needs to be added to your PATH
it doesn't automatically happen.
To add something to your PATH add this to your ```~/.bashrc```
```bash
# export PATH=<path>:$PATH
# for example
export PATH=$HOME/.local/bin:$PATH
```
