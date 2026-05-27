[English](README.md) · [Русский](ru/README.md)

# Dexoron Package Registry

Binary package repository for Dexoron projects.
Precompiled packages for multiple Linux distributions — install without building from source.

## Packages

| Package | Description | Platforms |
|---------|-------------|-----------|
| dcr     | Utility for managing C/C++ projects in a Cargo-like style | Arch Linux |

## Setup

### Arch Linux

Add the repository to `/etc/pacman.conf`:

```ini
# /etc/pacman.conf
[dexoron]
SigLevel = Optional TrustAll
Server = https://dexoron.github.io/packages/archlinux/$arch
```

Refresh and install:

```bash
sudo pacman -Sy dcr
```

### Debian / Ubuntu

Coming soon.

### Fedora / RHEL

Coming soon.

## Verify

```bash
dcr --version
```

## Links

- Website: https://dexoron.github.io/packages/
- GitHub: https://github.com/dexoron/packages
