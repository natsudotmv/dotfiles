# dotfiles
## Installing

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