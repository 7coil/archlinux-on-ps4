# 4.a. Writing the rootfs to the partition

Here comes the fun part; putting your operating system onto the disk!

If you've downloaded Arch Linux from the Arch Linux Archive, as recommended in [Step 1](../1/files.md), then this should be relatively easy.

## 4.a.1. Command

Run this in your downloads folder! (or wherever you put the `archlinux[...].tar.gz` file)

```bash
# Extract
sudo tar --numeric-owner --strip-components=1 -xvpf archlinux-bootstrap-2022.04.05-x86_64.tar.gz -C /path/to/the/ext4/partition/

# Give the root folder the correct permissions/owner
sudo chmod 755 /path/to/the/ext4/partition/
sudo chown root:root /path/to/the/ext4/partition/
```

Before running the command, you may wish to understand/change out bits of the command.

- **Bits you have to change**
    - `archlinux-bootstrap-2022.04.05-x86_64.tar.gz`  
    Change it to the actual file name of your root filesystem
    - `/path/to/the/ext4/partition/`  
    Change it to the mount path of the `psxitarch` partition. If you're having trouble trying to find this, try:
        1. Opening the EXT4 parition in a file manager
        2. Right click > Open in terminal
        3. Run the `pwd` command, which will return the required path
        - An example of this is `/run/media/leondro/psxitarch`
- Bits you may like to change
    - `sudo`  
    If you're not root, you will need this.
    - `--strip-components=1`  
    The Arch Linux rootfs is stored within a `root.x86_64` folder; this flag removes this, extracting the rootfs directly to the required location.
- Bits you shouldn't really change
    - `--numeric-owner`  
    Makes sure that users in your current OS aren't mixed up with users within the rootfs.
    - `-x` / Extract
    - `-v` / Verbose
    - `-p` / Preserve the permissions of files and folders within the rootfs
    - `-f` / File (as in, input file!)