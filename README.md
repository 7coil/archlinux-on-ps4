# Arch Linux on PS4

_Why would you use someone else's distro, when you can start from scratch?_

I'm using Arch Linux to run these steps, but these steps may be reproducable on other operating systems.

## Guide

> (Writers note: Feel free to ignore these writers notes, especially if you're not technically inclined; these notes are for those who feel like they're up for a challenge.)

1. Fetching Files
    - [From the internet!](./steps/1/files.md)
2. Partitioning your filesystem
    - [Using Gnome Disks](./steps/2/gnome-disks.md)
3. Placing Files / Mounting Partitions!
    - [Using a file manager!](./steps/3/gnome-files.md)
4. Writing the rootfs to the EXT4 partition
    - [With the terminal!](./steps/4/rootfs.md)
5. Initialising the operating system
    - [Like a professional](https://wiki.archlinux.org/title/Installation_guide)
6. Use your PS4 payload to run the Linux loader
    - This page hasn't been created, as it is assumed that you already know how to do this.  
    If you really need a tutorial, create an issue or help by creating a PR
7. Install a AUR Helper
    - [yay](https://github.com/Jguer/yay)
8. Installing a desktop environment
    - [gnome](./steps/8/gnome.md)
9. Fixing Video Drivers
    - [Using rinsuki/ps4linux-video-drivers](./steps/9/rinsuki.md)

## Extras
- If you're trying to install Steam, you should be able to follow the instructions within the [Arch Linux Wiki](https://wiki.archlinux.org/title/steam)
    - If there's any missing graphics drivers, see if that folder exists (during Step 9)