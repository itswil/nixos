# ❄️ NixOS Config

## 👷🏻‍♂️ Setup

From `~` (`/home/USERNAME`), temporarily install GIT and clone this repo:

```
nix-shell -p git
git clone https://github.com/itswil/nixos.git
cd nixos
```

The default `configuration.nix` is in `/etc/nixos`, but we will use this newly downloaded config

### Create a symlink for `hardware-configuration.nix`

```
ln -s /etc/nixos/hardware-configuration.nix .
```

This is necessary because the Rebuild step (next step) requires a `hardware-configuration.nix` to be in the same location as `configuration.nix`

### Rebuild NixOS

```
sudo nixos-rebuild switch -I nixos-config=configuration.nix
```

## 🎄 Config States

### Default (after GUI installation with GNOME)

[c84ef93](https://github.com/itswil/nixos-config/commit/c84ef9362e78effe6c7a0c8a200a05ed92e40d65)
