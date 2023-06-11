# dotfiles
## Prerequisites 
- Install ZSH
```bash
sudo apt install zsh
```
    - Verify installation by running `zsh --version`
    - Make it your default shell: `chsh -s $(which zsh)`

- Install Starship Prompt
```bash
curl -sS https://starship.rs/install.sh | sh
```
**BASH**
```bash
nano ~/.bashrc 
```

Add the following line to the end
```sh
eval "$(starship init bash)"
```

**ZSH**
```bash
nano ~/.zshrc 
```

Add the following line to the end
```sh
eval "$(starship init zsh)"
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

Clone into your `$HOME` directory or `~`

```bash
git clone https://github.com/nasheedibrahim/dotfiles .dotfiles
```

Initialize and Update the starship submodulde
```bash
git submodule update --init --recursive
```

Run `stow` to symlink everything or just select what you want

```bash
stow */ # Everything (the '/' ignores the README)
```

```bash
stow zsh # Just my zsh config
```