# Arch Linux on PS4

_Why would you use someone else's distro, when you can start from scratch?_

I'm using Arch Linux to run these steps, but these steps may be reproducable on other operating systems.

## Guide

> (Writers note: Feel free to ignore these writers notes, especially if you're not technically inclined; these notes are for those who feel like they're up for a challenge.)

In each step, choose one (and only one) of the bullet points to follow, depending on what you like/are using.

1. Fetching Files
    - [From the internet!](./steps/1/files.md)
2. Partitioning your filesystem
    - [Using Gnome Disks](./steps/2/gnome-disks.md)
3. Placing Files / Mounting Partitions!
    - [Using a file manager!](./steps/3/gnome-files.md)
4. Writing the rootfs to the EXT4 partition
    - [With the terminal!](./steps/4/rootfs.md)
5. Initialising the operating system
    - [Chrooting](./steps/5/arch-chroot.md)
6. Use your PS4 payload to run the Linux loader
    - Instructions on how to do so are not included, as it is out of scope for this repository.  
    ...but if you really wanted it, create a GitHub issue.
7. Install a AUR Helper
    - [yay](https://github.com/Jguer/yay)
8. Installing a desktop environment
    - [gnome](./steps/8/gnome.md)
9. Fixing Video Drivers
    - [Using rinsuki/ps4linux-video-drivers](./steps/9/rinsuki.md)

## Extras
- If you're trying to install Steam, you should be able to follow the instructions within the [Arch Linux Wiki](https://wiki.archlinux.org/title/steam)
    - If there's any missing graphics drivers, see if that folder exists (during Step 9)
