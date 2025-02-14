<!-- # [ zrfisaac ] -->

<!-- # [ about ] -->
<!-- # - author : Isaac Caires -->
<!-- # . - email : zrfisaac@gmail.com -->
<!-- # . - site : zrfisaac.github.io -->
<!-- # - version : zrfisaac.wiki.en.archlinux : 0.0.1 -->

<!-- # [ markdown ] -->
# Arch Linux

## Description
Arch Linux is a lightweight, rolling-release distro for advanced users, offering full customization and the latest updates. It features Pacman and AUR for extensive software support.

---

## Index
- Default
  - dd : `dd bs=4M if=/zrfisaac/repository/os/archlinux/archlinux-amd64.iso of=/dev/sda conv=fsync oflag=direct status=progress`
  - /etc/default/grub : `cryptdevice=UUID=7b927af8-fd64-4dcc-9c4e-a9819b6d150c:ZRFISAAC`
  - /etc/mkinitcpio.conf : `HOOKS=(base udev autodetect microcode modconf kms keyboard keymap consolefont block ` **encrypt** ` filesystems fsck)`
- [Shell](#shell)
  - [USB flash installation medium](#usb-flash-installation-medium)

---

## [Shell](#index)

### [USB flash installation medium](#index)

- using `cat` :
```bash
cat /zrfisaac/repository/os/archlinux/archlinux-amd64.iso > /dev/sda
```

- using `cp` :
```bash
cp /zrfisaac/repository/os/archlinux/archlinux-amd64.iso /dev/sda
```

- using `dd` :
```bash
dd bs=4M if=/zrfisaac/repository/os/archlinux/archlinux-amd64.iso of=/dev/sda conv=fsync oflag=direct status=progress
```

- using `tee` :
```bash
tee < /zrfisaac/repository/os/archlinux/archlinux-amd64.iso > /dev/sda
```

- using `pv` :
```bash
pv /zrfisaac/repository/os/archlinux/archlinux-amd64.iso -Yo /dev/sda
```
