# dotfiles
## Prerequisites 
- Install ZSH
```bash
sudo apt install zsh
```
- Verify installation by running `zsh --version`

- Install Starship Prompt
```bash
curl -sS https://starship.rs/install.sh | sh
```

- Install GNU Stow
```bash
sudo apt-get update -y
sudo apt-get install -y stow
```

- Install Zap Plugin Manager
```bash
zsh <(curl -s https://raw.githubusercontent.com/zap-zsh/zap/master/install.zsh) --branch release-v1
```

## Installation

You will need `git` and GNU `stow`

- CD to your `$HOME` directory or `~`
```bash
cd ~
```

- Remove the dotfiles to be Stowed
```bash
rm .bashrc .gitconfig .hushlogin .motd_shown .profile .zshrc
```

- Clone this repo as .dotfiles
```bash
git clone https://github.com/nasheedibrahim/dotfiles .dotfiles
```

- CD to .dotfiles and Initialize and Update the starship submodulde
```bash
cd .dotfiles
```

```bash
git submodule update --init --recursive
```

- Run `stow` to symlink everything or just select what you want
```bash
stow */ # Everything (the '/' ignores the README)
```

```bash
stow zsh # Just my zsh config
```

- Make zsh your default shell: `chsh -s $(which zsh)`
