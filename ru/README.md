[English](../README.md) · [Русский](README.md)

# Реестр пакетов Dexoron

Бинарный репозиторий проектов Dexoron.
Готовые сборки для популярных дистрибутивов Linux — установка без компиляции из исходного кода.

## Пакеты

| Пакет | Описание | Платформы |
|-------|----------|-----------|
| dcr   | Утилита для управления C/C++ проектами в стиле Cargo | Arch Linux |

## Установка

### Arch Linux

Добавьте репозиторий в `/etc/pacman.conf`:

```ini
# /etc/pacman.conf
[dexoron]
SigLevel = Optional TrustAll
Server = https://dexoron.github.io/packages/archlinux/$arch
```

Обновите базу и установите:

```bash
sudo pacman -Sy dcr
```

### Debian / Ubuntu

Скоро появятся.

### Fedora / RHEL

Скоро появятся.

## Проверка

```bash
dcr --version
```

## Ссылки

- Сайт: https://dexoron.github.io/packages/ru/
- GitHub: https://github.com/dexoron/packages
