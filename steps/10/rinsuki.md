# 10.a. @rinsuki / ps4linux-video-drivers

The video drivers provided in Arch Linux aren't fully compatible with the PS4.

![](./broken-drivers.jpg)

As a result, you will need to install alternative drivers.
Thankfully, @rinsuki has put in some hard work creating patches to help PS4s run 3D!

https://github.com/rinsuki/ps4linux-video-drivers

## 10.a.1. Clone the repository

To start, make a copy of the patches, and move into the directory.

```bash
git clone https://github.com/rinsuki/ps4linux-video-drivers
cd ps4linux-video-drivers
```

## 10.a.2. Building various drivers

```bash
# Start with the AMDGPU driver
cd xf86-video-amdgpu-ps4
makepkg -si
cd ..

# Move on to mesa
cd mesa-ps4
makepkg -si
cd ..
```

Happen to also be installing Steam?
You also need a 32-bit copy.

Don't forget to enable [multilib](https://wiki.archlinux.org/title/official_repositories#Enabling_multilib) first, then doing a system upgrade (yay) to fully enable it.

```bash
# Aforementioned system upgrade
yay

cd lib32-mesa-ps4
makepkg -si
cd ..
```

## 10.a.3. Restart your desktop manager

- Gnome
    - `sudo systemctl restart gdm`
