# keskos-desktop-meta

Meta package for the default KeskOS Plasma desktop shell and visual stack.

This repository stays separate from `keskos-desktop`, but it depends on the package names produced by that consolidated desktop repository.

## Build

```bash
makepkg -s --noconfirm
```

## Notes

- This repo remains its own pacman meta package source.
- It depends on the modular desktop packages published from `https://github.com/KeskOS/keskos-desktop`.
- It intentionally avoids large KDE application meta packages.
