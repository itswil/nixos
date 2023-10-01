# ❄️ NixOS Config

## 👷🏻‍♂️ Setup

### Temporarily install GIT

```
nix-shell -p git
```

### Clone config repo

From `~` (which is the same as `/home/USERNAME`):

```
git clone https://github.com/itswil/nixos.git
```

> Note: the default `configuration.nix` is located in `/etc/nixos`, but we will use this newly downloaded config

### Change to this directory

```
cd nixos
```

### Create a symlink for `hardware-configuration.nix`

```
ln -s /etc/nixos/hardware-configuration.nix .
```

> This is necessary because the Rebuild step (next step) requires a `hardware-configuration.nix` to be in the same location as `configuration.nix`

### Rebuild NixOS

```
sudo nixos-rebuild switch -I nixos-config=configuration.nix
```

## 🎄 Config States

### Default (after GUI installation with GNOME)

[c84ef93](https://github.com/itswil/nixos-config/commit/c84ef9362e78effe6c7a0c8a200a05ed92e40d65)

## 🔑 Modifications

Changes from the default `configuration.nix` have been marked with `##`
