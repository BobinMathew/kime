# kime

Korean IME

## Why kime

* Well tested input engine
* Low memory footprint
* Write in Rust no segfaults
* Allow custom layouts

## Supported frontend

- [x] XIM
- [ ] Wayland
- [ ] GTK2
- [x] GTK3
- [ ] GTK4
- [ ] Qt4
- [ ] Qt5

## Installation

### Arch Linux

you can install from AUR package [kime](https://aur.archlinux.org/packages/kime) for latest release, or [kime-git](https://aur.archlinux.org/packages/kime-git) if you want to build from source.

### Debian

you can install from .deb file at [releases](https://github.com/Riey/kime/releases) tab.

### Build from source

make sure **cargo** and other dependencies listed below are installed before build.

```sh
git clone https://github.com/Riey/kime
cd kime

cargo build --release

pkg/release.sh

# You can now install files from build/out
# or use script in pkg/install.sh
# e.g. sudo pkg/install.sh
```

## Configuration

add the following to .xprofile or .xinitrc and restart X:

```sh
export GTK_IM_MODULE=kime
kime-xim &
export XMODIFIERS=@im=kime
```

read [CONFIGURATION.md](CONFIGURATION.md) for detailed options.

## Dependencies

### GTK3

* gtk3
* pango

### XIM

* libxcb
* cairo
