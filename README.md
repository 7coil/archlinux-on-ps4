# Arch Linux on PS4

_Why would you use someone else's distro, when you can start from scratch?_

I'm using Arch Linux to run these steps, but these steps may be reproducable on other operating systems.
For instance, the _Chrooting_ step may be done within Microsoft Windows WSL.

## Pre-Made Root Filesystems

To save time, I have done most of the heavy lifting and done all steps (except for step 8), to save time.

1. Simply [fetch all the files](./steps/1/files.md), and grab your root filesystem here [releases](https://github.com/7coil/archlinux-on-ps4/releases)
2. Plop all of these files onto a FAT32 formatted USB stick.
3. Use your PS4 payload to run the Linux loader
    - Instructions on how to do so are not included, as it is out of scope for this repository.  
    ...but if you really wanted it, create a GitHub issue.
4. Run `install-psxitarch.sh` in the rescue shell
5. Install a desktop environment!
    - [gnome](./steps/8/gnome.md)

## Doing it from Scratch Guide

> (Writers note: Feel free to ignore these writers notes, especially if you're not technically inclined; these notes are for those who feel like they're up for a challenge.)

These instructions were written as I was performing them, so some instructions may be missing. Create a GitHub issue if you find anything wrong.

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
8. Make sure the time is set!
    - [Use `sudo timedatectl set-time "yyyy-MM-dd hh:mm:ss"` to set the date/time](https://wiki.archlinux.org/title/System_time#Set_system_clock)
    - [Install NTP](https://wiki.archlinux.org/title/Network_Time_Protocol_daemon) to make sure your clock is always correct in the future.
9. Installing a desktop environment
    - [gnome](./steps/9/gnome.md)
    - [kde](./steps/9/kde.md)
10. Fixing Video Drivers
    - [Using rinsuki/ps4linux-video-drivers](./steps/10/rinsuki.md)

## Extras
- If you're trying to install Steam, you should be able to follow the instructions within the [Arch Linux Wiki](https://wiki.archlinux.org/title/steam)
    - If there's any missing graphics drivers, see if that folder exists (during Step 9)
- Making your own `psxitarch.tar.xz` image:
    - You can use `tar -cvJzf psxitarch.tar.xz `
