# Linux

Linux is an open-source, Unix-like operating system kernel that serves as the foundation for a wide variety of operating systems (known as distributions or distros). Initially developed by Linus Torvalds in 1991, Linux has become one of the most widely used operating systems in the world, powering everything from personal computers and smartphones to servers, supercomputers, and embedded systems.

## Index

---

## Description of Each Directory in Linux

| Directory   | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| `/`         | The root directory, the starting point of the entire filesystem structure. |
| `/bin`      | Contains essential system binaries, accessible to all users, such as `ls` and `cp`. |
| `/boot`     | Contains boot-related files, including the kernel and bootloader (e.g., GRUB). |
| `/dev`      | Special files representing hardware devices, such as disks (`sda`) and terminals (`tty`). |
| `/etc`      | System configuration files and initialization scripts for services.         |
| `/home`     | Users' personal directories, where their files and configurations are stored. |
| `/lib`      | Shared libraries required by binaries in `/bin` and `/sbin`.               |
| `/media`    | Mount point for removable devices like USB drives and external disks.      |
| `/mnt`      | Directory for temporarily mounting filesystems.                            |
| `/opt`      | Optional software installed manually, typically third-party applications.  |
| `/proc`     | A virtual filesystem providing information about the kernel and running processes. |
| `/root`     | The home directory for the `root` superuser, separate from other users.    |
| `/run`      | Stores volatile runtime data, such as process IDs (PIDs) and sockets.      |
| `/sbin`     | Essential system binaries for administration, such as `fsck` and `iptables`. |
| `/tmp`      | Temporary files created by users or processes, usually cleared on reboot.  |
| `/usr`      | Contains non-essential programs and libraries, including user applications and tools. |
| `/var`      | Stores variable data like system logs, caches, and print queues.           |
