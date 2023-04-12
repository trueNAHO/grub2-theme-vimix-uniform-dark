<h1 align="center">
  Simple, very dark blue
  <a href="https://www.gnu.org/software/grub/">GRUB</a> theme.
</h1>

<p align="center">
  <a href="https://github.com/trueNAHO/grub2-theme-vimix-very-dark-blue/stargazers"
    ><img
      src="https://img.shields.io/github/stars/trueNAHO/grub2-theme-vimix-very-dark-blue?colorA=363a4f&colorB=b7bdf8&style=for-the-badge"
      alt="Stars: N/A"
  /></a>
  <a href="https://github.com/trueNAHO/grub2-theme-vimix-very-dark-blue/issues"
    ><img
      src="https://img.shields.io/github/issues/trueNAHO/grub2-theme-vimix-very-dark-blue?colorA=363a4f&colorB=f5a97f&style=for-the-badge"
      alt="Issues: N/A"
  /></a>
  <a href="https://github.com/trueNAHO/grub2-theme-vimix-very-dark-blue/contributors"
    ><img
      src="https://img.shields.io/github/contributors/trueNAHO/grub2-theme-vimix-very-dark-blue?colorA=363a4f&colorB=a6da95&style=for-the-badge"
      alt="Issues: N/A"
  /></a>
</p>

<h1 align="center">
  <img src="docs/preview.png" alt="PREVIEW" width="100%" />
</h1>

<!--toc:start-->
- [Features](#features)
- [Installation](#installation)
  - [Download](#download)
  - [Setup](#setup)
- [Installation Size](#installation-size)
- [Related](#related)
- [Contributing](#contributing)
- [License](#license)
<!--toc:end-->

## Features

- Stand out from the crowd with a boot process that radiates professionalism and
  modernity thanks to the simple and elegant design of this theme.
- Elevate your boot process to the next level with the addition of distribution
  logos.
- Effortlessly enhance your boot experience with the easy-to-install theme that
  is compatible with most Linux distributions.
- The dark blue color scheme creates a sense of elegance and visual appeal that
  makes your boot process perfect for both day and night use.
- This theme embodies the philosophy that simplicity is the ultimate form of
  sophistication.
- Say goodbye to squinting at your boot messages with the [Fira
  Code](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)
  font — readability has never been easier.
- Instead of overwhelming the user with unnecessary details, this theme allows
  the beauty of simplicity to shine through.

## Installation

Please note that installation procedures may vary across different Linux
distributions. If you're using [Fedora](https://getfedora.org), you can find
detailed instructions on the [Fedora Project
Wiki](https://fedoraproject.org/wiki/GRUB_2).

### Download

To install this theme from the
[AUR](https://aur.archlinux.org/packages/grub-theme-vimix-very-dark-blue) with
an [AUR helper](https://wiki.archlinux.org/title/AUR_helpers) like
[`yay`](https://github.com/Jguer/yay), run the following command:

```bash
yay -S grub-theme-vimix-very-dark-blue
```

Alternatively, install this theme with the `cp`, `git`, `install`, `mktemp`,
and `rm` utilities:

```bash
(
    GRUB_THEME_INSTALL_PATH="/usr/share/grub/themes/grub-theme-vimix-very-dark-blue" &&
        GRUB_THEME_REPO_URL="https://github.com/trueNAHO/grub2-theme-vimix-very-dark-blue.git" &&
        TMP_DIR="$(mktemp --directory)" &&
        git clone "$GRUB_THEME_REPO_URL" "$TMP_DIR" &&
        install --directory --mode 755 "$GRUB_THEME_INSTALL_PATH" &&
        cp \
            --no-preserve=ownership \
            --recursive \
            "$TMP_DIR/src/." \
            "$GRUB_THEME_INSTALL_PATH" &&
        rm --force --recursive "$TMP_DIR"
)
```

### Setup

To apply this theme, update the `GRUB_THEME` line in the `/etc/default/grub`
file to the following:

```bash
GRUB_THEME="/usr/share/grub/themes/grub-theme-vimix-very-dark-blue/theme.txt"
```

Then, generate the [GRUB](https://www.gnu.org/software/grub) configuration file
with superuser privileges by running the following command:

```bash
grub-mkconfig -o /boot/grub/grub.cfg
```

The system will start using the new theme after the next reboot.

## Installation Size

Boot partitions are often handled differently from other partitions, and may
have stricter size limitations.

The space usage by file length is as follows:

```bash
$ dust --apparent-size --number-of-lines 5 --terminal_width 60 src/
 63K   ┌── Fira_Code_Regular_22.pf2│            █████ │  26%
5.1K   │ ┌── lfs.png               │     ░░░░░░░░░░░█ │   2%
5.2K   │ ├── slackware.png         │     ░░░░░░░░░░░█ │   2%
5.3K   │ ├── gnu-linux.png         │     ░░░░░░░░░░░█ │   2%
158K   ├─┴ icons                   │     ████████████ │  65%
244K ┌─┴ src                       │█████████████████ │ 100%
```

The space usage with a block length of 4 KB is as follows:

```bash
$ dust --number-of-lines 5 --terminal_width 60 src/
 64K   ┌── Fira_Code_Regular_22.pf2│              ███ │  16%
8.0K   │ ┌── ubuntu.png            │     ░░░░░░░░░░░█ │   2%
8.0K   │ ├── windows.png           │     ░░░░░░░░░░░█ │   2%
8.0K   │ ├── xubuntu.png           │     ░░░░░░░░░░░█ │   2%
268K   ├─┴ icons                   │     ████████████ │  65%
412K ┌─┴ src                       │█████████████████ │ 100%
```

## Related

- [Commitizen](http://commitizen.github.io/cz-cli)
  - Simple commit conventions for internet citizens.
- [Fira
  Code](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)
  - Free monospaced font with programming ligatures.
- [GNU GRUB](https://www.gnu.org/software/grub)
  - GNU GRand Unified Bootloader.
- [GRUB2 Theme Vimix](https://github.com/Se7endAY/grub2-theme-vimix)
  - Blur theme for [GRUB](https://www.gnu.org/software/grub).
- [`dust`](https://github.com/bootandy/dust)
  - A more intuitive version of `du` in Rust.
- [`grub2-theme-preview`](https://github.com/hartwork/grub2-theme-preview)
  - Preview a full [GRUB](https://www.gnu.org/software/grub) 2.x theme (or just
    a background image) using KVM/QEMU.
- [`oxipng`](https://github.com/shssoichiro/oxipng)
  - Multithreaded PNG optimizer written in Rust.
- [`svgcleaner`](https://github.com/RazrFalcon/svgcleaner)
  - Clean up SVG files from unnecessary data.

## Contributing

For information on contributing to this project, please refer to
[CONTRIBUTING.md](docs/CONTRIBUTING.md).

## License

This project is licensed under [GNU GENERAL PUBLIC LICENSE Version 3](LICENSE).
