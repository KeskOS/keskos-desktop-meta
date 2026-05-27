# keskos-desktop-meta

`keskos-desktop-meta` is the default Plasma desktop bundle for KeskOS and depends on the package names produced by the desktop stack repos.

## What this is

This repository builds a pacman meta package. The package itself is empty at runtime and exists only to pull in a curated group of packages through dependencies.

## Role in KeskOS

Meta package for the default desktop shell and visual stack.

## Package name

```txt
Package: keskos-desktop-meta
Repo: [keskos]
Architecture: any
```

## What it installs or provides

- Installs no runtime files beyond pacman metadata.
- Pulls in its software set entirely through `depends` (and optional `optdepends` where present).

## Commands and launchers

- This package does not install commands, GUI launchers, config files, logs, or systemd units directly.

## Config, logs, and state

- Configuration and logs belong to the packages pulled in by this meta package, not to the meta package itself.

## Dependencies

- Current hard dependencies: `dolphin`, `konsole`, `kwin`, `networkmanager`, `plasma-desktop`, `plasma-nm`, `plasma-workspace`, `powerdevil`, `bluedevil`, `pipewire`, `sddm`, `systemsettings`, `wireplumber`, `xdg-desktop-portal-kde`, `keskos-branding`, `keskos-browser-startpage`, `keskos-kickoff`, `keskos-plasma-layout`, `keskos-plymouth`, `keskos-quickshell-hud`, `keskos-sddm-theme`, `keskos-theme`, and `keskos-workspace-switcher`.
- Build with `makepkg -s --noconfirm`.

## Build

```bash
makepkg -s --noconfirm
```

## Packaging notes

- This repo stays separate from `keskos-desktop`, but it should track the package names produced there.
- It should stay focused on the desktop shell and avoid turning into a grab-bag for optional apps.

## Troubleshooting

- If the desktop is incomplete after install, verify that the required desktop packages were published successfully before blaming the meta package.

## Docs website export notes

- Docs site usage: package-group overview plus the dependency list from this README.
