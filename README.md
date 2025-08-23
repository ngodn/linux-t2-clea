linux-t2-clea - Abbest Series
========

Arch Linux package for Linux kernel with bleeding edge T2 Mac support.
This is a fork maintained by **ngodn/eins0fx** for CLEA OS integration.

**Original project**: [NoaHimesaka1873/linux-t2-arch](https://github.com/NoaHimesaka1873/linux-t2-arch)

## Available Variants

- **Standard T2 Kernel**: `linux-t2` - Arch Linux kernel with T2 Mac patches
- **XanMod T2 Kernel**: `linux-t2-xanmod` - XanMod optimized kernel with T2 Mac patches

## Building

### Quick Setup (Recommended)
```sh
# Clone with submodules (includes T2 patches automatically)
git clone --recursive https://github.com/ngodn/linux-t2-clea.git
cd linux-t2-clea

# Build standard T2 kernel
makepkg -si

# OR build XanMod variant
makepkg -si -p PKGBUILD-xanmod
```

### Manual Setup (Alternative)
```sh
# If you forgot --recursive flag
git clone https://github.com/ngodn/linux-t2-clea.git
cd linux-t2-clea
git submodule update --init --recursive

# Then build as above
makepkg -si
```

## Installation

You can install the pre-built packages with:
```sh
sudo pacman -U <package-file>
```

Both variants include full T2 Mac hardware support and are part of the **Abbest** kernel series.

## Repository Structure

This project uses Git submodules to manage T2 patches:

- **Main Repository**: Contains PKGBUILD files and kernel configuration
- **Patches Submodule**: Contains T2-specific patches from [linux-t2-clea-patches](https://github.com/ngodn/linux-t2-clea-patches)

### Updating T2 Patches

To update the T2 patches to the latest version:

```sh
cd patches
git pull origin main
cd ..
git add patches
git commit -m "Update T2 patches"
git push
```

### For Developers

If you're contributing patches or modifications:

```sh
# Work on patches
cd patches
# Make your changes to patch files
git add .
git commit -m "Your patch changes"
git push origin main

# Update main repository to use new patches
cd ..
git add patches
git commit -m "Update to latest patches"
git push origin main
```