# Nvim Config

This is a fork of: kickstart.nvim
https://github.com/nvim-lua/kickstart.nvim

## Fresh setup

For a clean local reset, remove Neovim's cached state and plugin data, then start `nvim` again:

```sh
rm -rf ~/.local/share/nvim ~/.local/state/nvim ~/.cache/nvim
nvim
```

This config bootstraps `lazy.nvim` automatically on first launch.

After the first boot, run:

```vim
:TSInstallRequired
:MasonToolsInstall
```

Treesitter parsers are installed under the first writable Neovim `site` runtime path, which keeps setup predictable even when the default data directory is not writable.

## Merging changes from upstream

I have changed the name of the main branch. It's called `main` in my fork. This is to run `just` commands which expect the HEAD branch to be `main`.

```
git checkout -b merge-original
git pull original master
```
