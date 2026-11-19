# Magic Switch: downloads

**Magic Switch** wakes your computers from your phone with Wake-on-LAN, and with the small
**agent** installed on them it can also shut down, restart, sleep and lock them.
No accounts, no ads, no tracking.

**Website: [magicswitch.app](https://magicswitch.app)** (English, Русский, Українська, Deutsch, Español, Français) ·
[Privacy policy](https://magicswitch.app/privacy/) · [Support the project](https://www.paypal.com/ncp/payment/KGBAWPS7WMUZ8)

This repository holds only the downloads: see **[Releases](../../releases)**.
The app for iPhone, iPad and Mac is not out yet.

[English](#english) · [Русский](#русский) · [Українська](#українська)

## English

### Linux

| What | File in the [app release](../../releases/tag/app-v1.0.1) |
| --- | --- |
| App for Debian, Ubuntu, Mint | `magic-switch_<version>_amd64.deb` |
| App for Fedora, openSUSE | `magic-switch-<version>-1.x86_64.rpm` |
| App for any other distribution (installs into your home folder, no root) | `Magic-Switch-<version>-linux-x64.tar.gz`, then `./install.sh` |

### Windows

Download `Magic-Switch-<version>-windows-setup.exe` from the [app release](../../releases/tag/app-v1.0.1) and run it.
It installs the app, and the agent if you leave that option ticked. The file is not signed with a
publisher certificate, so Windows may show a SmartScreen warning: choose **More info**, then **Run anyway**.

### The agent (on the computer you want to control)

The fastest way on Linux and macOS, one command. It checks the signature of the download first and needs no root:

```sh
curl -fsSL https://github.com/zeroootwo/magic-switch-releases/releases/download/app-latest/get.sh | sh
```

Other ways, from the [agent release](../../releases/latest):

- **Debian, Ubuntu:** `sudo apt install ./magic-switch-agent_<version>_<arch>.deb`
- **Fedora, openSUSE:** `sudo dnf install --nogpgcheck ./magic-switch-agent-<version>-1.<arch>.rpm`
- **Arch Linux:** download `PKGBUILD` from the release, then `makepkg -si`
- **Any Linux, by hand:** the archive for your processor (`uname -m` shows it):

  | `uname -m` | Archive ends with |
  | --- | --- |
  | `x86_64` (most PCs and laptops) | `linux-amd64.tar.gz` |
  | `aarch64` (Raspberry Pi 3/4/5, ARM servers) | `linux-arm64.tar.gz` |
  | `armv7l` | `linux-armv7.tar.gz` |
  | `armv6l` (Raspberry Pi 1/Zero) | `linux-armv6.tar.gz` |
  | `i686` | `linux-386.tar.gz` |
  | `riscv64` | `linux-riscv64.tar.gz` |

  ```sh
  tar xzf magic-switch-agent-*-linux-amd64.tar.gz
  cd magic-switch-agent-*-linux-amd64
  ./install.sh
  ```

After installing the agent run `magic-switch-agent doctor`, then `magic-switch-agent pair` and enter
the code in the app. To update, install the new version over the old one: the pairing is kept.
To remove everything: `magic-switch-agent uninstall --purge`.

### Is the download genuine?

Every release carries a list of files signed with the author's Ed25519 key; `get.sh` and the apps check
that signature and the SHA-256 of each file before installing anything. By hand:
`sha256sum -c SHA256SUMS --ignore-missing`. The agent works on the local network only and never
contacts the internet.

## Русский

**Сайт: [magicswitch.app](https://magicswitch.app)** · [Политика конфиденциальности](https://magicswitch.app/privacy/) ·
[Поддержать проект](https://www.paypal.com/ncp/payment/KGBAWPS7WMUZ8). Приложения для iPhone, iPad и Mac пока нет.

- **Приложение для Linux:** `.deb` (Debian, Ubuntu, Mint), `.rpm` (Fedora, openSUSE) или архив `Magic-Switch-<версия>-linux-x64.tar.gz` с `./install.sh` (в домашнюю папку, без root). Файлы лежат в [релизе приложения](../../releases/tag/app-v1.0.1).
- **Windows:** скачайте `Magic-Switch-<версия>-windows-setup.exe` из того же релиза и запустите. Он ставит приложение и, если оставить галочку, агента. Файл без сертификата издателя, поэтому Windows может показать предупреждение SmartScreen: нажмите «Подробнее», затем «Выполнить в любом случае».
- **Агент (на компьютере, которым управляете):** одна команда для Linux и macOS, она сначала проверяет подпись загрузки и не требует root:

  ```sh
  curl -fsSL https://github.com/zeroootwo/magic-switch-releases/releases/download/app-latest/get.sh | sh
  ```

  Или из [релиза агента](../../releases/latest): `.deb` (`sudo apt install ./…deb`), `.rpm` (`sudo dnf install --nogpgcheck ./…rpm`), для Arch скачайте `PKGBUILD` и выполните `makepkg -si`, либо архив для вашего процессора (его показывает `uname -m`; таблица выше), затем `./install.sh`.
- После установки агента: `magic-switch-agent doctor`, затем `magic-switch-agent pair`, код вводите в приложении. Обновление: установите новую версию поверх, сопряжение сохранится. Полное удаление: `magic-switch-agent uninstall --purge`.
- **Проверка подлинности:** каждый релиз содержит список файлов, подписанный ключом автора Ed25519; `get.sh` и приложения проверяют подпись и SHA-256 каждого файла. Вручную: `sha256sum -c SHA256SUMS --ignore-missing`. Агент работает только в локальной сети и не выходит в интернет.

## Українська

**Сайт: [magicswitch.app](https://magicswitch.app)** · [Політика конфіденційності](https://magicswitch.app/privacy/) ·
[Підтримати проєкт](https://www.paypal.com/ncp/payment/KGBAWPS7WMUZ8). Застосунку для iPhone, iPad і Mac поки немає.

- **Застосунок для Linux:** `.deb` (Debian, Ubuntu, Mint), `.rpm` (Fedora, openSUSE) або архів `Magic-Switch-<версія>-linux-x64.tar.gz` з `./install.sh` (у домашню теку, без root). Файли лежать у [релізі застосунку](../../releases/tag/app-v1.0.1).
- **Windows:** завантажте `Magic-Switch-<версія>-windows-setup.exe` з того ж релізу й запустіть. Він ставить застосунок і, якщо залишити позначку, агента. Файл без сертифіката видавця, тому Windows може показати попередження SmartScreen: натисніть «Докладніше», потім «Все одно виконати».
- **Агент (на комп’ютері, яким керуєте):** одна команда для Linux і macOS, вона спершу перевіряє підпис завантаження й не потребує root:

  ```sh
  curl -fsSL https://github.com/zeroootwo/magic-switch-releases/releases/download/app-latest/get.sh | sh
  ```

  Або з [релізу агента](../../releases/latest): `.deb` (`sudo apt install ./….deb`), `.rpm` (`sudo dnf install --nogpgcheck ./….rpm`), для Arch завантажте `PKGBUILD` і виконайте `makepkg -si`, або архів для вашого процесора (його показує `uname -m`; таблиця вище), потім `./install.sh`.
- Після встановлення агента: `magic-switch-agent doctor`, потім `magic-switch-agent pair`, код вводьте в застосунку. Оновлення: встановіть нову версію поверх, сполучення збережеться. Повне видалення: `magic-switch-agent uninstall --purge`.
- **Перевірка справжності:** кожен реліз містить список файлів, підписаний ключем автора Ed25519; `get.sh` і застосунки перевіряють підпис та SHA-256 кожного файлу. Вручну: `sha256sum -c SHA256SUMS --ignore-missing`. Агент працює лише в локальній мережі й не виходить в інтернет.

## Terms

Copyright © 2026 Magic Switch. All rights reserved. You may install and use these
builds with the Magic Switch app. They are provided as they are, without warranty.
