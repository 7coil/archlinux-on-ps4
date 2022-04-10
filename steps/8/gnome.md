# 8.a. Installing Gnome on Arch Linux

Gnome 42 is cool.

## 8.a.1 Installing Gnome

```bash
yay -S gnome
```

This command downloads the Gnome group of packages, including the Gnome Desktop Manager, which is the familiar login screen that we all know and love.

## 8.a.2 Disabling Wayland

X11 support on PS4 is much better (citation needed) compared to Wayland.

To disable Wayland, uncomment the line in `/etc/gdm/custom.conf`

```conf
[daemon]
# Uncomment the line below to force the login screen to use Xorg
WaylandEnable=false
```

## 8.a.3 Enabling GDM on boot (and also immediately running GDM)

```bash
sudo systemctl enable gdm --now
```

You may notice that you have a black screen at the moment.
Return to the shell by pressing `CTRL+ALT+F2`

You can return to the graphical user interface (when it works) with `CTRL+ALT+F1`

> (Writers note: Try `CTRL+ALT+F3`, `F4`, `F5` or `F6` - They're all different terminals that you can interact with!)
