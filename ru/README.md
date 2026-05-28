[English](../README.md) · [Русский](README.md)

# Dexoron Packages

Бинарный репозиторий проектов Dexoron.
Готовые сборки для популярных дистрибутивов Linux — установка без компиляции из исходного кода.

## Пакеты

| Пакет | Описание | Платформы |
| --- | --- | --- |
| dcr | Утилита для управления C/C++ проектами в стиле Cargo | Arch · Debian · Fedora |

## Установка

### Arch Linux

1. Установите пакет с ключами для доверия к репозиторию:

```bash
curl -O https://pkg.dexoron.su/archlinux/x86_64/dexoron-keyring-20260528-1-any.pkg.tar.zst
sudo pacman -U dexoron-keyring-20260528-1-any.pkg.tar.zst
```

2. Добавьте репозиторий в `/etc/pacman.conf`:

```ini
# /etc/pacman.conf
[dexoron]
SigLevel = Required PackageOptional
Server = https://pkg.dexoron.su/archlinux/$arch

```

3. Обновите базы и установите пакет:

```bash
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

## Проверка

```bash
dcr --version

```

## Ссылки

* Сайт: [https://pkg.dexoron.su](https://pkg.dexoron.su)
* GitHub: [https://github.com/dexoron/packages](https://github.com/dexoron/packages)
