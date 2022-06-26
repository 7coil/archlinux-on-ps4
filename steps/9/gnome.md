# 9.a. Installing Gnome on Arch Linux

Gnome 42 is cool.

## 9.a.1 Installing Gnome

```bash
yay -S gnome
```

This command downloads the Gnome group of packages, including the Gnome Desktop Manager, which is the familiar login screen that we all know and love.

## 9.a.2 Enabling GDM on boot (and also immediately running GDM)

```bash
sudo systemctl enable gdm --now
```

## 9.a.3 (Optional) Disabling Wayland

You may wish to enable X11 instead of using Wayland, especially if you currently have a black screen.
Press `CTRL+ALT+F2` to change to tty2 (and F3 for tty3, F4 etc.)

To disable Wayland, uncomment the line in `/etc/gdm/custom.conf`

```conf
[daemon]
# Uncomment the line below to force the login screen to use Xorg
WaylandEnable=false
```
