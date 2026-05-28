[English](../README.md) · [Русский](README.md)

# Dexoron Packages

Бинарный репозиторий проектов Dexoron.
Готовые сборки для популярных дистрибутивов Linux — установка без компиляции из исходного кода.

## Пакеты

| Пакет | Описание | Платформы |
|-------|----------|-----------|
| dcr   | Утилита для управления C/C++ проектами в стиле Cargo | Arch · Debian · Fedora |

## Установка

### Arch Linux

Добавьте репозиторий в `/etc/pacman.conf`:

```ini
# /etc/pacman.conf
[dexoron]
SigLevel = Required DatabaseOptional
Server = https://pkg.dexoron.su/archlinux/$arch
```

Импортируйте ключ подписи и установите:

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

## Проверка

```bash
dcr --version
```

## Ссылки

- Сайт: https://pkg.dexoron.su
- GitHub: https://github.com/dexoron/packages
