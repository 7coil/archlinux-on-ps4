# Arch Linux on PS4

This repository aims to create a usable instance of Arch Linux, following the Arch Linux release cycle of roughly every month.
This is achieved by using GitHub Actions to create a new and up-to-date `psxitarch.tar.gz` on demand.

[The old instructions on how to do this manually is now in the steps folder](./steps/README.md)

These images are generated on-demand by a script and should work on all Playstation 4 consoles.

As well as the base Arch Linux packages, the following have been installed.

| Package          | Comment                              |
| ---------------- | ------------------------------------ |
| networkmanager   |                                      |
| git              |                                      |
| base-devel       |                                      |
| nano             |                                      |
| htop             |                                      |
| wget             |                                      |
| curl             |                                      |
| sudo             |                                      |
| reflector        |                                      |
| ntp              |                                      |
| mesa-git         | psxitarch GPU drivers                |
| lib32-libdrm-git | psxitarch GPU drivers                |
| lib32-mesa-git   | psxitarch GPU drivers                |
| libdrm-git       | psxitarch GPU drivers                |
| llvm14-libs      | Required for GPU acceleration in X11 |

## Downloads

To find the latest `psxitarch.tar.xz` file, go to [GitHub Actions](https://github.com/7coil/archlinux-on-ps4/actions) and download the artifact file.

## Quick Usage

1. Download a kernel (`bzImage`) and initial root file system (`initramfs.cpio.gz`)
   - https://github.com/Hakkuraifu/PS4Linux-Documentation
2. Find the `psxitarch.tar.gz` inside the artifact zip from [GitHub Actions](https://github.com/7coil/archlinux-on-ps4/actions)
3. Place all three files into a FAT32 USB mass storage device
4. Start the Linux payload with your corrupt _exfat_ USB mass storage device
   - You can use this site to help: https://hippie68.github.io/
5. Run `install-psxitarch.sh`
   - It won't work immediately. Sorry.
6. Reboot your PS4 and reload your Linux payload
7. You can now brag about using Arch Linux
8. Install a desktop environment like KDE.
