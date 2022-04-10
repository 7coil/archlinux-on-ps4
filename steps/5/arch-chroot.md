# 5.a. Initialising Arch Linux

Just like how you would do it from a LiveCD, this step outlines how to set-up your Arch Linux installation.

The following instructions assume that your terminal is currently located within the `psxitarch` EXT4 folder.

> (Writers note: `yay` is my preferred AUR helper.)

## 5.a.1. Select your mirrors

Uncomment your favourite/local mirror service, by editing the `etc/pacman.d/mirrorlist` file.

```bash
# NOT /etc/pacman.d/mirrorlist
# You want to edit the file on the USB, not your local Arch installation.
sudo nano etc/pacman.d/mirrorlist
```

I uncommented the Kentish `mirrorservice.org`, because I live within the United Kingdom, and who doesn't love the University of Kent?

## 5.a.2. Start your chroot

```bash
# Only if you have `arch-install-scripts` installed
sudo arch-chroot "$(pwd)"
```

```bash
# If you don't have `arch-install-scripts` installed
cp /etc/resolv.conf /tmp/root.x86_64/etc
mount --rbind /proc /tmp/root.x86_64/proc
mount --rbind /sys /tmp/root.x86_64/sys
mount --rbind /dev /tmp/root.x86_64/dev
mount --rbind /run /tmp/root.x86_64/run
chroot /tmp/root.x86_64/
```

## 5.a.3. Set your internationalisation settings

Follow the Arch Wiki steps on _Time Zone_, _Localisation_ and _Network Configuration_

[Arch Wiki](https://wiki.archlinux.org/title/Installation_guide)

## 5.a.3. Update your system

```bash
# Initialising and setting up your keyring
pacman-key --init
pacman-key --populate archlinux

# Upgrade your system
pacman -Syu

# Installs system utilities and tools
pacman -S networkmanager nano htop wget curl sudo

# Auto-start the networking
systemctl enable NetworkManager
```

## 5.a.4. Create a new user

```bash
useradd leondro -m -G wheel
```

This command creates the `leondro` account, and puts them within the `wheel` group.

> (Writers note: It's very unlikely your name is also `leondro`, give it a change before you run the command.)

## 5.a.5. Set the sudoers group.

In this installation, the `wheel` group is our sudoers group.

Edit `/etc/sudoers` and uncomment (the bit before the %) to enable the use of `sudo`.

```
## Same thing without a password
%wheel ALL=(ALL:ALL) NOPASSWD: ALL
```

> (Writers note: You may also wish to force yourself to type a password every time you use sudo, just uncomment the other line above.)

## 5.a.6. Set your password!

Don't forget to set your passwords!

```bash
passwd
passwd leondro
```
