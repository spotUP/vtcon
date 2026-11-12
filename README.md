# UP-Term for AmigaOS

A modern terminal, a Unix userland and a flat desktop for AmigaOS 3.x (68020 or better, AmigaOS 3.0 and up; tested most on 3.2). This repository holds the release archives and the upkg package feed; the source is [spotUP/UP-Term](https://github.com/spotUP/UP-Term).

- **UP-Term**: a console window (`XCON:`) with a real terminal inside: 16, 256 and RGB colours, mouse, tabs, sixel and kitty pictures. Unix ports (the bash-compatible `vsh`, vim, tmux, less, git, ssh, curl) and Amiga programs both render right.
- **Amarchy**: a desktop suite on top of Workbench: Left Amiga key shortcuts for the whole machine, a bar, menus, notices, themes, and a flat look for system gadgets and Preferences programs.
- **upkg**: a package manager with a feed of 28 add-ons, from the Shell or a Workbench window.

![The Amarchy desktop](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/amarchy-desktop.png)

| | |
|---|---|
| ![A Unix program in an UP-Term window](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/terminal-unix.png) | ![A picture in the terminal through the kitty graphics protocol](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/terminal-kitty-picture.png) |
| ![The upkg package browser](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/upkg-browser.png) | ![A Preferences program with the flat look](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/prefs-flat.png) |

![A Directory Opus lister](https://raw.githubusercontent.com/spotUP/UP-Term/main/docs/screenshots/dopus-lister.png)

## Download

Get the archives from the [latest release](https://github.com/spotUP/vtcon/releases/latest) (1.1).

| Archive | What it is | Use it when |
|---|---|---|
| [`up-term.lha`](https://github.com/spotUP/vtcon/releases/latest/download/up-term.lha) (33 MB) | The base kit: terminal, Amarchy, Unix userland, upkg | The Amiga has a network: add-ons come through upkg |
| [`up-term-full.lha`](https://github.com/spotUP/vtcon/releases/latest/download/up-term-full.lha) (70 MB) | The base kit plus all 28 packages in a `Packages` drawer | The Amiga has no network |
| `up-claude.lha`, `up-dopus.lha`, `up-nvim.lha`, `up-pi.lha`, `up-python.lha`, `up-uhc.lha` | Add-ons with their own Install | You want one add-on without upkg |
| `up-term-src.lha` | The sources of everything shipped | |

The other files of a release (`Packages`, `Packages.gz`, `upkg-index.txt`, the `.ipk` files) are the upkg feed; upkg reads them, you do not need to download them.

## What you need

- An Amiga, or an FPGA or emulated Amiga, with a 68020 or better and AmigaOS 3.0 or newer. Install refuses a 68000.
- `lha` to unpack the archive, and Installer for the Install icon (AmigaOS 3.2 has it; a Shell route exists without it).
- Only for the network parts: a TCP/IP stack (Roadshow, Miami or AmiTCP), and AmiSSL 5 for curl.

## Install

1. Copy the archive to the Amiga and unpack it: `lha x up-term.lha`.
2. Double-click `Install` in the `up-term` drawer. From a Shell without Installer: `CD` into the drawer, then `Execute Files/install.dos Files`.
3. Reboot when Install offers to.
4. Add-ons, with a TCP/IP stack running: open an UP-Term window, type `upkg update`, then `upkg browse` (or double-click `UP-Term:bin/upkg` on Workbench). From the full kit, with no network: in a Shell, `CD` to the unpacked drawer and `Execute Install-Packages`.

Remove everything again: double-click `Uninstall`.

## Update

Install a newer kit over the old one: Install names both versions and offers Update, which copies only the files that changed and keeps your choices. Add-ons: `upkg update`, then `upkg upgrade`.

## Packages

Each package is named `up-<name>`: claude, pi, nvim, python, git, perl, vim, bitchx, vbcc, mutt, lynx, joe, mg, nano, tig, ncdu, nnn, lua, jq, hexedit, picocom, nc, fzy, ctags, zip, dopus, uhc, sqlite3.

`upkg list` shows them with versions; `upkg install up-git` installs one.

## Documentation

- `README.txt` in the kit, also [online](https://github.com/spotUP/UP-Term/blob/main/dist/README.txt): install, update, use, menu, keys, tmux, Amarchy, serial login, network, add-ons.
- [Release notes](https://github.com/spotUP/vtcon/releases): changes and known issues per release.
- Licences: `LICENSES.txt` in the kit, also [online](https://github.com/spotUP/UP-Term/blob/main/dist/LICENSES.txt).
