[English](README.md) · [Русский](ru/README.md)

# Dexoron Packages

Binary package repository for Dexoron projects.
Precompiled packages for multiple Linux distributions — install without building from source.

## Packages

| Package | Description | Platforms |
|---------|-------------|-----------|
| dcr     | Utility for managing C/C++ projects in a Cargo-like style | Arch · Debian · Fedora |

## Setup

### Arch Linux

Add the repository to `/etc/pacman.conf`:

```ini
# /etc/pacman.conf
[dexoron]
SigLevel = Required DatabaseOptional
Server = https://pkg.dexoron.su/archlinux/$arch
```

Import the signing key and install:

```bash
sudo pacman-key --recv-keys 74322D39483E9C9E8C86C0AA0770A5C2A2A82DAC
sudo pacman-key --lsign-key 74322D39483E9C9E8C86C0AA0770A5C2A2A82DAC
sudo pacman -Sy dcr
```

### Debian / Ubuntu

```bash
curl -fsSL https://pkg.dexoron.su/dexoron.gpg | sudo tee /etc/apt/trusted.gpg.d/dexoron.asc > /dev/null
echo "deb [signed-by=/etc/apt/trusted.gpg.d/dexoron.asc] https://pkg.dexoron.su/debian ./" | sudo tee /etc/apt/sources.list.d/dexoron.list
sudo apt update && sudo apt install dcr
```

### Fedora / RHEL

```bash
sudo curl -fsSL https://pkg.dexoron.su/fedora/x86_64/dexoron.repo -o /etc/yum.repos.d/dexoron.repo
sudo dnf install dcr
```

## Verify

```bash
dcr --version
```

## Links

- Website: https://pkg.dexoron.su
- GitHub: https://github.com/dexoron/packages
