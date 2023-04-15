https://github.com/AstroNvim/AstroNvim

Setup nvim (develop version): 

`brew install --HEAD neovim`

Update the develop version

`brew upgrade neovim --fetch-HEAD` 

Backup current nvim and share folder

```
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
```

Clone astro

```
git clone --depth 1 https://github.com/AstroNvim/AstroNvim ~/.config/nvim
nvim
```

