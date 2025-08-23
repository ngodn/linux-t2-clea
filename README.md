linux-t2-clea - Abbest Series
========

Arch Linux package for Linux kernel with bleeding edge T2 Mac support.
This is a fork maintained by **ngodn/eins0fx** for CLEA OS integration.

**Original project**: [NoaHimesaka1873/linux-t2-arch](https://github.com/NoaHimesaka1873/linux-t2-arch)

## Available Variants

- **Standard T2 Kernel**: `linux-t2` - Arch Linux kernel with T2 Mac patches
- **XanMod T2 Kernel**: `linux-t2-xanmod` - XanMod optimized kernel with T2 Mac patches

## Building

To build the standard T2 kernel:
```sh
git clone https://github.com/ngodn/linux-t2-clea
cd linux-t2-clea
makepkg -si
```

To build the XanMod variant:
```sh
git clone https://github.com/ngodn/linux-t2-clea
cd linux-t2-clea
makepkg -si -p PKGBUILD-xanmod
```

## Installation

You can install the pre-built packages with:
```sh
sudo pacman -U <package-file>
```

Both variants include full T2 Mac hardware support and are part of the **Abbest** kernel series.