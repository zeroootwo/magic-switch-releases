# Magic Switch agent: downloads

Ready-to-use builds of the **Magic Switch agent**, the small program that lets the
Magic Switch app put your Linux computer to sleep, restart, shut down or lock it.
This repository holds only the downloads: see **[Releases](../../releases/latest)**.

[English](#english) · [Русский](#русский) · [Українська](#українська)

## English

1. Open the [latest release](../../releases/latest) and download the archive for your
   processor (`uname -m` shows it):

   | `uname -m` | Archive ends with |
   | --- | --- |
   | `x86_64` (most PCs and laptops) | `linux-amd64.tar.gz` |
   | `aarch64` (Raspberry Pi 3/4/5, ARM servers) | `linux-arm64.tar.gz` |
   | `armv7l` | `linux-armv7.tar.gz` |
   | `armv6l` (Raspberry Pi 1/Zero) | `linux-armv6.tar.gz` |
   | `i686` | `linux-386.tar.gz` |
   | `riscv64` | `linux-riscv64.tar.gz` |

2. Check the download (optional): `sha256sum -c SHA256SUMS --ignore-missing`
3. Unpack and install (no root needed):

   ```sh
   tar xzf magic-switch-agent-*-linux-amd64.tar.gz
   cd magic-switch-agent-*-linux-amd64
   ./install.sh
   ```

   The installer checks the archive fits your computer before it changes anything,
   then prints the next steps (`magic-switch-agent doctor`, then `pair`).
4. To update, repeat with the new archive: the pairing is kept.
5. To remove everything: `magic-switch-agent uninstall --purge`

The agent works on the local network only and never contacts the internet. The
Magic Switch app has a built-in guide; the archive also contains a README with
details.

## Русский

1. Откройте [последний релиз](../../releases/latest) и скачайте архив для вашего
   процессора (его показывает `uname -m`; соответствие см. в таблице выше).
2. Проверка (по желанию): `sha256sum -c SHA256SUMS --ignore-missing`
3. Распакуйте и установите (права root не нужны):

   ```sh
   tar xzf magic-switch-agent-*-linux-amd64.tar.gz
   cd magic-switch-agent-*-linux-amd64
   ./install.sh
   ```

   Установщик сначала проверяет, что архив подходит этому компьютеру, и только потом
   что-то меняет; затем показывает следующие шаги (`magic-switch-agent doctor`, потом
   `pair`).
4. Обновление: повторите с новым архивом, сопряжение сохранится.
5. Полное удаление: `magic-switch-agent uninstall --purge`

Агент работает только в локальной сети и не выходит в интернет. В приложении Magic
Switch есть встроенная справка; в архиве лежит ещё README с подробностями.

## Українська

1. Відкрийте [останній реліз](../../releases/latest) і завантажте архів для вашого
   процесора (його показує `uname -m`; відповідність дивіться в таблиці вище).
2. Перевірка (за бажанням): `sha256sum -c SHA256SUMS --ignore-missing`
3. Розпакуйте й встановіть (права root не потрібні):

   ```sh
   tar xzf magic-switch-agent-*-linux-amd64.tar.gz
   cd magic-switch-agent-*-linux-amd64
   ./install.sh
   ```

   Установник спершу перевіряє, що архів підходить цьому комп’ютеру, і лише потім
   щось змінює; далі показує наступні кроки (`magic-switch-agent doctor`, потім
   `pair`).
4. Оновлення: повторіть з новим архівом, сполучення збережеться.
5. Повне видалення: `magic-switch-agent uninstall --purge`

Агент працює лише в локальній мережі й не виходить в інтернет. У застосунку Magic
Switch є вбудована довідка; в архіві лежить ще README з подробицями.

## Terms

Copyright © 2026 Magic Switch. All rights reserved. You may install and use these
builds with the Magic Switch app. They are provided as they are, without warranty.
