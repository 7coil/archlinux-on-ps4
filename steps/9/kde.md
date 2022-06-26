# 9.b. Installing Plasma Desktop on Arch Linux

Plasma Desktop is pretty cool.

## 9.a.1 Installing KDE Plasma

```bash
yay -S plasma-desktop
```

When questioned on the following choices, I did the following, but any other choice should be valid.

```
2) pipewire-jack
1) pipewire-media-session
1) gnu-free-fonts
1) phonon-qt5-gstreamer
```

## 9.a.2 Installing the Simple Desktop Display Manager (SDDM)

Although you have a desktop, you do not have a login screen - SDDM fills in this role!

```bash
yay -S sddm sddm-kcm
```

> (Writers note: `sddm-kcm` is for the KConfig Module... according to the [Arch Wiki](https://wiki.archlinux.org/title/SDDM))

## 9.a.3 Installing Desktop Applications

You may wish to install some Desktop applications before you enter KDE with no way of using it.

```bash
yay -S firefox konsole
```

## 9.a.4 Enabling SDDM on boot (and also immediately running SDDM)

```bash
sudo systemctl enable sddm --now
```
